# AWS OpsWorks Stack RdsDbInstance<a name="aws-properties-opsworks-stack-rdsdbinstance"></a>

`RdsDbInstance` is a property of the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) resource that registers an Amazon Relational Database Service \(Amazon RDS\) DB instance with an AWS OpsWorks stack\.

## Syntax<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax"></a>

### JSON<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-dbpassword)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-dbuser)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-dbpassword): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-dbuser): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn): String
```

## Properties<a name="aws-properties-opsworks-stack-rdsdbinstance-properties"></a>

`DbPassword`  
The password of the registered database\.  
*Required: *Yes  
*Type*: String

`DbUser`  
The master user name of the registered database\.  
*Required: *Yes  
*Type*: String

`RdsDbInstanceArn`  
The Amazon Resource Name \(ARN\) of the Amazon RDS DB instance to register with the AWS OpsWorks stack\.  
*Required: *Yes  
*Type*: String