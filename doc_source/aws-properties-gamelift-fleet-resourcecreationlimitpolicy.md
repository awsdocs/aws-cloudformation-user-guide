# AWS::GameLift::Fleet ResourceCreationLimitPolicy<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy"></a>

A policy that limits the number of game sessions a player can create on the same fleet\. This optional policy gives game owners control over how players can consume available game server resources\. A resource creation policy makes the following statement: "An individual player can create a maximum number of new game sessions within a specified time period"\.

The policy is evaluated when a player tries to create a new game session\. For example, assume you have a policy of 10 new game sessions and a time period of 60 minutes\. On receiving a `CreateGameSession` request, Amazon GameLift checks that the player \(identified by `CreatorId`\) has created fewer than 10 game sessions in the past 60 minutes\.

## Syntax<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy-syntax.json"></a>

```
{
  "[NewGameSessionsPerCreator](#cfn-gamelift-fleet-resourcecreationlimitpolicy-newgamesessionspercreator)" : Integer,
  "[PolicyPeriodInMinutes](#cfn-gamelift-fleet-resourcecreationlimitpolicy-policyperiodinminutes)" : Integer
}
```

### YAML<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy-syntax.yaml"></a>

```
  [NewGameSessionsPerCreator](#cfn-gamelift-fleet-resourcecreationlimitpolicy-newgamesessionspercreator): Integer
  [PolicyPeriodInMinutes](#cfn-gamelift-fleet-resourcecreationlimitpolicy-policyperiodinminutes): Integer
```

## Properties<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy-properties"></a>

`NewGameSessionsPerCreator`  <a name="cfn-gamelift-fleet-resourcecreationlimitpolicy-newgamesessionspercreator"></a>
The maximum number of game sessions that an individual can create during the policy period\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyPeriodInMinutes`  <a name="cfn-gamelift-fleet-resourcecreationlimitpolicy-policyperiodinminutes"></a>
The time span used in evaluating the resource creation limit policy\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-fleet-resourcecreationlimitpolicy--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [ResourceCreationLimitPolicy](https://docs.aws.amazon.com/gamelift/latest/apireference/API_ResourceCreationLimitPolicy.html) in the *Amazon GameLift API Reference* 

