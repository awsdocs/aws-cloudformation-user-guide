# AWS::SecretsManager::RotationSchedule HostedRotationLambda<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda"></a>

Creates a new Lambda rotation function based on one of the [ Secrets Manager rotation function templates](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html)\.

You must specify `Transform: AWS::SecretsManager-2020-07-23` at the beginning of the CloudFormation template\.

For Amazon RDS master user credentials, see [AWS::RDS::DBCluster MasterUserSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbcluster-masterusersecret.html)\.

## Syntax<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-secretsmanager-rotationschedule-hostedrotationlambda-syntax.json"></a>

```
{
  "[ExcludeCharacters](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-excludecharacters)" : String,
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
  [ExcludeCharacters](#cfn-secretsmanager-rotationschedule-hostedrotationlambda-excludecharacters): String
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

`ExcludeCharacters`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-excludecharacters"></a>
A string of the characters that you don't want in the password\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-kmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the secret\. If you don't specify this value, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretarn"></a>
The ARN of the secret that contains elevated credentials\. You must create the elevated secret before you can set this property\. The Lambda rotation function uses this secret for the [ Alternating users rotation strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\.  
You can specify `MasterSecretArn` or `SuperuserSecretArn` but not both\. They represent the same superuser secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterSecretKmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-mastersecretkmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the elevated secret if you use the [alternating users strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\. If you don't specify this value and you use the alternating users strategy, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.  
You can specify `MasterSecretKmsKeyArn` or `SuperuserSecretKmsKeyArn` but not both\. They represent the same superuser secret KMS key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationLambdaName`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationlambdaname"></a>
The name of the Lambda rotation function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationType`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype"></a>
The rotation template to base the rotation function on, one of the following:  
+ `MySQLSingleUser` to use the template [SecretsManagerRDSMySQLRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mysql-singleuser)\.
+ `MySQLMultiUser` to use the template [SecretsManagerRDSMySQLRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mysql-multiuser)\. 
+ `PostgreSQLSingleUser` to use the template [ SecretsManagerRDSPostgreSQLRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-postgre-singleuser)
+ `PostgreSQLMultiUser` to use the template [SecretsManagerRDSPostgreSQLRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-postgre-multiuser)\.
+ `OracleSingleUser` to use the template [SecretsManagerRDSOracleRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-oracle-singleuser)\.
+ `OracleMultiUser` to use the template [SecretsManagerRDSOracleRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-oracle-multiuser)\.
+ `MariaDBSingleUser` to use the template [SecretsManagerRDSMariaDBRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mariadb-singleuser)\.
+ `MariaDBMultiUser` to use the template [SecretsManagerRDSMariaDBRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mariadb-multiuser)\.
+ `SQLServerSingleUser` to use the template [SecretsManagerRDSSQLServerRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-sqlserver-singleuser)\.
+ `SQLServerMultiUser` to use the template [SecretsManagerRDSSQLServerRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-sqlserver-multiuser)\.
+ `RedshiftSingleUser` to use the template [SecretsManagerRedshiftRotationSingleUsr](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-redshift-singleuser)\.
+ `RedshiftMultiUser` to use the template [SecretsManagerRedshiftRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-redshift-multiuser)\.
+ `MongoDBSingleUser` to use the template [SecretsManagerMongoDBRotationSingleUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mongodb-singleuser)\.
+ `MongoDBMultiUser` to use the template [SecretsManagerMongoDBRotationMultiUser](https://docs.aws.amazon.com/secretsmanager/latest/userguide/reference_available-rotation-templates.html#sar-template-mongodb-multiuser)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuperuserSecretArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretarn"></a>
The ARN of the secret that contains elevated credentials\. You must create the superuser secret before you can set this property\. The Lambda rotation function uses this secret for the [ Alternating users rotation strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\.  
You can specify `MasterSecretArn` or `SuperuserSecretArn` but not both\. They represent the same superuser secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuperuserSecretKmsKeyArn`  <a name="cfn-secretsmanager-rotationschedule-hostedrotationlambda-superusersecretkmskeyarn"></a>
The ARN of the KMS key that Secrets Manager uses to encrypt the elevated secret if you use the [alternating users strategy](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets_strategies.html#rotating-secrets-two-users)\. If you don't specify this value and you use the alternating users strategy, then Secrets Manager uses the key `aws/secretsmanager`\. If `aws/secretsmanager` doesn't yet exist, then Secrets Manager creates it for you automatically the first time it encrypts the secret value\.  
You can specify `MasterSecretKmsKeyArn` or `SuperuserSecretKmsKeyArn` but not both\. They represent the same superuser secret KMS key\.  
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