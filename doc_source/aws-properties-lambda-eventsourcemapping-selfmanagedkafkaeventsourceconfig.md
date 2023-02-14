# AWS::Lambda::EventSourceMapping SelfManagedKafkaEventSourceConfig<a name="aws-properties-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig"></a>

Specific configuration settings for a self\-managed Apache Kafka event source\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-syntax.json"></a>

```
{
  "[ConsumerGroupId](#cfn-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-consumergroupid)" : String
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-syntax.yaml"></a>

```
  [ConsumerGroupId](#cfn-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-consumergroupid): String
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-properties"></a>

`ConsumerGroupId`  <a name="cfn-lambda-eventsourcemapping-selfmanagedkafkaeventsourceconfig-consumergroupid"></a>
The identifier for the Kafka consumer group to join\. The consumer group ID must be unique among all your Kafka event sources\. After creating a Kafka event source mapping with the consumer group ID specified, you cannot update this value\. For more information, see [Customizable consumer group ID](https://docs.aws.amazon.com/lambda/latest/dg/with-msk.html#services-msk-consumer-group-id)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `[a-zA-Z0-9-\/*:_+=.@-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)