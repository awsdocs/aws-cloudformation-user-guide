# AWS::GameLift::Alias RoutingStrategy<a name="aws-properties-gamelift-alias-routingstrategy"></a>

The routing configuration for a fleet alias\.

## Syntax<a name="aws-properties-gamelift-alias-routingstrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-gamelift-alias-routingstrategy-properties"></a>

`FleetId`  <a name="cfn-gamelift-alias-routingstrategy-fleetid"></a>
A unique identifier for a fleet that the alias points to\. If you specify `SIMPLE` for the `Type` property, you must specify this property\.  
*Required*: Conditional  
*Type*: String  
*Pattern*: `^fleet-\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Message`  <a name="cfn-gamelift-alias-routingstrategy-message"></a>
The message text to be used with a terminal routing strategy\. If you specify `TERMINAL` for the `Type` property, you must specify this property\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-gamelift-alias-routingstrategy-type"></a>
A type of routing strategy\.  
Possible routing types include the following:  
+  **SIMPLE** \- The alias resolves to one specific fleet\. Use this type when routing to active fleets\.
+  **TERMINAL** \- The alias does not resolve to a fleet but instead can be used to display a message to the user\. A terminal alias throws a `TerminalRoutingStrategyException` with the message that you specified in the `Message` property\.
*Required*: No  
*Type*: String  
*Allowed values*: `SIMPLE | TERMINAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-alias-routingstrategy--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Add an Alias to a GameLift Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/aliases-creating.html) in the *Amazon GameLift Developer Guide* 
+  [RoutingStrategy](https://docs.aws.amazon.com/gamelift/latest/apireference/API_RoutingStrategy.html) in the *Amazon GameLift API Reference* 

