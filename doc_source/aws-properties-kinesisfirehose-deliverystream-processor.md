# Amazon Kinesis Firehose DeliveryStream Processor<a name="aws-properties-kinesisfirehose-deliverystream-processor"></a>

The `Processor` property specifies a data processor for an Amazon Kinesis Firehose delivery stream\. `Processor` is a property of the [Amazon Kinesis Firehose DeliveryStream ProcessingConfiguration](aws-properties-kinesisfirehose-deliverystream-processingconfiguration.md) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax.json"></a>

```
{
  "[Parameters](#cfn-kinesisfirehose-deliverystream-processor-parameters)" : [ [*ProcessorParameter*](aws-properties-kinesisfirehose-deliverystream-processorparameter.md), ... ],
  "[Type](#cfn-kinesisfirehose-deliverystream-processor-type)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax.yaml"></a>

```
  [Parameters](#cfn-kinesisfirehose-deliverystream-processor-parameters): 
    - [*ProcessorParameter*](aws-properties-kinesisfirehose-deliverystream-processorparameter.md) 
  [Type](#cfn-kinesisfirehose-deliverystream-processor-type): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processor-properties"></a>

`Parameters`  <a name="cfn-kinesisfirehose-deliverystream-processor-parameters"></a>
The processor parameters\.  
 *Required*: Yes  
 *Type*: List of [Amazon Kinesis Firehose DeliveryStream ProcessorParameter](aws-properties-kinesisfirehose-deliverystream-processorparameter.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Type`  <a name="cfn-kinesisfirehose-deliverystream-processor-type"></a>
The type of processor\. Valid values: `Lambda`\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 