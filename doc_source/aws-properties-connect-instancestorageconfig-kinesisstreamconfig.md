# AWS::Connect::InstanceStorageConfig KinesisStreamConfig<a name="aws-properties-connect-instancestorageconfig-kinesisstreamconfig"></a>

Configuration information of a Kinesis data stream\.

## Syntax<a name="aws-properties-connect-instancestorageconfig-kinesisstreamconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-instancestorageconfig-kinesisstreamconfig-syntax.json"></a>

```
{
  "[StreamArn](#cfn-connect-instancestorageconfig-kinesisstreamconfig-streamarn)" : String
}
```

### YAML<a name="aws-properties-connect-instancestorageconfig-kinesisstreamconfig-syntax.yaml"></a>

```
  [StreamArn](#cfn-connect-instancestorageconfig-kinesisstreamconfig-streamarn): String
```

## Properties<a name="aws-properties-connect-instancestorageconfig-kinesisstreamconfig-properties"></a>

`StreamArn`  <a name="cfn-connect-instancestorageconfig-kinesisstreamconfig-streamarn"></a>
The Amazon Resource Name \(ARN\) of the data stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)