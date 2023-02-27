# AWS::GameLift::GameServerGroup AutoScalingPolicy<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy"></a>

 **This data type is used with the GameLift FleetIQ and game server groups\.** 

Configuration settings for intelligent automatic scaling that uses target tracking\. After the Auto Scaling group is created, all updates to Auto Scaling policies, including changing this policy and adding or removing other policies, is done directly on the Auto Scaling group\. 

## Syntax<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy-syntax.json"></a>

```
{
  "[EstimatedInstanceWarmup](#cfn-gamelift-gameservergroup-autoscalingpolicy-estimatedinstancewarmup)" : Double,
  "[TargetTrackingConfiguration](#cfn-gamelift-gameservergroup-autoscalingpolicy-targettrackingconfiguration)" : TargetTrackingConfiguration
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy-syntax.yaml"></a>

```
  [EstimatedInstanceWarmup](#cfn-gamelift-gameservergroup-autoscalingpolicy-estimatedinstancewarmup): Double
  [TargetTrackingConfiguration](#cfn-gamelift-gameservergroup-autoscalingpolicy-targettrackingconfiguration): 
    TargetTrackingConfiguration
```

## Properties<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy-properties"></a>

`EstimatedInstanceWarmup`  <a name="cfn-gamelift-gameservergroup-autoscalingpolicy-estimatedinstancewarmup"></a>
Length of time, in seconds, it takes for a new instance to start new game server processes and register with GameLift FleetIQ\. Specifying a warm\-up time can be useful, particularly with game servers that take a long time to start up, because it avoids prematurely starting new instances\.   
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingConfiguration`  <a name="cfn-gamelift-gameservergroup-autoscalingpolicy-targettrackingconfiguration"></a>
Settings for a target\-based scaling policy applied to Auto Scaling group\. These settings are used to create a target\-based policy that tracks the GameLift FleetIQ metric `PercentUtilizedGameServers` and specifies a target value for the metric\. As player usage changes, the policy triggers to adjust the game server group capacity so that the metric returns to the target value\.  
*Required*: Yes  
*Type*: [TargetTrackingConfiguration](aws-properties-gamelift-gameservergroup-targettrackingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)