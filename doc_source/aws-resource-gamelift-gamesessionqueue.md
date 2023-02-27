# AWS::GameLift::GameSessionQueue<a name="aws-resource-gamelift-gamesessionqueue"></a>

The `AWS::GameLift::GameSessionQueue` resource creates a placement queue that processes requests for new game sessions\. A queue uses FleetIQ algorithms to determine the best placement locations and find an available game server, then prompts the game server to start a new game session\. Queues can have destinations \(GameLift fleets or aliases\), which determine where the queue can place new game sessions\. A queue can have destinations with varied fleet type \(Spot and On\-Demand\), instance type, and AWS Region\. 

## Syntax<a name="aws-resource-gamelift-gamesessionqueue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-gamesessionqueue-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::GameSessionQueue",
  "Properties" : {
      "[CustomEventData](#cfn-gamelift-gamesessionqueue-customeventdata)" : String,
      "[Destinations](#cfn-gamelift-gamesessionqueue-destinations)" : [ Destination, ... ],
      "[FilterConfiguration](#cfn-gamelift-gamesessionqueue-filterconfiguration)" : FilterConfiguration,
      "[Name](#cfn-gamelift-gamesessionqueue-name)" : String,
      "[NotificationTarget](#cfn-gamelift-gamesessionqueue-notificationtarget)" : String,
      "[PlayerLatencyPolicies](#cfn-gamelift-gamesessionqueue-playerlatencypolicies)" : [ PlayerLatencyPolicy, ... ],
      "[PriorityConfiguration](#cfn-gamelift-gamesessionqueue-priorityconfiguration)" : PriorityConfiguration,
      "[Tags](#cfn-gamelift-gamesessionqueue-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TimeoutInSeconds](#cfn-gamelift-gamesessionqueue-timeoutinseconds)" : Integer
    }
}
```

### YAML<a name="aws-resource-gamelift-gamesessionqueue-syntax.yaml"></a>

```
Type: AWS::GameLift::GameSessionQueue
Properties: 
  [CustomEventData](#cfn-gamelift-gamesessionqueue-customeventdata): String
  [Destinations](#cfn-gamelift-gamesessionqueue-destinations): 
    - Destination
  [FilterConfiguration](#cfn-gamelift-gamesessionqueue-filterconfiguration): 
    FilterConfiguration
  [Name](#cfn-gamelift-gamesessionqueue-name): String
  [NotificationTarget](#cfn-gamelift-gamesessionqueue-notificationtarget): String
  [PlayerLatencyPolicies](#cfn-gamelift-gamesessionqueue-playerlatencypolicies): 
    - PlayerLatencyPolicy
  [PriorityConfiguration](#cfn-gamelift-gamesessionqueue-priorityconfiguration): 
    PriorityConfiguration
  [Tags](#cfn-gamelift-gamesessionqueue-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TimeoutInSeconds](#cfn-gamelift-gamesessionqueue-timeoutinseconds): Integer
```

## Properties<a name="aws-resource-gamelift-gamesessionqueue-properties"></a>

`CustomEventData`  <a name="cfn-gamelift-gamesessionqueue-customeventdata"></a>
Information to be added to all events that are related to this game session queue\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destinations`  <a name="cfn-gamelift-gamesessionqueue-destinations"></a>
A list of fleets and/or fleet aliases that can be used to fulfill game session placement requests in the queue\. Destinations are identified by either a fleet ARN or a fleet alias ARN, and are listed in order of placement preference\.  
*Required*: No  
*Type*: List of [Destination](aws-properties-gamelift-gamesessionqueue-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterConfiguration`  <a name="cfn-gamelift-gamesessionqueue-filterconfiguration"></a>
A list of locations where a queue is allowed to place new game sessions\. Locations are specified in the form of AWS Region codes, such as `us-west-2`\. If this parameter is not set, game sessions can be placed in any queue location\.   
*Required*: No  
*Type*: [FilterConfiguration](aws-properties-gamelift-gamesessionqueue-filterconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-gamesessionqueue-name"></a>
A descriptive label that is associated with game session queue\. Queue names must be unique within each Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotificationTarget`  <a name="cfn-gamelift-gamesessionqueue-notificationtarget"></a>
An SNS topic ARN that is set up to receive game session placement notifications\. See [ Setting up notifications for game session placement](https://docs.aws.amazon.com/gamelift/latest/developerguide/queue-notification.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `300`  
*Pattern*: `[a-zA-Z0-9:_-]*(\.fifo)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlayerLatencyPolicies`  <a name="cfn-gamelift-gamesessionqueue-playerlatencypolicies"></a>
A set of policies that act as a sliding cap on player latency\. FleetIQ works to deliver low latency for most players in a game session\. These policies ensure that no individual player can be placed into a game with unreasonably high latency\. Use multiple policies to gradually relax latency requirements a step at a time\. Multiple policies are applied based on their maximum allowed latency, starting with the lowest value\.  
*Required*: No  
*Type*: List of [PlayerLatencyPolicy](aws-properties-gamelift-gamesessionqueue-playerlatencypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PriorityConfiguration`  <a name="cfn-gamelift-gamesessionqueue-priorityconfiguration"></a>
Custom settings to use when prioritizing destinations and locations for game session placements\. This configuration replaces the FleetIQ default prioritization process\. Priority types that are not explicitly named will be automatically applied at the end of the prioritization process\.   
*Required*: No  
*Type*: [PriorityConfiguration](aws-properties-gamelift-gamesessionqueue-priorityconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-gamelift-gamesessionqueue-tags"></a>
A list of labels to assign to the new game session queue resource\. Tags are developer\-defined key\-value pairs\. Tagging AWS resources are useful for resource management, access management and cost allocation\. For more information, see [ Tagging AWS Resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) in the * AWS General Reference*\. Once the resource is created, you can use TagResource, UntagResource, and ListTagsForResource to add, remove, and view tags\. The maximum tag limit may be lower than stated\. See the AWS General Reference for actual tagging limits\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInSeconds`  <a name="cfn-gamelift-gamesessionqueue-timeoutinseconds"></a>
The maximum time, in seconds, that a new game session placement request remains in the queue\. When a request exceeds this time, the game session placement changes to a `TIMED_OUT` status\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-gamesessionqueue-return-values"></a>

### Ref<a name="aws-resource-gamelift-gamesessionqueue-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the game session queue, which is unique within each Region\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-gamesessionqueue-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-gamesessionqueue-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The unique Amazon Resource Name \(ARN\) for the `GameSessionQueue`\.

`Name`  <a name="Name-fn::getatt"></a>
A descriptive label that is associated with a game session queue\. Names are unique within each Region\.

## Examples<a name="aws-resource-gamelift-gamesessionqueue--examples"></a>

### Create a Game Session Queue<a name="aws-resource-gamelift-gamesessionqueue--examples--Create_a_Game_Session_Queue"></a>

The following example creates a GameLift game session queue named `MyGameSessionQueue`\. The queue is configured with two destinations, one using a fleet ID and one using an alias ID\. The queue has a latency policy\.

#### JSON<a name="aws-resource-gamelift-gamesessionqueue--examples--Create_a_Game_Session_Queue--json"></a>

```
{
    "Resources": {
        "Queue": {
            "Type": "AWS::GameLift::GameSessionQueue",
            "Properties": {
                "Name": "MyGameSessionQueue",
                "TimeoutInSeconds": 60,
                "NotificationTarget": "arn:aws:sns:us-west-2:111122223333:My_Placement_SNS_Topic",
                "Destinations": [
                    {
                        "DestinationArn": "arn:aws:gamelift:us-west-2:012345678912:fleet/fleet-id"
                    },
                    {
                        "DestinationArn": "arn:aws:gamelift:us-west-2:012345678912:alias/alias-id"
                    }
                ],
                "PlayerLatencyPolicies": [
                    {
                        "MaximumIndividualPlayerLatencyMilliseconds": 1000,
                        "PolicyDurationSeconds": 60
                    }
                ],
                "PriorityConfiguration": {
                    "LocationOrder": [
                        "us-west-2",
                        "us-east-1"
                    ],
                    "PriorityOrder": [
                        "COST",
                        "LATENCY",
                        "LOCATION",
                        "DESTINATION"
                    ]
                },
                "FilterConfiguration": {
                    "AllowedLocations": [
                        "us-east-1",
                        "us-west-2"
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-gamesessionqueue--examples--Create_a_Game_Session_Queue--yaml"></a>

```
Resources:
  Queue:
    Type: "AWS::GameLift::GameSessionQueue"
    Properties:
      Name: "MyGameSessionQueue"
      TimeoutInSeconds: 60
      NotificationTarget: "arn:aws:sns:us-west-2:111122223333:My_Placement_SNS_Topic"
      Destinations:
        # DestinationArn can be either an Alias arn or Fleet arn that you own
        - DestinationArn: "arn:aws:gamelift:us-west-2:012345678912:fleet/fleet-id"
        - DestinationArn: "arn:aws:gamelift:us-west-2:012345678912:alias/alias-id"
      PlayerLatencyPolicies:
        - MaximumIndividualPlayerLatencyMilliseconds: 1000
          PolicyDurationSeconds: 60
          PriorityConfiguration:
          LocationOrder: 
          - 'us-west-2'
          - 'us-east-1'
          PriorityOrder: 
          - 'COST'
          - 'LATENCY'
          - 'LOCATION'
          - 'DESTINATION'
      FilterConfiguration:
        AllowedLocations:
          - 'us-east-1'
          - 'us-west-2'
```

## See also<a name="aws-resource-gamelift-gamesessionqueue--seealso"></a>
+ [ Create GameLift resources Using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Setting up GameLift queues for game session placement](https://docs.aws.amazon.com/gamelift/latest/developerguide/queues-intro.html) in the *Amazon GameLift Developer Guide*
+  [CreateGameSessionQueue](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateGameSessionQueue.html) in the *Amazon GameLift API Reference* 