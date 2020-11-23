# AWS::KinesisFirehose::DeliveryStream ProcessingConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration"></a>

The `ProcessingConfiguration` property configures data processing for an Amazon Kinesis Data Firehose delivery stream\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-kinesisfirehose-deliverystream-processingconfiguration-enabled)" : Boolean,
  "[Processors](#cfn-kinesisfirehose-deliverystream-processingconfiguration-processors)" : [ Processor, ... ]
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-kinesisfirehose-deliverystream-processingconfiguration-enabled): Boolean
  [Processors](#cfn-kinesisfirehose-deliverystream-processingconfiguration-processors): 
    - Processor
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-properties"></a>

`Enabled`  <a name="cfn-kinesisfirehose-deliverystream-processingconfiguration-enabled"></a>
Indicates whether data processing is enabled \(true\) or disabled \(false\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Processors`  <a name="cfn-kinesisfirehose-deliverystream-processingconfiguration-processors"></a>
The data processors\.  
*Required*: No  
*Type*: List of [Processor](aws-properties-kinesisfirehose-deliverystream-processor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)