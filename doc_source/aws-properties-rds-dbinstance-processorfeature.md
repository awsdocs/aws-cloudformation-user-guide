# Amazon RDS DBInstance ProcessorFeature<a name="aws-properties-rds-dbinstance-processorfeature"></a>

<a name="aws-properties-rds-dbinstance-processorfeature-description"></a>The `ProcessorFeature` property type specifies the processor features of a DB instance class status\.

<a name="aws-properties-rds-dbinstance-processorfeature-inheritance"></a> `ProcessorFeature` is a property of the [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md) resource type\.

## Syntax<a name="aws-properties-rds-dbinstance-processorfeature-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-dbinstance-processorfeature-syntax.json"></a>

```
{
  "[Name](#cfn-rds-dbinstance-processorfeature-name)" : String,
  "[Value](#cfn-rds-dbinstance-processorfeature-value)" : String
}
```

### YAML<a name="aws-properties-rds-dbinstance-processorfeature-syntax.yaml"></a>

```
[Name](#cfn-rds-dbinstance-processorfeature-name): String
[Value](#cfn-rds-dbinstance-processorfeature-value): String
```

## Properties<a name="aws-properties-rds-dbinstance-processorfeature-properties"></a>

`Name`  <a name="cfn-rds-dbinstance-processorfeature-name"></a>
The name of the processor feature\. Valid values are `coreCount` to specify the number of CPU cores and `threadsPerCore` to specify the number of threads per core\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-rds-dbinstance-processorfeature-value"></a>
The value of a processor feature name\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-rds-dbinstance-processorfeature-seealso"></a>
+ [ProcessorFeature](https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ProcessorFeature.html) in the *Amazon RDS API Reference*