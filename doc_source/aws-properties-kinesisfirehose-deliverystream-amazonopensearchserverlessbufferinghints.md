# AWS::KinesisFirehose::DeliveryStream AmazonOpenSearchServerlessBufferingHints<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints"></a>

Describes the buffering to perform before delivering data to the Serverless offering for Amazon OpenSearch Service destination\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-syntax.json"></a>

```
{
  "[IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-intervalinseconds)" : Integer,
  "[SizeInMBs](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-sizeinmbs)" : Integer
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-syntax.yaml"></a>

```
  [IntervalInSeconds](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-intervalinseconds): Integer
  [SizeInMBs](#cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-sizeinmbs): Integer
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-properties"></a>

`IntervalInSeconds`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-intervalinseconds"></a>
Buffer incoming data for the specified period of time, in seconds, before delivering it to the destination\. The default value is 300 \(5 minutes\)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `900`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeInMBs`  <a name="cfn-kinesisfirehose-deliverystream-amazonopensearchserverlessbufferinghints-sizeinmbs"></a>
Buffer incoming data to the specified size, in MBs, before delivering it to the destination\. The default value is 5\.   
We recommend setting this parameter to a value greater than the amount of data you typically ingest into the delivery stream in 10 seconds\. For example, if you typically ingest data at 1 MB/sec, the value should be 10 MB or higher\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)