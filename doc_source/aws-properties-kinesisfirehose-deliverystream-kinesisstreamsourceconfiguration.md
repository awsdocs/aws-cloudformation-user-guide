# AWS::KinesisFirehose::DeliveryStream KinesisStreamSourceConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration"></a>

The `KinesisStreamSourceConfiguration` property type specifies the stream and role Amazon Resource Names \(ARNs\) for a Kinesis stream used as the source for a delivery stream\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-syntax.json"></a>

```
{
  "[KinesisStreamARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn)" : String,
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-syntax.yaml"></a>

```
  [KinesisStreamARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn): String
  [RoleARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-properties"></a>

`KinesisStreamARN`  <a name="cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn"></a>
The ARN of the source Kinesis data stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn"></a>
The ARN of the role that provides access to the source Kinesis data stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)