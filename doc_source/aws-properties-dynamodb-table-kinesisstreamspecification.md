# AWS::DynamoDB::Table KinesisStreamSpecification<a name="aws-properties-dynamodb-table-kinesisstreamspecification"></a>

The Kinesis Data Streams configuration for the specified table\.

## Syntax<a name="aws-properties-dynamodb-table-kinesisstreamspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-kinesisstreamspecification-syntax.json"></a>

```
{
  "[StreamArn](#cfn-dynamodb-table-kinesisstreamspecification-streamarn)" : String
}
```

### YAML<a name="aws-properties-dynamodb-table-kinesisstreamspecification-syntax.yaml"></a>

```
  [StreamArn](#cfn-dynamodb-table-kinesisstreamspecification-streamarn): String
```

## Properties<a name="aws-properties-dynamodb-table-kinesisstreamspecification-properties"></a>

`StreamArn`  <a name="cfn-dynamodb-table-kinesisstreamspecification-streamarn"></a>
The ARN for a specific Kinesis data stream\.  
Length Constraints: Minimum length of 37\. Maximum length of 1024\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `37`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dynamodb-table-kinesisstreamspecification--seealso"></a>
+ [Change Data Capture for Kinesis Data Streams with DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/kds.html)

