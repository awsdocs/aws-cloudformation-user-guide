# AWS::DynamoDB::Table ProvisionedThroughput<a name="aws-properties-dynamodb-provisionedthroughput"></a>

Throughput for the specified table, which consists of values for `ReadCapacityUnits` and `WriteCapacityUnits`\. For more information about the contents of a provisioned throughput structure, see [Amazon DynamoDB Table ProvisionedThroughput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dynamodb-provisionedthroughput.html)\. 

## Syntax<a name="aws-properties-dynamodb-provisionedthroughput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-provisionedthroughput-syntax.json"></a>

```
{
  "[ReadCapacityUnits](#cfn-dynamodb-provisionedthroughput-readcapacityunits)" : Long,
  "[WriteCapacityUnits](#cfn-dynamodb-provisionedthroughput-writecapacityunits)" : Long
}
```

### YAML<a name="aws-properties-dynamodb-provisionedthroughput-syntax.yaml"></a>

```
  [ReadCapacityUnits](#cfn-dynamodb-provisionedthroughput-readcapacityunits): Long
  [WriteCapacityUnits](#cfn-dynamodb-provisionedthroughput-writecapacityunits): Long
```

## Properties<a name="aws-properties-dynamodb-provisionedthroughput-properties"></a>

`ReadCapacityUnits`  <a name="cfn-dynamodb-provisionedthroughput-readcapacityunits"></a>
The maximum number of strongly consistent reads consumed per second before DynamoDB returns a `ThrottlingException`\. For more information, see [Specifying Read and Write Requirements](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html#ProvisionedThroughput) in the *Amazon DynamoDB Developer Guide*\.  
If read/write capacity mode is `PAY_PER_REQUEST` the value is set to 0\.  
*Required*: Yes  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteCapacityUnits`  <a name="cfn-dynamodb-provisionedthroughput-writecapacityunits"></a>
The maximum number of writes consumed per second before DynamoDB returns a `ThrottlingException`\. For more information, see [Specifying Read and Write Requirements](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html#ProvisionedThroughput) in the *Amazon DynamoDB Developer Guide*\.  
If read/write capacity mode is `PAY_PER_REQUEST` the value is set to 0\.  
*Required*: Yes  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)