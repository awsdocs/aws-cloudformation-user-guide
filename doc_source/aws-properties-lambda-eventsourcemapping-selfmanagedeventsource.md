# AWS::Lambda::EventSourceMapping SelfManagedEventSource<a name="aws-properties-lambda-eventsourcemapping-selfmanagedeventsource"></a>

The Self\-Managed Apache Kafka cluster for your event source\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-selfmanagedeventsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-selfmanagedeventsource-syntax.json"></a>

```
{
  "[Endpoints](#cfn-lambda-eventsourcemapping-selfmanagedeventsource-endpoints)" : Endpoints
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-selfmanagedeventsource-syntax.yaml"></a>

```
  [Endpoints](#cfn-lambda-eventsourcemapping-selfmanagedeventsource-endpoints): 
    Endpoints
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-selfmanagedeventsource-properties"></a>

`Endpoints`  <a name="cfn-lambda-eventsourcemapping-selfmanagedeventsource-endpoints"></a>
The list of bootstrap servers for your Kafka brokers in the following format: `"KafkaBootstrapServers": ["abc.xyz.com:xxxx","abc2.xyz.com:xxxx"]`\.  
*Required*: No  
*Type*: [Endpoints](aws-properties-lambda-eventsourcemapping-endpoints.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)