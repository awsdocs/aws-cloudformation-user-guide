# AWS::Connect::RoutingProfile RoutingProfileQueueReference<a name="aws-properties-connect-routingprofile-routingprofilequeuereference"></a>

Contains the channel and queue identifier for a routing profile\.

## Syntax<a name="aws-properties-connect-routingprofile-routingprofilequeuereference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-routingprofile-routingprofilequeuereference-syntax.json"></a>

```
{
  "[Channel](#cfn-connect-routingprofile-routingprofilequeuereference-channel)" : String,
  "[QueueArn](#cfn-connect-routingprofile-routingprofilequeuereference-queuearn)" : String
}
```

### YAML<a name="aws-properties-connect-routingprofile-routingprofilequeuereference-syntax.yaml"></a>

```
  [Channel](#cfn-connect-routingprofile-routingprofilequeuereference-channel): String
  [QueueArn](#cfn-connect-routingprofile-routingprofilequeuereference-queuearn): String
```

## Properties<a name="aws-properties-connect-routingprofile-routingprofilequeuereference-properties"></a>

`Channel`  <a name="cfn-connect-routingprofile-routingprofilequeuereference-channel"></a>
The channels agents can handle in the Contact Control Panel \(CCP\) for this routing profile\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CHAT | TASK | VOICE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueArn`  <a name="cfn-connect-routingprofile-routingprofilequeuereference-queuearn"></a>
The Amazon Resource Name \(ARN\) of the queue\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)