# AWS::RDS::DBInstance MasterUserSecret<a name="aws-properties-rds-dbinstance-masterusersecret"></a>

Contains the secret managed by RDS in AWS Secrets Manager for the master user password\.

For more information, see [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-secrets-manager.html) in the *Amazon RDS User Guide* and [Password management with AWS Secrets Manager](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-secrets-manager.html) in the *Amazon Aurora User Guide\.* 

## Syntax<a name="aws-properties-rds-dbinstance-masterusersecret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbinstance-masterusersecret-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-rds-dbinstance-masterusersecret-kmskeyid)" : String,
  "[SecretArn](#cfn-rds-dbinstance-masterusersecret-secretarn)" : String
}
```

### YAML<a name="aws-properties-rds-dbinstance-masterusersecret-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-rds-dbinstance-masterusersecret-kmskeyid): String
  [SecretArn](#cfn-rds-dbinstance-masterusersecret-secretarn): String
```

## Properties<a name="aws-properties-rds-dbinstance-masterusersecret-properties"></a>

`KmsKeyId`  <a name="cfn-rds-dbinstance-masterusersecret-kmskeyid"></a>
The AWS KMS key identifier that is used to encrypt the secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-rds-dbinstance-masterusersecret-secretarn"></a>
The Amazon Resource Name \(ARN\) of the secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)