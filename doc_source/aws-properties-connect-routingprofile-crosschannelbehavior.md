# AWS::Connect::RoutingProfile CrossChannelBehavior<a name="aws-properties-connect-routingprofile-crosschannelbehavior"></a>

Defines the cross\-channel routing behavior that allows an agent working on a contact in one channel to be offered a contact from a different channel\.

## Syntax<a name="aws-properties-connect-routingprofile-crosschannelbehavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-routingprofile-crosschannelbehavior-syntax.json"></a>

```
{
  "[BehaviorType](#cfn-connect-routingprofile-crosschannelbehavior-behaviortype)" : String
}
```

### YAML<a name="aws-properties-connect-routingprofile-crosschannelbehavior-syntax.yaml"></a>

```
  [BehaviorType](#cfn-connect-routingprofile-crosschannelbehavior-behaviortype): String
```

## Properties<a name="aws-properties-connect-routingprofile-crosschannelbehavior-properties"></a>

`BehaviorType`  <a name="cfn-connect-routingprofile-crosschannelbehavior-behaviortype"></a>
Specifies the other channels that can be routed to an agent handling their current channel\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ROUTE_ANY_CHANNEL | ROUTE_CURRENT_CHANNEL_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)