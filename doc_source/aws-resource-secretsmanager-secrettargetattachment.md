# AWS::SecretsManager::SecretTargetAttachment<a name="aws-resource-secretsmanager-secrettargetattachment"></a>

The `AWS::SecretsManager::SecretTargetAttachment` resource completes the final link between a Secrets Manager secret and the associated database\. This is required because each has a dependency on the other\. No matter which one you create first, the other doesn't exist yet\. To resolve this, you must create the resources in the following order:

1. Define the secret without referencing the service or database\. You can't reference the service or database because it doesn't exist yet\. The secret must contain a user name and password\.

1. Next, define the service or database\. Include the reference to the secret to use stored credentials to define the database admin user and password\.

1. Finally, define a `SecretTargetAttachment` resource type to finish configuring the secret with the required database engine type and the connection details of the service or database\. The rotation function requires the details, if you attach one later by defining a [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html) resource type\.

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
The ARN or name of the secret\. To reference a secret also created in this template, use the see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function with the secret's logical ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetId`  <a name="cfn-secretsmanager-secrettargetattachment-targetid"></a>
The ID of the database or cluster\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-secretsmanager-secrettargetattachment-targettype"></a>
A string that defines the type of service or database associated with the secret\. This value instructs Secrets Manager how to update the secret with the details of the service or database\. This value must be one of the following:   
+ AWS::RDS::DBInstance
+ AWS::RDS::DBCluster
+ AWS::Redshift::Cluster
+ AWS::DocDB::DBInstance
+ AWS::DocDB::DBCluster
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-secretsmanager-secrettargetattachment-return-values"></a>

### Ref<a name="aws-resource-secretsmanager-secrettargetattachment-return-values-ref"></a>

When you pass the logical ID of an `AWS::SecretsManager::SecretTargetAttachment` resource to the intrinsic `Ref` function, the function returns the ARN of the secret, such as:

`arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`

You can use the ARN to reference a secret you created in one part of the stack template from within the definition of another resource from a different part of the same template\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-secretsmanager-secrettargetattachment--examples"></a>

The following examples create a secret, and then creates an AWS resource as defined by the TargetType using the credentials found in the secret for the new AWS resource user and password\. Finally, the code updates the secret with the connection details of the AWS resource by defining the `SecretTargetAttachment` object\.

### Creating a secret for a RDS database instance<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_secret_for_a_RDS_database_instance"></a>

#### JSON<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_secret_for_a_RDS_database_instance--json"></a>

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

#### YAML<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_secret_for_a_RDS_database_instance--yaml"></a>

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

### Creating a secret for a Redshift cluster<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_secret_for_a_Redshift_cluster"></a>

#### JSON<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_secret_for_a_Redshift_cluster--json"></a>

```
{
   "AWSTemplateFormatVersion":"2010-09-09",
   "Resources":{
      "MyRedshiftSecret":{
         "Type":"AWS::SecretsManager::Secret",
         "Properties":{
            "Description":"This is a Secrets Manager secret for a Redshift cluster",
            "GenerateSecretString":{
               "SecretStringTemplate":"{\"username\": \"admin\"}",
               "GenerateStringKey":"password",
               "PasswordLength":16,
               "ExcludeCharacters":"\"'@/\\"
            }
         }
      },
      "MyRedshiftCluster":{
         "Type":"AWS::Redshift::Cluster",
         "Properties":{
            "DBName":"myjsondb",
            "MasterUsername":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"
            },
            "MasterUserPassword":{
               "Fn::Sub":"{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"
            },
            "NodeType":"ds2.xlarge",
            "ClusterType":"single-node"
         }
      },
      "SecretRedshiftAttachment":{
         "Type":"AWS::SecretsManager::SecretTargetAttachment",
         "Properties":{
            "SecretId":{
               "Ref":"MyRedshiftSecret"
            },
            "TargetId":{
               "Ref":"MyRedshiftCluster"
            },
            "TargetType":"AWS::Redshift::Cluster"
         }
      }
   }
}
```

### Creating a Redshift cluster using YAML<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Redshift_cluster_using_YAML"></a>

#### YAML<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Redshift_cluster_using_YAML--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyRedshiftSecret:
    Type: AWS::SecretsManager::Secret
    Properties:
      Description: This is a Secrets Manager secret for a Redshift cluster
      GenerateSecretString:
        SecretStringTemplate: '{"username": "admin"}'
        GenerateStringKey: password
        PasswordLength: 16
        ExcludeCharacters: "\"'@/\\"
  MyRedshiftCluster:
    Type: AWS::Redshift::Cluster
    Properties:
      DBName: myjsondb
      MasterUsername:
        Fn::Sub: "{{resolve:secretsmanager:${MyRedshiftSecret}::username}}"
      MasterUserPassword:
        Fn::Sub: "{{resolve:secretsmanager:${MyRedshiftSecret}::password}}"
      NodeType: ds2.xlarge
      ClusterType: single-node
  SecretRedshiftAttachment:
    Type: AWS::SecretsManager::SecretTargetAttachment
    Properties:
      SecretId:
        Ref: MyRedshiftSecret
      TargetId:
        Ref: MyRedshiftCluster
      TargetType: AWS::Redshift::Cluster
```

## See also<a name="aws-resource-secretsmanager-secrettargetattachment--seealso"></a>
+  [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)
+  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)
+  [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)