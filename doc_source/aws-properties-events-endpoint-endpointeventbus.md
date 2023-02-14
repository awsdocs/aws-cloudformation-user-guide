# AWS::Events::Endpoint EndpointEventBus<a name="aws-properties-events-endpoint-endpointeventbus"></a>

The event buses the endpoint is associated with\.

## Syntax<a name="aws-properties-events-endpoint-endpointeventbus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-endpoint-endpointeventbus-syntax.json"></a>

```
{
  "[EventBusArn](#cfn-events-endpoint-endpointeventbus-eventbusarn)" : String
}
```

### YAML<a name="aws-properties-events-endpoint-endpointeventbus-syntax.yaml"></a>

```
  [EventBusArn](#cfn-events-endpoint-endpointeventbus-eventbusarn): String
```

## Properties<a name="aws-properties-events-endpoint-endpointeventbus-properties"></a>

`EventBusArn`  <a name="cfn-events-endpoint-endpointeventbus-eventbusarn"></a>
The ARN of the event bus the endpoint is associated with\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^arn:aws[a-z-]*:events:[a-z]{2}-[a-z-]+-\d+:\d{12}:event-bus/[\w.-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)