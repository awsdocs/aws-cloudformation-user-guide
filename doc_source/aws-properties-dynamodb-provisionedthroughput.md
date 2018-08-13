# Amazon DynamoDB Table ProvisionedThroughput<a name="aws-properties-dynamodb-provisionedthroughput"></a>

Describes a set of provisioned throughput values for an [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource\. DynamoDB uses these capacity units to allocate sufficient resources to provide the requested throughput\.

For a complete discussion of DynamoDB provisioned throughput values, see [Specifying Read and Write Requirements](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.html#ProvisionedThroughput) in the *DynamoDB Developer Guide*\.

## Syntax<a name="w3ab2c21c14d627b7"></a>

### JSON<a name="aws-properties-dynamodb-provisionedthroughput-syntax.json"></a>

```
{
   "[ReadCapacityUnits](#cfn-dynamodb-provisionedthroughput-readcapacityunits)" : Number,
   "[WriteCapacityUnits](#cfn-dynamodb-provisionedthroughput-writecapacityunits)" : Number
}
```

### YAML<a name="aws-properties-dynamodb-provisionedthroughput-syntax.yaml"></a>

```
[ReadCapacityUnits](#cfn-dynamodb-provisionedthroughput-readcapacityunits): Number
[WriteCapacityUnits](#cfn-dynamodb-provisionedthroughput-writecapacityunits): Number
```

## Parameters<a name="w3ab2c21c14d627b9"></a>

`ReadCapacityUnits`  <a name="cfn-dynamodb-provisionedthroughput-readcapacityunits"></a>
Sets the desired minimum number of consistent reads of items \(up to 1KB in size\) per second for the specified table before Amazon DynamoDB balances the load\.  
*Required*: Yes  
*Type*: Number

`WriteCapacityUnits`  <a name="cfn-dynamodb-provisionedthroughput-writecapacityunits"></a>
Sets the desired minimum number of consistent writes of items \(up to 1KB in size\) per second for the specified table before Amazon DynamoDB balances the load\.  
*Required*: Yes  
*Type*: Number

**Note**  
For detailed information about the limits of provisioned throughput values in DynamoDB, see [Limits in Amazon DynamoDB](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html) in the *DynamoDB Developer Guide*\.