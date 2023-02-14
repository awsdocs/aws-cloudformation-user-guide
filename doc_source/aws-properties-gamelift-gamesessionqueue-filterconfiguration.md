# AWS::GameLift::GameSessionQueue FilterConfiguration<a name="aws-properties-gamelift-gamesessionqueue-filterconfiguration"></a>

A list of fleet locations where a game session queue can place new game sessions\. You can use a filter to temporarily turn off placements for specific locations\. For queues that have multi\-location fleets, you can use a filter configuration allow placement with some, but not all of these locations\.

## Syntax<a name="aws-properties-gamelift-gamesessionqueue-filterconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gamesessionqueue-filterconfiguration-syntax.json"></a>

```
{
  "[AllowedLocations](#cfn-gamelift-gamesessionqueue-filterconfiguration-allowedlocations)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-gamelift-gamesessionqueue-filterconfiguration-syntax.yaml"></a>

```
  [AllowedLocations](#cfn-gamelift-gamesessionqueue-filterconfiguration-allowedlocations): 
    - String
```

## Properties<a name="aws-properties-gamelift-gamesessionqueue-filterconfiguration-properties"></a>

`AllowedLocations`  <a name="cfn-gamelift-gamesessionqueue-filterconfiguration-allowedlocations"></a>
 A list of locations to allow game session placement in, in the form of AWS Region codes such as `us-west-2`\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)