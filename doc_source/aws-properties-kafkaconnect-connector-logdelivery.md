# AWS::KafkaConnect::Connector LogDelivery<a name="aws-properties-kafkaconnect-connector-logdelivery"></a>

Details about log delivery\.

## Syntax<a name="aws-properties-kafkaconnect-connector-logdelivery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-logdelivery-syntax.json"></a>

```
{
  "[WorkerLogDelivery](#cfn-kafkaconnect-connector-logdelivery-workerlogdelivery)" : WorkerLogDelivery
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-logdelivery-syntax.yaml"></a>

```
  [WorkerLogDelivery](#cfn-kafkaconnect-connector-logdelivery-workerlogdelivery): 
    WorkerLogDelivery
```

## Properties<a name="aws-properties-kafkaconnect-connector-logdelivery-properties"></a>

`WorkerLogDelivery`  <a name="cfn-kafkaconnect-connector-logdelivery-workerlogdelivery"></a>
The workers can send worker logs to different destination types\. This configuration specifies the details of these destinations\.  
*Required*: Yes  
*Type*: [WorkerLogDelivery](aws-properties-kafkaconnect-connector-workerlogdelivery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)