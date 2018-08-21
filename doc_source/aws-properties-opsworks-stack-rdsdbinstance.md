# AWS OpsWorks Stack RdsDbInstance<a name="aws-properties-opsworks-stack-rdsdbinstance"></a>

`RdsDbInstance` is a property of the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) resource that registers an Amazon Relational Database Service \(Amazon RDS\) DB instance with an AWS OpsWorks stack\.

## Syntax<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax"></a>

### JSON<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax.json"></a>

```
{
  "[DbPassword](#cfn-opsworks-stack-rdsdbinstance-dbpassword)" : String,
  "[DbUser](#cfn-opsworks-stack-rdsdbinstance-dbuser)" : String,
  "[RdsDbInstanceArn](#cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax.yaml"></a>

```
[DbPassword](#cfn-opsworks-stack-rdsdbinstance-dbpassword): String
[DbUser](#cfn-opsworks-stack-rdsdbinstance-dbuser): String
[RdsDbInstanceArn](#cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn): String
```

## Properties<a name="aws-properties-opsworks-stack-rdsdbinstance-properties"></a>

`DbPassword`  <a name="cfn-opsworks-stack-rdsdbinstance-dbpassword"></a>
The password of the registered database\.  
*Required*: Yes  
*Type*: String

`DbUser`  <a name="cfn-opsworks-stack-rdsdbinstance-dbuser"></a>
The master user name of the registered database\.  
*Required*: Yes  
*Type*: String

`RdsDbInstanceArn`  <a name="cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn"></a>
The Amazon Resource Name \(ARN\) of the Amazon RDS DB instance to register with the AWS OpsWorks stack\.  
*Required*: Yes  
*Type*: String