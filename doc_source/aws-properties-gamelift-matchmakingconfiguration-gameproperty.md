# AWS::GameLift::MatchmakingConfiguration GameProperty<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty"></a>

A set of key\-value pairs that contain information about a game session\. When included in a game session request, these properties communicate details to be used when setting up the new game session\. For example, a property might specify a game mode, level, or map\. Game properties are passed to the game server process when initiating a new game session\. 

## Syntax<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty-syntax.json"></a>

```
{
  "[Key](#cfn-gamelift-matchmakingconfiguration-gameproperty-key)" : String,
  "[Value](#cfn-gamelift-matchmakingconfiguration-gameproperty-value)" : String
}
```

### YAML<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty-syntax.yaml"></a>

```
  [Key](#cfn-gamelift-matchmakingconfiguration-gameproperty-key): String
  [Value](#cfn-gamelift-matchmakingconfiguration-gameproperty-value): String
```

## Properties<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty-properties"></a>

`Key`  <a name="cfn-gamelift-matchmakingconfiguration-gameproperty-key"></a>
The game property identifier\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-gamelift-matchmakingconfiguration-gameproperty-value"></a>
The game property value\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `96`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-matchmakingconfiguration-gameproperty--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Design a FlexMatch Matchmaker](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-configuration.html) in the *Amazon GameLift Developer Guide* 
+  [GameProperty](https://docs.aws.amazon.com/gamelift/latest/apireference/API_GameProperty.html) in the *Amazon GameLift API Reference* 

