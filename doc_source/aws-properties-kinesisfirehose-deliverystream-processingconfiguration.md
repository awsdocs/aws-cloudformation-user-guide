# Amazon Kinesis Firehose DeliveryStream ProcessingConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration"></a>

The `ProcessingConfiguration` property configures data processing for an Amazon Kinesis Firehose delivery stream\.

`ProcessingConfiguration` is a property of the [Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md), [Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md), and [Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md) property types\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processingconfiguration-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processingconfiguration-processors)" : [ Processor, ... ]
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processingconfiguration-enabled): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processingconfiguration-processors): 
    - Processor
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processingconfiguration-properties"></a>

`Enabled`  
Indicates whether data processing is enabled \(`true`\) or disabled \(`false`\)\.  
 *Required*: Yes  
*Type*: Boolean  
 *Update requires*: No interruption 

`Processors`  
The data processors\.  
 *Required*: Yes  
 *Type*: List of [Kinesis Firehose DeliveryStream Processor](aws-properties-kinesisfirehose-deliverystream-processor.md)  
 *Update requires*: No interruption 