# AWS::GreengrassV2::ComponentVersion LambdaEventSource<a name="aws-properties-greengrassv2-componentversion-lambdaeventsource"></a>

Contains information about an event source for an AWS Lambda function\. The event source defines the topics on which this Lambda function subscribes to receive messages that run the function\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdaeventsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdaeventsource-syntax.json"></a>

```
{
  "[Topic](#cfn-greengrassv2-componentversion-lambdaeventsource-topic)" : String,
  "[Type](#cfn-greengrassv2-componentversion-lambdaeventsource-type)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdaeventsource-syntax.yaml"></a>

```
  [Topic](#cfn-greengrassv2-componentversion-lambdaeventsource-topic): String
  [Type](#cfn-greengrassv2-componentversion-lambdaeventsource-type): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdaeventsource-properties"></a>

`Topic`  <a name="cfn-greengrassv2-componentversion-lambdaeventsource-topic"></a>
The topic to which to subscribe to receive event messages\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-greengrassv2-componentversion-lambdaeventsource-type"></a>
The type of event source\. Choose from the following options:  
+ `PUB_SUB` – Subscribe to local publish/subscribe messages\. This event source type doesn't support MQTT wildcards \(`+` and `#`\) in the event source topic\.
+ `IOT_CORE` – Subscribe to AWS IoT Core MQTT messages\. This event source type supports MQTT wildcards \(`+` and `#`\) in the event source topic\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)