# AWS::GameLift::MatchmakingRuleSet<a name="aws-resource-gamelift-matchmakingruleset"></a>

Creates a new rule set for FlexMatch matchmaking\. A rule set describes the type of match to create, such as the number and size of teams\. It also sets the parameters for acceptable player matches, such as minimum skill level or character type\. 

To create a matchmaking rule set, provide unique rule set name and the rule set body in JSON format\. Rule sets must be defined in the same Region as the matchmaking configuration they are used with\.

Since matchmaking rule sets cannot be edited, it is a good idea to check the rule set syntax\.

 **Learn more** 
+  [Build a rule set](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-rulesets.html) 
+  [Design a matchmaker](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-configuration.html) 
+  [Matchmaking with FlexMatch](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-intro.html) 

## Syntax<a name="aws-resource-gamelift-matchmakingruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-matchmakingruleset-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::MatchmakingRuleSet",
  "Properties" : {
      "[Name](#cfn-gamelift-matchmakingruleset-name)" : String,
      "[RuleSetBody](#cfn-gamelift-matchmakingruleset-rulesetbody)" : String,
      "[Tags](#cfn-gamelift-matchmakingruleset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-gamelift-matchmakingruleset-syntax.yaml"></a>

```
Type: AWS::GameLift::MatchmakingRuleSet
Properties: 
  [Name](#cfn-gamelift-matchmakingruleset-name): String
  [RuleSetBody](#cfn-gamelift-matchmakingruleset-rulesetbody): String
  [Tags](#cfn-gamelift-matchmakingruleset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-gamelift-matchmakingruleset-properties"></a>

`Name`  <a name="cfn-gamelift-matchmakingruleset-name"></a>
A unique identifier for the matchmaking rule set\. A matchmaking configuration identifies the rule set it uses by this name value\. Note that the rule set name is different from the optional `name` field in the rule set body\.  
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

`Tags`  <a name="cfn-gamelift-matchmakingruleset-tags"></a>
A list of labels to assign to the new matchmaking rule set resource\. Tags are developer\-defined key\-value pairs\. Tagging AWS resources are useful for resource management, access management and cost allocation\. For more information, see [ Tagging AWS Resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference*\. Once the resource is created, you can use TagResource, UntagResource, and ListTagsForResource to add, remove, and view tags\. The maximum tag limit may be lower than stated\. See the AWS General Reference for actual tagging limits\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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
+ [ Create GameLift Resources Using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Build a FlexMatch Rule Set](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-rulesets.html) in the *Amazon GameLift Developer Guide*
+  [ CreateMatchmakingRuleSet](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateMatchmakingRuleSet.html) in the *Amazon GameLift API Reference* 