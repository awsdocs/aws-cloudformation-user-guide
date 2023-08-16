# AWS::IVSChat::LoggingConfiguration FirehoseDestinationConfiguration<a name="aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration"></a>

The FirehoseDestinationConfiguration property type specifies a Kinesis Firehose location where chat logs will be stored\.

## Syntax<a name="aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration-syntax.json"></a>

```
{
  "[DeliveryStreamName](#cfn-ivschat-loggingconfiguration-firehosedestinationconfiguration-deliverystreamname)" : String
}
```

### YAML<a name="aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration-syntax.yaml"></a>

```
  [DeliveryStreamName](#cfn-ivschat-loggingconfiguration-firehosedestinationconfiguration-deliverystreamname): String
```

## Properties<a name="aws-properties-ivschat-loggingconfiguration-firehosedestinationconfiguration-properties"></a>

`DeliveryStreamName`  <a name="cfn-ivschat-loggingconfiguration-firehosedestinationconfiguration-deliverystreamname"></a>
Name of the Amazon Kinesis Firehose delivery stream where chat activity will be logged\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9_.-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)