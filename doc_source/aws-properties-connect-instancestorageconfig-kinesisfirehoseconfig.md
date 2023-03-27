# AWS::Connect::InstanceStorageConfig KinesisFirehoseConfig<a name="aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig"></a>

Configuration information of a Kinesis Data Firehose delivery stream\.

## Syntax<a name="aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig-syntax.json"></a>

```
{
  "[FirehoseArn](#cfn-connect-instancestorageconfig-kinesisfirehoseconfig-firehosearn)" : String
}
```

### YAML<a name="aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig-syntax.yaml"></a>

```
  [FirehoseArn](#cfn-connect-instancestorageconfig-kinesisfirehoseconfig-firehosearn): String
```

## Properties<a name="aws-properties-connect-instancestorageconfig-kinesisfirehoseconfig-properties"></a>

`FirehoseArn`  <a name="cfn-connect-instancestorageconfig-kinesisfirehoseconfig-firehosearn"></a>
The Amazon Resource Name \(ARN\) of the delivery stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)