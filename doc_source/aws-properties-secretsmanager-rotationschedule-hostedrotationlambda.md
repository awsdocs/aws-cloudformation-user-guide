# AWS::SecretsManager::RotationSchedule HostedRotationLambda<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda"></a>

Specifies that you want to create a hosted rotation lambda\.

To use these values, you must specify `Transform: AWS::SecretsManager-2020-07-23` at the beginning of the CloudFormation template\.

## Syntax<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-syntax.json"></a>

```
{
  "[KmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-kmskeyarn)" : String,
  "[MasterSecretArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretarn)" : String,
  "[MasterSecretKmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretkmskeyarn)" : String,
  "[RotationLambdaName](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationlambdaname)" : String,
  "[RotationType](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype)" : String,
  "[VpcSecurityGroupIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsecuritygroupids)" : String,
  "[VpcSubnetIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsubnetids)" : String
}
```

### YAML<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-syntax.yaml"></a>

```
  [KmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-kmskeyarn): String
  [MasterSecretArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretarn): String
  [MasterSecretKmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretkmskeyarn): String
  [RotationLambdaName](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationlambdaname): String
  [RotationType](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype): String
  [VpcSecurityGroupIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsecuritygroupids): String
  [VpcSubnetIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsubnetids): String
```

## Properties<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-properties"></a>

`KmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-kmskeyarn"></a>
Specifies the ARN of the KMS key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretarn"></a>
Specifies the ARN of the MasterSecret that contains a privileged user’s credentials\. The Lambda uses this secret to rotate the current secret\. See [Permissions Required to Automatically Rotate Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets-required-permissions.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretKmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretkmskeyarn"></a>
Specifies the ARN of the KMS key used to encrypt the master secret\. You only need this property if you use a master secret to rotate the current secret, and you encrypt the master secret with a custom CMK\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationLambdaName`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationlambdaname"></a>
Specifies the name of the Lambda created to rotate your secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationType`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype"></a>
Specifies the type of RotationSchedule used by Secrets Manager\. You can specify one of the following `RotationTypes`:  
+ MySQLSingleUser
+ MySQLMultiUser
+ PostgreSQLSingleUser
+ PostgreSQLMultiUser
+ OracleSingleUser
+ OracleMultiUser
+ MariaDBSingleUser
+ MariaDBMultiUser
+ SQLServerSingleUser
+ SQLServerMultiUser
+ RedshiftSingleUser
+ RedshiftMultiUser
+ MongoDBSingleUser
+ MongoDBMultiUser
The rotation type uses a combination of the target database and the rotation strategy\. For more information on single user and multi user rotation, see [ Rotating Secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html) in the AWS Secrets Manager User’s Guide\.\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsecuritygroupids"></a>
Specifies the comma\-separated list of security group IDs applied on the target with a secret in rotation\.  
The templates applies the same security groups as on the rotation Lambda created as part of this stack  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSubnetIds`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsubnetids"></a>
Specifies the comma separated list of VPC subnet IDs of the target database network\. The rotation Lambda resides in the same subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)