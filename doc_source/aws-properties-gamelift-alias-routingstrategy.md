# AWS::GameLift::Alias RoutingStrategy<a name="aws-properties-gamelift-alias-routingstrategy"></a>

Routing configuration for a fleet alias\.

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
Unique identifier for a fleet that the alias points to\.  
 *Required:* Conditional\. If you specify `SIMPLE` for the `Type` property, you must specify this property\.  
*Required*: No  
*Type*: String  
*Pattern*: `^fleet-\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Message`  <a name="cfn-gamelift-alias-routingstrategy-message"></a>
Message text to be used with a terminal routing strategy\.  
 *Required:* Conditional\. If you specify `TERMINAL` for the `Type` property, you must specify this property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-gamelift-alias-routingstrategy-type"></a>
Type of routing strategy\.  
Possible routing types include the following:  
+  **SIMPLE** \-\- The alias resolves to one specific fleet\. Use this type when routing to active fleets\.
+  **TERMINAL** \-\- The alias does not resolve to a fleet but instead can be used to display a message to the user\. A terminal alias throws a TerminalRoutingStrategyException with the message that you specified in the `Message` property\.
*Required*: Yes  
*Type*: String  
*Allowed Values*: `SIMPLE | TERMINAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-gamelift-alias-routingstrategy--seealso"></a>
+  [RoutingStrategy](https://docs.aws.amazon.com/gamelift/latest/apireference/API_RoutingStrategy.html) in the *Amazon GameLift API Reference* 