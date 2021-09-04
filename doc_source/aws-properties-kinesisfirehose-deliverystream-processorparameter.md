# AWS::KinesisFirehose::DeliveryStream ProcessorParameter<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter"></a>

The `ProcessorParameter` property specifies a processor parameter in a data processor for an Amazon Kinesis Data Firehose delivery stream\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax.json"></a>

```
{
  "[ParameterName](#cfn-kinesisfirehose-deliverystream-processorparameter-parametername)" : String,
  "[ParameterValue](#cfn-kinesisfirehose-deliverystream-processorparameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-syntax.yaml"></a>

```
  [ParameterName](#cfn-kinesisfirehose-deliverystream-processorparameter-parametername): String
  [ParameterValue](#cfn-kinesisfirehose-deliverystream-processorparameter-parametervalue): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-processorparameter-properties"></a>

`ParameterName`  <a name="cfn-kinesisfirehose-deliverystream-processorparameter-parametername"></a>
The name of the parameter\. Currently the following default values are supported: 3 for `NumberOfRetries`, 60 for the `BufferIntervalInSeconds`, and 3 for the `BufferSizeInMBs`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BufferIntervalInSeconds | BufferSizeInMBs | Delimiter | JsonParsingEngine | LambdaArn | MetadataExtractionQuery | NumberOfRetries | RoleArn | SubRecordType`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValue`  <a name="cfn-kinesisfirehose-deliverystream-processorparameter-parametervalue"></a>
The parameter value\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `5120`  
*Pattern*: `^(?!\s*$).+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)