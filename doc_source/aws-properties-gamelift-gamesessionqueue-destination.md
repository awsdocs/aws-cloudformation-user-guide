# AWS::GameLift::GameSessionQueue Destination<a name="aws-properties-gamelift-gamesessionqueue-destination"></a>

A fleet or alias designated in a game session queue\. Queues fulfill requests for new game sessions by placing a new game session on any of the queue's destinations\. 

## Syntax<a name="aws-properties-gamelift-gamesessionqueue-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gamesessionqueue-destination-syntax.json"></a>

```
{
  "[DestinationArn](#cfn-gamelift-gamesessionqueue-destination-destinationarn)" : String
}
```

### YAML<a name="aws-properties-gamelift-gamesessionqueue-destination-syntax.yaml"></a>

```
  [DestinationArn](#cfn-gamelift-gamesessionqueue-destination-destinationarn): String
```

## Properties<a name="aws-properties-gamelift-gamesessionqueue-destination-properties"></a>

`DestinationArn`  <a name="cfn-gamelift-gamesessionqueue-destination-destinationarn"></a>
The Amazon Resource Name \(ARN\) that is assigned to fleet or fleet alias\. ARNs, which include a fleet ID or alias ID and a Region name, provide a unique identifier across all Regions\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9:/-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-gamesessionqueue-destination--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Create a queue](https://docs.aws.amazon.com/gamelift/latest/developerguide/queues-creating.html) in the *Amazon GameLift Developer Guide*
+ [GameSessionQueueDestination](https://docs.aws.amazon.com/gamelift/latest/apireference/API_GameSessionQueueDestination.html) in the *Amazon GameLift API Reference*