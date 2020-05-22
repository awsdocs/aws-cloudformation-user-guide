# AWS::RDS::DBInstance ProcessorFeature<a name="aws-properties-rds-dbinstance-processorfeature"></a>

The `ProcessorFeature` property type specifies the processor features of a DB instance class status\. 

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
The name of the processor feature\. Valid names are `coreCount` and `threadsPerCore`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-rds-dbinstance-processorfeature-value"></a>
The value of a processor feature name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)