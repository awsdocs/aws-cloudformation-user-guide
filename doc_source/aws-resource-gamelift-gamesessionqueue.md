# AWS::GameLift::GameSessionQueue<a name="aws-resource-gamelift-gamesessionqueue"></a>

The `AWS::GameLift::GameSessionQueue` resource establishes a queue for processing requests to create new game sessions\. A queue identifies where new game sessions can be hosted by specifying a list of destinations \(fleets or aliases\)\. It also sets how long requests can wait in the queue before timing out\. You can set up a queue with destinations in multiple Regions\. 

## Syntax<a name="aws-resource-gamelift-gamesessionqueue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-gamesessionqueue-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::GameSessionQueue",
  "Properties" : {
      "[Destinations](#cfn-gamelift-gamesessionqueue-destinations)" : [ Destination, ... ],
      "[Name](#cfn-gamelift-gamesessionqueue-name)" : String,
      "[PlayerLatencyPolicies](#cfn-gamelift-gamesessionqueue-playerlatencypolicies)" : [ PlayerLatencyPolicy, ... ],
      "[TimeoutInSeconds](#cfn-gamelift-gamesessionqueue-timeoutinseconds)" : Integer
    }
}
```

### YAML<a name="aws-resource-gamelift-gamesessionqueue-syntax.yaml"></a>

```
Type: AWS::GameLift::GameSessionQueue
Properties: 
  [Destinations](#cfn-gamelift-gamesessionqueue-destinations): 
    - Destination
  [Name](#cfn-gamelift-gamesessionqueue-name): String
  [PlayerLatencyPolicies](#cfn-gamelift-gamesessionqueue-playerlatencypolicies): 
    - PlayerLatencyPolicy
  [TimeoutInSeconds](#cfn-gamelift-gamesessionqueue-timeoutinseconds): Integer
```

## Properties<a name="aws-resource-gamelift-gamesessionqueue-properties"></a>

`Destinations`  <a name="cfn-gamelift-gamesessionqueue-destinations"></a>
A list of fleets that can be used to fulfill game session placement requests in the queue\. Fleets are identified by either a fleet ARN or a fleet alias ARN\. Destinations are listed in default preference order\.  
*Required*: No  
*Type*: List of [Destination](aws-properties-gamelift-gamesessionqueue-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-gamesessionqueue-name"></a>
A descriptive label that is associated with game session queue\. Queue names must be unique within each Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlayerLatencyPolicies`  <a name="cfn-gamelift-gamesessionqueue-playerlatencypolicies"></a>
A collection of latency policies to apply when processing game sessions placement requests with player latency information\. Multiple policies are evaluated in order of the maximum latency value, starting with the lowest latency values\. With just one policy, the policy is enforced at the start of the game session placement for the duration period\. With multiple policies, each policy is enforced consecutively for its duration period\. For example, a queue might enforce a 60\-second policy followed by a 120\-second policy, and then no policy for the remainder of the placement\. A player latency policy must set a value for `MaximumIndividualPlayerLatencyMilliseconds`\. If none is set, this API request fails\.  
*Required*: No  
*Type*: List of [PlayerLatencyPolicy](aws-properties-gamelift-gamesessionqueue-playerlatencypolicy.md)  
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
                ]
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
      Destinations:
        # DestinationArn can be either an Alias arn or Fleet arn that you own
        - DestinationArn: "arn:aws:gamelift:us-west-2:012345678912:fleet/fleet-id"
        - DestinationArn: "arn:aws:gamelift:us-west-2:012345678912:alias/alias-id"
      PlayerLatencyPolicies:
        - MaximumIndividualPlayerLatencyMilliseconds: 1000
          PolicyDurationSeconds: 60
```

## See also<a name="aws-resource-gamelift-gamesessionqueue--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Using Multi\-Region Queues](https://docs.aws.amazon.com/gamelift/latest/developerguide/queues-intro.html) in the *Amazon GameLift Developer Guide*
+  [CreateGameSessionQueue](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateGameSessionQueue.html) in the *Amazon GameLift API Reference* 