# Amazon GameLift Alias RoutingStrategy<a name="aws-properties-gamelift-alias-routingstrategy"></a>

`RoutingStrategy` is a property of the [AWS::GameLift::Alias](aws-resource-gamelift-alias.md) resource that configures the routing strategy for an Amazon GameLift \(GameLift\) alias\. For more information, see the [RoutingStrategy](http://docs.aws.amazon.com/gamelift/latest/apireference/API_RoutingStrategy.html) data type in the *Amazon GameLift API Reference*\.

## Syntax<a name="w3ab2c21c14e1209b5"></a>

### JSON<a name="aws-properties-gamelift-alias-routingstrategy-syntax.json"></a>

```
{
  "[FleetId](#cfn-gamelift-alias-routingstrategy-fleetid)" : String,
  "[Message](#cfn-gamelift-alias-routingstrategy-message)" : String,
  "[Type](#cfn-gamelift-alias-routingstrategy-type)" : String
}
```

### YAML<a name="aws-properties-gamelift-alias-routingstrategy-syntax.yaml"></a>

```
[FleetId](#cfn-gamelift-alias-routingstrategy-fleetid): String
[Message](#cfn-gamelift-alias-routingstrategy-message): String
[Type](#cfn-gamelift-alias-routingstrategy-type): String
```

## Properties<a name="w3ab2c21c14e1209b7"></a>

`FleetId`  <a name="cfn-gamelift-alias-routingstrategy-fleetid"></a>
A unique identifier of a GameLift fleet to associate with the alias\.  
*Required*: Conditional\. If you specify `SIMPLE` for the `Type` property, you must specify this property\.  
*Type*: String

`Message`  <a name="cfn-gamelift-alias-routingstrategy-message"></a>
A text message that GameLift displays for the `Terminal` routing type\.  
*Required*: Conditional\. If you specify `TERMINAL` for the `Type` property, you must specify this property\.  
*Type*: String

`Type`  <a name="cfn-gamelift-alias-routingstrategy-type"></a>
The type of routing strategy\. For the `SIMPLE` type, traffic is routed to an active GameLift fleet\. For the `Terminal` type, GameLift returns an exception with the message that you specified in the `Message` property\.  
*Required*: Yes  
*Type*: String