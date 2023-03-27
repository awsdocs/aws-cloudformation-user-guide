# AWS::DynamoDB::GlobalTable KinesisStreamSpecification<a name="aws-properties-dynamodb-globaltable-kinesisstreamspecification"></a>

The Kinesis Data Streams configuration for the specified global table replica\.

## Syntax<a name="aws-properties-dynamodb-globaltable-kinesisstreamspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-kinesisstreamspecification-syntax.json"></a>

```
{
  "[StreamArn](#cfn-dynamodb-globaltable-kinesisstreamspecification-streamarn)" : String
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-kinesisstreamspecification-syntax.yaml"></a>

```
  [StreamArn](#cfn-dynamodb-globaltable-kinesisstreamspecification-streamarn): String
```

## Properties<a name="aws-properties-dynamodb-globaltable-kinesisstreamspecification-properties"></a>

`StreamArn`  <a name="cfn-dynamodb-globaltable-kinesisstreamspecification-streamarn"></a>
The ARN for a specific Kinesis data stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `37`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)