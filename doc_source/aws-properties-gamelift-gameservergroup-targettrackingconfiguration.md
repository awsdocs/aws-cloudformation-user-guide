# AWS::GameLift::GameServerGroup TargetTrackingConfiguration<a name="aws-properties-gamelift-gameservergroup-targettrackingconfiguration"></a>

 **This data type is used with the Amazon GameLift FleetIQ and game server groups\.** 

Settings for a target\-based scaling policy as part of a `GameServerGroupAutoScalingPolicy`\. These settings are used to create a target\-based policy that tracks the GameLift FleetIQ metric `"PercentUtilizedGameServers"` and specifies a target value for the metric\. As player usage changes, the policy triggers to adjust the game server group capacity so that the metric returns to the target value\. 

## Syntax<a name="aws-properties-gamelift-gameservergroup-targettrackingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-targettrackingconfiguration-syntax.json"></a>

```
{
  "[TargetValue](#cfn-gamelift-gameservergroup-targettrackingconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-targettrackingconfiguration-syntax.yaml"></a>

```
  [TargetValue](#cfn-gamelift-gameservergroup-targettrackingconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-gamelift-gameservergroup-targettrackingconfiguration-properties"></a>

`TargetValue`  <a name="cfn-gamelift-gameservergroup-targettrackingconfiguration-targetvalue"></a>
Desired value to use with a game server group target\-based scaling policy\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)