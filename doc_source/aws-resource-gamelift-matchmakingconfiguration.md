# AWS::GameLift::MatchmakingConfiguration<a name="aws-resource-gamelift-matchmakingconfiguration"></a>

The `AWS::GameLift::MatchmakingConfiguration` resource defines a new matchmaking configuration for use with FlexMatch\. Whether you're using FlexMatch with GameLift hosting or as a standalone matchmaking service, the matchmaking configuration sets out rules for matching players and forming teams\. If you're using GameLift hosting, it also defines how to start game sessions for each match\. Your matchmaking system can use multiple configurations to handle different game scenarios\. All matchmaking requests identify the matchmaking configuration to use and provide player attributes that are consistent with that configuration\.

## Syntax<a name="aws-resource-gamelift-matchmakingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-matchmakingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::MatchmakingConfiguration",
  "Properties" : {
      "[AcceptanceRequired](#cfn-gamelift-matchmakingconfiguration-acceptancerequired)" : Boolean,
      "[AcceptanceTimeoutSeconds](#cfn-gamelift-matchmakingconfiguration-acceptancetimeoutseconds)" : Integer,
      "[AdditionalPlayerCount](#cfn-gamelift-matchmakingconfiguration-additionalplayercount)" : Integer,
      "[BackfillMode](#cfn-gamelift-matchmakingconfiguration-backfillmode)" : String,
      "[CustomEventData](#cfn-gamelift-matchmakingconfiguration-customeventdata)" : String,
      "[Description](#cfn-gamelift-matchmakingconfiguration-description)" : String,
      "[FlexMatchMode](#cfn-gamelift-matchmakingconfiguration-flexmatchmode)" : String,
      "[GameProperties](#cfn-gamelift-matchmakingconfiguration-gameproperties)" : [ GameProperty, ... ],
      "[GameSessionData](#cfn-gamelift-matchmakingconfiguration-gamesessiondata)" : String,
      "[GameSessionQueueArns](#cfn-gamelift-matchmakingconfiguration-gamesessionqueuearns)" : [ String, ... ],
      "[Name](#cfn-gamelift-matchmakingconfiguration-name)" : String,
      "[NotificationTarget](#cfn-gamelift-matchmakingconfiguration-notificationtarget)" : String,
      "[RequestTimeoutSeconds](#cfn-gamelift-matchmakingconfiguration-requesttimeoutseconds)" : Integer,
      "[RuleSetName](#cfn-gamelift-matchmakingconfiguration-rulesetname)" : String,
      "[Tags](#cfn-gamelift-matchmakingconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-gamelift-matchmakingconfiguration-syntax.yaml"></a>

```
Type: AWS::GameLift::MatchmakingConfiguration
Properties: 
  [AcceptanceRequired](#cfn-gamelift-matchmakingconfiguration-acceptancerequired): Boolean
  [AcceptanceTimeoutSeconds](#cfn-gamelift-matchmakingconfiguration-acceptancetimeoutseconds): Integer
  [AdditionalPlayerCount](#cfn-gamelift-matchmakingconfiguration-additionalplayercount): Integer
  [BackfillMode](#cfn-gamelift-matchmakingconfiguration-backfillmode): String
  [CustomEventData](#cfn-gamelift-matchmakingconfiguration-customeventdata): String
  [Description](#cfn-gamelift-matchmakingconfiguration-description): String
  [FlexMatchMode](#cfn-gamelift-matchmakingconfiguration-flexmatchmode): String
  [GameProperties](#cfn-gamelift-matchmakingconfiguration-gameproperties): 
    - GameProperty
  [GameSessionData](#cfn-gamelift-matchmakingconfiguration-gamesessiondata): String
  [GameSessionQueueArns](#cfn-gamelift-matchmakingconfiguration-gamesessionqueuearns): 
    - String
  [Name](#cfn-gamelift-matchmakingconfiguration-name): String
  [NotificationTarget](#cfn-gamelift-matchmakingconfiguration-notificationtarget): String
  [RequestTimeoutSeconds](#cfn-gamelift-matchmakingconfiguration-requesttimeoutseconds): Integer
  [RuleSetName](#cfn-gamelift-matchmakingconfiguration-rulesetname): String
  [Tags](#cfn-gamelift-matchmakingconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-gamelift-matchmakingconfiguration-properties"></a>

`AcceptanceRequired`  <a name="cfn-gamelift-matchmakingconfiguration-acceptancerequired"></a>
A flag that determines whether a match that was created with this configuration must be accepted by the matched players\. To require acceptance, set to `TRUE`\. With this option enabled, matchmaking tickets use the status `REQUIRES_ACCEPTANCE` to indicate when a completed potential match is waiting for player acceptance\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AcceptanceTimeoutSeconds`  <a name="cfn-gamelift-matchmakingconfiguration-acceptancetimeoutseconds"></a>
The length of time \(in seconds\) to wait for players to accept a proposed match, if acceptance is required\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalPlayerCount`  <a name="cfn-gamelift-matchmakingconfiguration-additionalplayercount"></a>
The number of player slots in a match to keep open for future players\. For example, if the configuration's rule set specifies a match for a single 12\-person team, and the additional player count is set to 2, only 10 players are selected for the match\. This parameter is not used if `FlexMatchMode` is set to `STANDALONE`\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackfillMode`  <a name="cfn-gamelift-matchmakingconfiguration-backfillmode"></a>
The method used to backfill game sessions that are created with this matchmaking configuration\. Specify `MANUAL` when your game manages backfill requests manually or does not use the match backfill feature\. Specify `AUTOMATIC` to have GameLift create a `StartMatchBackfill` request whenever a game session has one or more open slots\. Learn more about manual and automatic backfill in [Backfill Existing Games with FlexMatch](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-backfill.html)\. Automatic backfill is not available when `FlexMatchMode` is set to `STANDALONE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | MANUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomEventData`  <a name="cfn-gamelift-matchmakingconfiguration-customeventdata"></a>
Information to add to all events related to the matchmaking configuration\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-gamelift-matchmakingconfiguration-description"></a>
A description for the matchmaking configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlexMatchMode`  <a name="cfn-gamelift-matchmakingconfiguration-flexmatchmode"></a>
Indicates whether this matchmaking configuration is being used with GameLift hosting or as a standalone matchmaking solution\.   
+  **STANDALONE** \- FlexMatch forms matches and returns match information, including players and team assignments, in a [ MatchmakingSucceeded](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-events.html#match-events-matchmakingsucceeded) event\.
+  **WITH\_QUEUE** \- FlexMatch forms matches and uses the specified GameLift queue to start a game session for the match\. 
*Required*: No  
*Type*: String  
*Allowed values*: `STANDALONE | WITH_QUEUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GameProperties`  <a name="cfn-gamelift-matchmakingconfiguration-gameproperties"></a>
A set of custom properties for a game session, formatted as key\-value pairs\. These properties are passed to a game server process with a request to start a new game session\. See [ Start a Game Session](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-api.html#gamelift-sdk-server-startsession)\. This parameter is not used if `FlexMatchMode` is set to `STANDALONE`\.  
*Required*: No  
*Type*: List of [GameProperty](aws-properties-gamelift-matchmakingconfiguration-gameproperty.md)  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GameSessionData`  <a name="cfn-gamelift-matchmakingconfiguration-gamesessiondata"></a>
A set of custom game session properties, formatted as a single string value\. This data is passed to a game server process with a request to start a new game session\. See [Start a Game Session](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-sdk-server-api.html#gamelift-sdk-server-startsession)\. This parameter is not used if`FlexMatchMode` is set to `STANDALONE`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GameSessionQueueArns`  <a name="cfn-gamelift-matchmakingconfiguration-gamesessionqueuearns"></a>
The Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) that is assigned to a GameLift game session queue resource and uniquely identifies it\. ARNs are unique across all Regions\. Format is `arn:aws:gamelift:<region>::gamesessionqueue/<queue name>`\. Queues can be located in any Region\. Queues are used to start new GameLift\-hosted game sessions for matches that are created with this matchmaking configuration\. If `FlexMatchMode` is set to `STANDALONE`, do not set this parameter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-matchmakingconfiguration-name"></a>
A unique identifier for the matchmaking configuration\. This name is used to identify the configuration associated with a matchmaking request or ticket\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-\.]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotificationTarget`  <a name="cfn-gamelift-matchmakingconfiguration-notificationtarget"></a>
An SNS topic ARN that is set up to receive matchmaking notifications\. See [ Setting up notifications for matchmaking](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/match-notification.html) for more information\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `300`  
*Pattern*: `[a-zA-Z0-9:_/-]*(.fifo)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestTimeoutSeconds`  <a name="cfn-gamelift-matchmakingconfiguration-requesttimeoutseconds"></a>
The maximum duration, in seconds, that a matchmaking ticket can remain in process before timing out\. Requests that fail due to timing out can be resubmitted as needed\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `43200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleSetName`  <a name="cfn-gamelift-matchmakingconfiguration-rulesetname"></a>
A unique identifier for the matchmaking rule set to use with this configuration\. You can use either the rule set name or ARN value\. A matchmaking configuration can only use rule sets that are defined in the same Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9-\.]*|^arn:.*:matchmakingruleset\/[a-zA-Z0-9-\.]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-gamelift-matchmakingconfiguration-tags"></a>
A list of labels to assign to the new matchmaking configuration resource\. Tags are developer\-defined key\-value pairs\. Tagging AWS resources are useful for resource management, access management and cost allocation\. For more information, see [ Tagging AWS Resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference*\. Once the resource is created, you can use TagResource, UntagResource, and ListTagsForResource to add, remove, and view tags\. The maximum tag limit may be lower than stated\. See the AWS General Reference for actual tagging limits\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-matchmakingconfiguration-return-values"></a>

### Ref<a name="aws-resource-gamelift-matchmakingconfiguration-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `MatchmakingConfiguration` name, which is unique\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-matchmakingconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-matchmakingconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The unique Amazon Resource Name \(ARN\) for the `MatchmakingConfiguration`\.

`Name`  <a name="Name-fn::getatt"></a>
 The `MatchmakingConfiguration` name, which is unique\.

## Examples<a name="aws-resource-gamelift-matchmakingconfiguration--examples"></a>

### Create a matchmaking configuration for use with GameLift managed hosting<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_use_with_GameLift_managed_hosting"></a>

The following example creates a matchmaking configuration for a game that is being hosted on GameLift servers, identifying a game session queue and providing a set of game properties to be passed on to new game sessions\. Player acceptance is required, with a 60\-second timeout, and auto\-backfill is enabled\. The example uses a `Ref` intrinsic function to specify the game session queue and rule set, which are also in the template\. 

#### JSON<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_use_with_GameLift_managed_hosting--json"></a>

```
{
    "Resources": {
        "QueueResource": {
            "Type": "AWS::GameLift::GameSessionQueue",
            "Properties": {
                "Name": "MyGameSessionQueue"
            }
        },
        "MatchmakingRuleSetResource": {
            "Type": "AWS::GameLift::MatchmakingRuleSet",
            "Properties": {
                "Name": "MyRuleSet",
                "RuleSetBody": {
                  "Fn::Sub": "{\"name\": \"MyMatchmakingRuleSet\",\"ruleLanguageVersion\": \"1.0\", \"teams\": [{\"name\": \"MyTeam\",\"minPlayers\": 1,\"maxPlayers\": 20}]}"
                }
            }            
        },
        "MatchmakingConfigurationResource": {
            "Type": "AWS::GameLift::MatchmakingConfiguration",
            "Properties": {
                "Name": "MyMatchmakingConfiguration",
                "AcceptanceRequired": true,
                "AcceptanceTimeoutSeconds": 60,
                "AdditionalPlayerCount": 8,
                "BackfillMode": "AUTOMATIC",
                "CustomEventData": "MyCustomEventData",
                "Description": "A basic matchmaking configuration for a GameLift-hosted game",
                "FlexMatchMode": "WITH_QUEUE",
                "GameSessionData": "MyGameSessionData",
                "GameProperties": [
                    {
                        "Key": "level",
                        "Value": "10"
                    },
                    {
                        "Key": "gameMode",
                        "Value": "hard"
                    }
                ],
                "GameSessionQueueArns": [
                    {
                        "Fn::GetAtt": [
                            "QueueResource",
                            "Arn"
                        ]
                    }
                ],
                "RequestTimeoutSeconds": 100,
                "RuleSetName": {
                    "Ref": "MatchmakingRuleSetResource"
                }
            },
            "DependsOn": [
                "QueueResource",
                "MatchmakingRuleSetResource"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_use_with_GameLift_managed_hosting--yaml"></a>

```
Resources:
  QueueResource:
    Type: "AWS::GameLift::GameSessionQueue"
    Properties:
      Name: "MyGameSessionQueue"
  MatchmakingRuleSetResource:
    Type: "AWS::GameLift::MatchmakingRuleSet"
    Properties:
      Name: "MyRuleSet"
      # Rule set body for a game of 20 players
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
  MatchmakingConfigurationResource:
    Type: "AWS::GameLift::MatchmakingConfiguration"
    Properties:
      Name: "MyMatchmakingConfiguration"
      AcceptanceRequired: true
      AcceptanceTimeoutSeconds: 60
      AdditionalPlayerCount: 8
      BackfillMode: "AUTOMATIC"
      CustomEventData: "MyCustomEventData"
      Description: "A basic matchmaking configuration for a GameLift-hosted game"
      FlexMatchMode: "WITH_QUEUE"
      GameSessionData: "MyGameSessionData"
      GameProperties:
        - Key: "level"
          Value: "10"
        - Key: "gameMode"
          Value: "hard"
      GameSessionQueueArns:
        - !GetAtt QueueResource.Arn
      RequestTimeoutSeconds: 100
      RuleSetName: !Ref MatchmakingRuleSetResource
    DependsOn:
      - QueueResource
      - MatchmakingRuleSetResource
```

### Create a matchmaking configuration for a standalone FlexMatch system<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_a_standalone_FlexMatch_system"></a>

The following example creates a matchmaking configuration for a game that is hosted on resources other than GameLift game servers\. This includes games that are hosted on Amazon EC2 with GameLift FleetIQ\. This configuration omits the game session queue, game properties and session data, and additional player count\. Player acceptance is required, with a 60\-second timeout\. It uses a `Ref` intrinsic function to specify the rule set, which is also in the template\. 

#### JSON<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_a_standalone_FlexMatch_system--json"></a>

```
{
    "Resources": {
        "MatchmakingRuleSetResource": {
            "Type": "AWS::GameLift::MatchmakingRuleSet",
            "Properties": {
                "Name": "MyRuleSet",
                "RuleSetBody": {
                    "Fn::Sub": "{\"name\": \"MyMatchmakingRuleSet\",\"ruleLanguageVersion\": \"1.0\", \"teams\": [{\"name\": \"MyTeam\",\"minPlayers\": 1,\"maxPlayers\": 20}]}"
                }
            }            
        },
        "MatchmakingConfigurationResource": {
            "Type": "AWS::GameLift::MatchmakingConfiguration",
            "Properties": {
                "Name": "MyMatchmakingConfiguration",
                "AcceptanceRequired": true,
                "AcceptanceTimeoutSeconds": 60,
                "BackfillMode": "MANUAL",
                "CustomEventData": "MyCustomEventData",
                "Description": "A basic standalone matchmaking configuration",
                "FlexMatchMode": "STANDALONE",
                "RequestTimeoutSeconds": 100,
                "RuleSetName": {
                    "Ref": "MatchmakingRuleSetResource"
                }
            },
            "DependsOn": [
                "MatchmakingRuleSetResource"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-matchmakingconfiguration--examples--Create_a_matchmaking_configuration_for_a_standalone_FlexMatch_system--yaml"></a>

```
Resources:
    MatchmakingRuleSetResource:
        Type: "AWS::GameLift::MatchmakingRuleSet"
        Properties:
            Name: "MyRuleSet"
            # Rule set body for a game of 20 players
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
    MatchmakingConfigurationResource:
        Type: "AWS::GameLift::MatchmakingConfiguration"
        Properties:
            Name: "MyMatchmakingConfiguration"
            AcceptanceRequired: true
            AcceptanceTimeoutSeconds: 60
            BackfillMode: "MANUAL"
            CustomEventData: "MyCustomEventData"
            Description: "A basic standalone matchmaking configuration"
            FlexMatchMode: "STANDALONE"
            RequestTimeoutSeconds: 100
            RuleSetName: !Ref MatchmakingRuleSetResource
        DependsOn:
          - MatchmakingRuleSetResource
```

## See also<a name="aws-resource-gamelift-matchmakingconfiguration--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Setting up GameLift FlexMatch matchmakers](https://docs.aws.amazon.com/gamelift/latest/flexmatchguide/matchmaker-build.html) in the *Amazon GameLift Developer Guide* 
+ [MatchmakingConfiguration](https://docs.aws.amazon.com/gamelift/latest/apireference/API_MatchmakingConfiguration.html) in the *Amazon GameLift API Reference* 

