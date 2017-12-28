# Amazon Kinesis Firehose DeliveryStream ProcessorParameter<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter"></a>

The `ProcessorParameter` property specifies a processor parameter in a data processor for an Amazon Kinesis Firehose delivery stream\.

`ProcessorParameter` is a property of the [Amazon Kinesis Firehose DeliveryStream Processor](aws-properties-kinesisfirehose-deliverystream-processor.md) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processorparameter-parametername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processorparameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processorparameter-parametername): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-kinesisfirehose-deliverystream-processorparameter-parametervalue): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-properties"></a>

For more information about each property, including constraints and valid values, see [ProcessorParameter](http://docs.aws.amazon.com/firehose/latest/APIReference/API_ProcessorParameter.html) in the *Amazon Kinesis Firehose API Reference*\.

`ParameterName`  
The name of the parameter\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 

`ParameterValue`  
The parameter value\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: No interruption 