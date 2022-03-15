# AWS::SecretsManager::RotationSchedule HostedRotationLambda<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda"></a>

Specifies that you want to create a hosted Lambda rotation function\.

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
  "[SuperuserSecretArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretarn)" : String,
  "[SuperuserSecretKmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretkmskeyarn)" : String,
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
  [SuperuserSecretArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretarn): String
  [SuperuserSecretKmsKeyArn](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretkmskeyarn): String
  [VpcSecurityGroupIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsecuritygroupids): String
  [VpcSubnetIds](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsubnetids): String
```

## Properties<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-properties"></a>

`KmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-kmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the secret\. If you don't specify this value, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretarn"></a>
The ARN of the secret that contains elevated credentials\. You must create the elevated secret before you can set this property\. The Lambda rotation function uses this secret for the [ Alternating users rotation strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretKmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretkmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the elevated secret if you use the [alternating users strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\. If you don't specify this value and you use the alternating users strategy, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationLambdaName`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationlambdaname"></a>
The name of the Lambda rotation function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationType`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype"></a>
The type of rotation template to use\. For more information, see [ Secrets Manager rotation function templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html)\.  
You can specify one of the following `RotationTypes`:  
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
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuperuserSecretArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretarn"></a>
The ARN of the secret that contains elevated credentials\. You must create the superuser secret before you can set this property\. The Lambda rotation function uses this secret for the [ Alternating users rotation strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuperuserSecretKmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretkmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the elevated secret if you use the [alternating users strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\. If you don't specify this value and you use the alternating users strategy, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsecuritygroupids"></a>
A comma\-separated list of security group IDs applied to the target database\.  
The templates applies the same security groups as on the Lambda rotation function that is created as part of this stack\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSubnetIds`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-vpcsubnetids"></a>
A comma separated list of VPC subnet IDs of the target database network\. The Lambda rotation function is in the same subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)