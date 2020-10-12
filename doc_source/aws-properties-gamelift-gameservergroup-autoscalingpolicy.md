# AWS::GameLift::GameServerGroup AutoScalingPolicy<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy"></a>

Configuration settings for intelligent automatic scaling that uses target tracking\. An Auto Scaling policy can be specified when a new game server group is created\. This policy is passed to the associated Auto Scaling group\. The Auto Scaling group takes action based on this policy, as well as \(and potentially in conflict with\) other scaling policies that are separately applied to the Auto Scaling group\. 

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
Settings for a target\-based scaling policy applied to Auto Scaling group\. These settings are used to create a target\-based policy that tracks the GameLift FleetIQ metric `"PercentUtilizedGameServers"` and specifies a target value for the metric\. As player usage changes, the policy triggers to adjust the game server group capacity so that the metric returns to the target value\.   
*Required*: Yes  
*Type*: [TargetTrackingConfiguration](aws-properties-gamelift-gameservergroup-targettrackingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-gamelift-gameservergroup-autoscalingpolicy--seealso"></a>
+  [GameLift FleetIQ Guide](https://docs.aws.amazon.com/gamelift/latest/developerguide/gsg-intro.html) 