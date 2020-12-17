# AWS::OpsWorks::Stack RdsDbInstance<a name="aws-properties-opsworks-stack-rdsdbinstance"></a>

Describes an Amazon RDS instance\.

## Syntax<a name="aws-properties-opsworks-stack-rdsdbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
AWS OpsWorks Stacks returns `*****FILTERED*****` instead of the actual value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DbUser`  <a name="cfn-opsworks-stack-rdsdbinstance-dbuser"></a>
The master user name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RdsDbInstanceArn`  <a name="cfn-opsworks-stack-rdsdbinstance-rdsdbinstancearn"></a>
The instance's ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)