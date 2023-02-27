# AWS::SecretsManager::SecretTargetAttachment<a name="aws-resource-secretsmanager-secrettargetattachment"></a>

The `AWS::SecretsManager::SecretTargetAttachment` resource completes the final link between a Secrets Manager secret and the associated database by adding the database connection information to the secret JSON\. If you want to turn on automatic rotation for a database credential secret, the secret must contain the database connection information\. For more information, see [JSON structure of Secrets Manager database credential secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_secret_json_structure.html)\. 

For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.

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

### Creating a Redshift cluster<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Redshift_cluster"></a>

The following example creates a secret and an Amazon Redshift resource as defined by the `TargetType` using the credentials found in the secret as the new Amazon Redshift user and password\. Then the code updates the secret with the connection details of the AWS resource by defining the `SecretTargetAttachment` object\.

#### YAML<a name="aws-resource-secretsmanager-secrettargetattachment--examples--Creating_a_Redshift_cluster--yaml"></a>

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