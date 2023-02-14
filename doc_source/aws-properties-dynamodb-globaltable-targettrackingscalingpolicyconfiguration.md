# AWS::DynamoDB::GlobalTable TargetTrackingScalingPolicyConfiguration<a name="aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration"></a>

Defines a target tracking scaling policy\.

## Syntax<a name="aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-syntax.json"></a>

```
{
  "[DisableScaleIn](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-disablescalein)" : Boolean,
  "[ScaleInCooldown](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleincooldown)" : Integer,
  "[ScaleOutCooldown](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleoutcooldown)" : Integer,
  "[TargetValue](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-targetvalue)" : Double
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-syntax.yaml"></a>

```
  [DisableScaleIn](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-disablescalein): Boolean
  [ScaleInCooldown](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleincooldown): Integer
  [ScaleOutCooldown](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleoutcooldown): Integer
  [TargetValue](#cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-targetvalue): Double
```

## Properties<a name="aws-properties-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-properties"></a>

`DisableScaleIn`  <a name="cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-disablescalein"></a>
Indicates whether scale in by the target tracking scaling policy is disabled\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleInCooldown`  <a name="cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleincooldown"></a>
The amount of time, in seconds, after a scale\-in activity completes before another scale\-in activity can start\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleOutCooldown`  <a name="cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-scaleoutcooldown"></a>
The amount of time, in seconds, after a scale\-out activity completes before another scale\-out activity can start\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-dynamodb-globaltable-targettrackingscalingpolicyconfiguration-targetvalue"></a>
Defines a target value for the scaling policy\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)