# AWS::KinesisFirehose::DeliveryStream Processor<a name="aws-properties-kinesisfirehose-deliverystream-processor"></a>

The `Processor` property specifies a data processor for an Amazon Kinesis Data Firehose delivery stream\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax.json"></a>

```
{
  "[Parameters](#cfn-kinesisfirehose-deliverystream-processor-parameters)" : [ ProcessorParameter, ... ],
  "[Type](#cfn-kinesisfirehose-deliverystream-processor-type)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processor-syntax.yaml"></a>

```
  [Parameters](#cfn-kinesisfirehose-deliverystream-processor-parameters): 
    - ProcessorParameter
  [Type](#cfn-kinesisfirehose-deliverystream-processor-type): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processor-properties"></a>

`Parameters`  <a name="cfn-kinesisfirehose-deliverystream-processor-parameters"></a>
The processor parameters\.  
*Required*: No  
*Type*: List of [ProcessorParameter](aws-properties-kinesisfirehose-deliverystream-processorparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-kinesisfirehose-deliverystream-processor-type"></a>
The type of processor\. Valid values: `Lambda`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `Lambda`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)