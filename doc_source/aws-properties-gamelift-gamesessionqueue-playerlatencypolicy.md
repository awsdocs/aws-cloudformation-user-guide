# AWS::GameLift::GameSessionQueue PlayerLatencyPolicy<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy"></a>

The queue setting that determines the highest latency allowed for individual players when placing a game session\. When a latency policy is in force, a game session cannot be placed with any fleet in a Region where a player reports latency higher than the cap\. Latency policies are only enforced when the placement request contains player latency information\.

## Syntax<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy-syntax.json"></a>

```
{
  "[MaximumIndividualPlayerLatencyMilliseconds](#cfn-gamelift-gamesessionqueue-playerlatencypolicy-maximumindividualplayerlatencymilliseconds)" : Integer,
  "[PolicyDurationSeconds](#cfn-gamelift-gamesessionqueue-playerlatencypolicy-policydurationseconds)" : Integer
}
```

### YAML<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy-syntax.yaml"></a>

```
  [MaximumIndividualPlayerLatencyMilliseconds](#cfn-gamelift-gamesessionqueue-playerlatencypolicy-maximumindividualplayerlatencymilliseconds): Integer
  [PolicyDurationSeconds](#cfn-gamelift-gamesessionqueue-playerlatencypolicy-policydurationseconds): Integer
```

## Properties<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy-properties"></a>

`MaximumIndividualPlayerLatencyMilliseconds`  <a name="cfn-gamelift-gamesessionqueue-playerlatencypolicy-maximumindividualplayerlatencymilliseconds"></a>
The maximum latency value that is allowed for any player, in milliseconds\. All policies must have a value set for this property\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDurationSeconds`  <a name="cfn-gamelift-gamesessionqueue-playerlatencypolicy-policydurationseconds"></a>
The length of time, in seconds, that the policy is enforced while placing a new game session\. A null value for this property means that the policy is enforced until the queue times out\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-gamesessionqueue-playerlatencypolicy--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Create a Queue](https://docs.aws.amazon.com/gamelift/latest/developerguide/queues-creating.html) in the *Amazon GameLift Developer Guide*
+ [PlayerLatencyPolicy](https://docs.aws.amazon.com/gamelift/latest/apireference/API_PlayerLatencyPolicy.html) in the *Amazon GameLift API Reference*