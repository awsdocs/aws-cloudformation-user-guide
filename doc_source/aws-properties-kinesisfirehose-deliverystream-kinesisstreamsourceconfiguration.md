# Amazon Kinesis Data Firehose DeliveryStream KinesisStreamSourceConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration"></a>

<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-description"></a> The `KinesisStreamSourceConfiguration` property type specifies the stream and role Amazon Resource Names \(ARNs\) for a Kinesis stream used as the source for a delivery stream\.

<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-inheritance"></a> `KinesisStreamSourceConfiguration` is a property of the [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) resource\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-syntax.json"></a>

```
{
  "[KinesisStreamARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn)" : String
  "[RoleARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration.yaml"></a>

```
[KinesisStreamARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn): String
[RoleARN](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-properties"></a>

`KinesisStreamARN`  <a name="cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-kinesisstreamarn"></a>
The Amazon Resource Name \(ARN\) of the source Kinesis stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RoleARN`  <a name="cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that provides access to the source Kinesis stream\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 