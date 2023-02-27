# AWS::KafkaConnect::Connector WorkerConfiguration<a name="aws-properties-kafkaconnect-connector-workerconfiguration"></a>

The configuration of the workers, which are the processes that run the connector logic\.

## Syntax<a name="aws-properties-kafkaconnect-connector-workerconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-workerconfiguration-syntax.json"></a>

```
{
  "[Revision](#cfn-kafkaconnect-connector-workerconfiguration-revision)" : Integer,
  "[WorkerConfigurationArn](#cfn-kafkaconnect-connector-workerconfiguration-workerconfigurationarn)" : String
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-workerconfiguration-syntax.yaml"></a>

```
  [Revision](#cfn-kafkaconnect-connector-workerconfiguration-revision): Integer
  [WorkerConfigurationArn](#cfn-kafkaconnect-connector-workerconfiguration-workerconfigurationarn): String
```

## Properties<a name="aws-properties-kafkaconnect-connector-workerconfiguration-properties"></a>

`Revision`  <a name="cfn-kafkaconnect-connector-workerconfiguration-revision"></a>
The revision of the worker configuration\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WorkerConfigurationArn`  <a name="cfn-kafkaconnect-connector-workerconfiguration-workerconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the worker configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)