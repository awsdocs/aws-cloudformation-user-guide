# AWS::DynamoDB::Table ProvisionedThroughput<a name="aws-properties-dynamodb-table-provisionedthroughput"></a>

Throughput for the specified table, which consists of values for `ReadCapacityUnits` and `WriteCapacityUnits`\. For more information about the contents of a provisioned throughput structure, see [Amazon DynamoDB Table ProvisionedThroughput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dynamodb-provisionedthroughput.html)\. 

## Syntax<a name="aws-properties-dynamodb-table-provisionedthroughput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-provisionedthroughput-syntax.json"></a>

```
{
  "[ReadCapacityUnits](#cfn-dynamodb-table-provisionedthroughput-readcapacityunits)" : Integer,
  "[WriteCapacityUnits](#cfn-dynamodb-table-provisionedthroughput-writecapacityunits)" : Integer
}
```

### YAML<a name="aws-properties-dynamodb-table-provisionedthroughput-syntax.yaml"></a>

```
  [ReadCapacityUnits](#cfn-dynamodb-table-provisionedthroughput-readcapacityunits): Integer
  [WriteCapacityUnits](#cfn-dynamodb-table-provisionedthroughput-writecapacityunits): Integer
```

## Properties<a name="aws-properties-dynamodb-table-provisionedthroughput-properties"></a>

`ReadCapacityUnits`  <a name="cfn-dynamodb-table-provisionedthroughput-readcapacityunits"></a>
The maximum number of strongly consistent reads consumed per second before DynamoDB returns a `ThrottlingException`\. For more information, see [Specifying Read and Write Requirements](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html#ProvisionedThroughput) in the *Amazon DynamoDB Developer Guide*\.  
If read/write capacity mode is `PAY_PER_REQUEST` the value is set to 0\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteCapacityUnits`  <a name="cfn-dynamodb-table-provisionedthroughput-writecapacityunits"></a>
The maximum number of writes consumed per second before DynamoDB returns a `ThrottlingException`\. For more information, see [Specifying Read and Write Requirements](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html#ProvisionedThroughput) in the *Amazon DynamoDB Developer Guide*\.  
If read/write capacity mode is `PAY_PER_REQUEST` the value is set to 0\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)