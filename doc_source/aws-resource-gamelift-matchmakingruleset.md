# AWS::GameLift::MatchmakingRuleSet<a name="aws-resource-gamelift-matchmakingruleset"></a>

The `AWS::GameLift::MatchmakingRuleSet` resource creates a new rule set for FlexMatch matchmaking\. A rule set describes the type of match to create, such as the number and size of teams\. It also sets the parameters for acceptable player matches, such as minimum skill level or character type\. A rule set is used by a matchmaking configuration\.

## Syntax<a name="aws-resource-gamelift-matchmakingruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-matchmakingruleset-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::MatchmakingRuleSet",
  "Properties" : {
      "[Name](#cfn-gamelift-matchmakingruleset-name)" : String,
      "[RuleSetBody](#cfn-gamelift-matchmakingruleset-rulesetbody)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-matchmakingruleset-syntax.yaml"></a>

```
Type: AWS::GameLift::MatchmakingRuleSet
Properties: 
  [Name](#cfn-gamelift-matchmakingruleset-name): String
  [RuleSetBody](#cfn-gamelift-matchmakingruleset-rulesetbody): String
```

## Properties<a name="aws-resource-gamelift-matchmakingruleset-properties"></a>

`Name`  <a name="cfn-gamelift-matchmakingruleset-name"></a>
A unique identifier for a matchmaking rule set\. A matchmaking configuration identifies the rule set it uses by this name value\. Note that the rule set name is different from the optional `name` field in the rule set body\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-\.]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RuleSetBody`  <a name="cfn-gamelift-matchmakingruleset-rulesetbody"></a>
A collection of matchmaking rules, formatted as a JSON string\. Comments are not allowed in JSON, but most elements support a description field\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-gamelift-matchmakingruleset-return-values"></a>

### Ref<a name="aws-resource-gamelift-matchmakingruleset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the rule set name, which is unique within each Region\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-matchmakingruleset-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-matchmakingruleset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The unique Amazon Resource Name \(ARN\) assigned to the rule set\.

`Name`  <a name="Name-fn::getatt"></a>
The unique name of the rule set\.

## Examples<a name="aws-resource-gamelift-matchmakingruleset--examples"></a>

### Create a Matchmaking Rule Set<a name="aws-resource-gamelift-matchmakingruleset--examples--Create_a_Matchmaking_Rule_Set"></a>

The following example creates a matchmaking rule set for GameLift FlexMatch named `MyRuleSet`\. The simple rule set defines a match with one team containing 1 to 20 players\. In the YAML example, since RuleSetBody must be in JSON format, the \!Sub command is used to specify JSON content within the YAML format\. 

#### JSON<a name="aws-resource-gamelift-matchmakingruleset--examples--Create_a_Matchmaking_Rule_Set--json"></a>

```
{
  "Resources": {
    "MatchmakingRuleSet": {
      "Type": "AWS::GameLift::MatchmakingRuleSet",
      "Properties": {
        "Name": "MyRuleSet",
        "RuleSetBody": {
          "Fn::Sub": "{\"name\": \"MyMatchmakingRuleSet\",\"ruleLanguageVersion\": \"1.0\", \"teams\": [{\"name\": \"MyTeam\",\"minPlayers\": 1,\"maxPlayers\": 20}]}"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-gamelift-matchmakingruleset--examples--Create_a_Matchmaking_Rule_Set--yaml"></a>

```
Resources:
  MatchmakingRuleSet:
    Type: "AWS::GameLift::MatchmakingRuleSet"
    Properties:
      Name: "MyRuleSet"
      RuleSetBody: !Sub |
        {
          "name": "MyMatchmakingRuleSet",
          "ruleLanguageVersion": "1.0",
          "teams": [{
                      "name": "MyTeam",
                      "minPlayers": 1,
                      "maxPlayers": 20
                  }]
        }
```

## See also<a name="aws-resource-gamelift-matchmakingruleset--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Build a FlexMatch Rule Set](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-rulesets.html) in the *Amazon GameLift Developer Guide*
+  [ CreateMatchmakingRuleSet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateMatchmakingRuleSet.html) in the *Amazon GameLift API Reference* 