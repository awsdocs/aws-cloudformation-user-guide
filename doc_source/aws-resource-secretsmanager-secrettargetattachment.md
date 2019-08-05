# AWS::SecretsManager::SecretTargetAttachment<a name="aws-resource-secretsmanager-secrettargetattachment"></a>

The `AWS::SecretsManager::SecretTargetAttachment`resource completes the final link between a Secrets Manager secret and its associated database\. This is required because each has a dependency on the other\. No matter which one you create first, the other doesn't exist yet\. To resolve this, you must create the resources in the following order:

1. Define the secret without referencing the service or database\. You can't reference the service or database because it doesn't exist yet\.

1. Next, define the service or database\. Include the reference to the secret to use its stored credentials to define the database's master user and password\.

1. Finally, define a `SecretTargetAttachment`resource type to finish configuring the secret with the required database engine type and the connection details of the service or database\. These details are required by a rotation function, if one is attached later by defining a [AWS::SecretsManager::RotationSchedule ](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-secretsmanager-rotationschedule.html) resource type\.

## Syntax<a name="aws-resource-secretsmanager-secrettargetattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-secretsmanager-secrettargetattachment-syntax.json"></a>

```
{
  "Type" : "AWS::SecretsManager::SecretTargetAttachment",
  "Properties" : {
      "[SecretId](#cfn-secretsmanager-secrettargetattachment-secretid)" : String,
      "[TargetId](#cfn-secretsmanager-secrettargetattachment-targetid)" : String,
      "[TargetType](#cfn-secretsmanager-secrettargetattachment-targettype)" : String
    }
}
```

### YAML<a name="aws-resource-secretsmanager-secrettargetattachment-syntax.yaml"></a>

```
Type: AWS::SecretsManager::SecretTargetAttachment
Properties:
  [SecretId](#cfn-secretsmanager-secrettargetattachment-secretid): String
  [TargetId](#cfn-secretsmanager-secrettargetattachment-targetid): String
  [TargetType](#cfn-secretsmanager-secrettargetattachment-targettype): String
```

## Properties<a name="aws-resource-secretsmanager-secrettargetattachment-properties"></a>

`SecretId`  <a name="cfn-secretsmanager-secrettargetattachment-secretid"></a>
The Amazon Resource Name \(ARN\) or the friendly name of the secret that contains the credentials that you want to use with the specified service or database\. To reference a secret that's also created in this template, use the see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetId`  <a name="cfn-secretsmanager-secrettargetattachment-targetid"></a>
The ARN of the service or database whose credentials are stored in the specified secret\.
*Required*: Yes
*Type*: String
*Minimum*: `20`
*Maximum*: `2048`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-secretsmanager-secrettargetattachment-targettype"></a>
A string used by the Secrets Manager console to determine how to parse the structure of the secret text and place the values in the proper fields of the console user interface\. If you created this secret using the Secrets Manager console then we recommend that you do not modify this value\. If this is a custom secret, then this field is available for your use\. As a best practice, do not store any sensitive information in this field\. Instead, store sensitive information in the `SecretString` or `SecretBinary` fields to ensure that it is encrypted\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-secretsmanager-secrettargetattachment-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-secrettargetattachment-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::SecretTargetAttachement` resource to the intrinsic `Ref` function, the function returns the ARN of the secret, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

This enables you to reference a secret that you create in one part of the stack template from within the definition of another resource from a different part of the same template\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-secretsmanager-secrettargetattachment--examples"></a>

### Creating a Secret and an RDS DB Instance<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Secret_and_an_RDS_DB_Instance"></a>

The following example creates a secret,and then creates an Amazon RDS DB instance by using the credentials found in the secret for the new database's master user and password\. Finally, it updates the secret with the connection details of the database by defining the `SecretTargetAttachment`object\.

**Note**
The JSON specification doesn't allow any kind of comments\. See the YAML example for comments\.

#### JSON<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Secret_and_an_RDS_DB_Instance--json"></a>

```
{
  "MyRDSSecret": {
    "Type": "AWS::SecretsManager::Secret",
    "Properties": {
      "Description": "This is a Secrets Manager secret for an RDS DB instance",
      "GenerateSecretString": {
        "SecretStringTemplate": "{\"username\": \"admin\"}",
        "GenerateStringKey": "password",
        "PasswordLength": 16,
        "ExcludeCharacters": "\"@/\\"
      }
    }
  },
  "MyRDSInstance": {
    "Type": "AWS::RDS::DBInstance",
    "Properties": {
      "AllocatedStorage": "’20’",
      "DBInstanceClass": "db.t2.micro",
      "Engine": "mysql",
      "MasterUsername": {"Fn::Join": ["", ["{{resolve:secretsmanager:",{"Ref": "MyRDSSecret"},":SecretString:username}}"] ] },
      "MasterUserPassword": {"Fn::Join": ["", ["{{resolve:secretsmanager:",{"Ref": "MyRDSSecret"},":SecretString:password}}"] ] },
      "BackupRetentionPeriod": 0,
      "DBInstanceIdentifier": "rotation-instance"
    }
  },
  "SecretRDSInstanceAttachment": {
    "Type": "AWS::SecretsManager::SecretTargetAttachment",
    "Properties": {
      "SecretId": {"Ref": "MyRDSSecret"},
      "TargetId": {"Ref": "MyRDSInstance"},
      "TargetType": "AWS::RDS::DBInstance"
    }
  }
}
```

#### YAML<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Secret_and_an_RDS_DB_Instance--yaml"></a>

```
#This is a Secret resource with a randomly generated password in its SecretString JSON.
  MyRDSSecret:
    Type: "AWS::SecretsManager::Secret"
    Properties:
      Description: "This is a Secrets Manager secret for an RDS DB instance"
      GenerateSecretString:
        SecretStringTemplate: '{"username": "admin"}'
        GenerateStringKey: "password"
        PasswordLength: 16
        ExcludeCharacters: '"@/\'

  # This is an RDS instance resource. The master username and password use dynamic references
  # to resolve values from Secrets Manager. The dynamic reference guarantees that CloudFormation
  # will not log or persist the resolved value. We use a Ref to the secret resource's logical id
  # to construct the dynamic reference, since the secret name is generated by CloudFormation.
  MyRDSInstance:
    Type: AWS::RDS::DBInstance
    Properties:
      AllocatedStorage: 20
      DBInstanceClass: db.t2.micro
      Engine: mysql
      MasterUsername: !Join ['', ['{{resolve:secretsmanager:', !Ref MyRDSSecret, ':SecretString:username}}' ]]
      MasterUserPassword: !Join ['', ['{{resolve:secretsmanager:', !Ref MyRDSSecret, ':SecretString:password}}' ]]
      BackupRetentionPeriod: 0
      DBInstanceIdentifier: 'rotation-instance'

  #This is a SecretTargetAttachment resource which updates the referenced Secret resource with properties about
  #the referenced RDS instance
  SecretRDSInstanceAttachment:
    Type: "AWS::SecretsManager::SecretTargetAttachment"
    Properties:
      SecretId: !Ref MyRDSSecret
      TargetId: !Ref MyRDSInstance
      TargetType: AWS::RDS::DBInstance
```

## See Also<a name="aws-resource-secretsmanager-secrettargetattachment--seealso"></a>
+  [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)
