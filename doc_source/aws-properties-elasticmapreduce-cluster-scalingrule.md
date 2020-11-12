# AWS::EMR::Cluster ScalingRule<a name="aws-properties-elasticmapreduce-cluster-scalingrule"></a>

`ScalingRule` is a subproperty of the `AutoScalingPolicy` property type\. `ScalingRule` defines the scale\-in or scale\-out rules for scaling activity, including the CloudWatch metric alarm that triggers activity, how EC2 instances are added or removed, and the periodicity of adjustments\. The automatic scaling policy for an instance group can comprise one or more automatic scaling rules\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-scalingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-scalingrule-syntax.json"></a>

```
{
  "[Action](#cfn-elasticmapreduce-cluster-scalingrule-action)" : ScalingAction,
  "[Description](#cfn-elasticmapreduce-cluster-scalingrule-description)" : String,
  "[Name](#cfn-elasticmapreduce-cluster-scalingrule-name)" : String,
  "[Trigger](#cfn-elasticmapreduce-cluster-scalingrule-trigger)" : ScalingTrigger
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-scalingrule-syntax.yaml"></a>

```
  [Action](#cfn-elasticmapreduce-cluster-scalingrule-action): 
    ScalingAction
  [Description](#cfn-elasticmapreduce-cluster-scalingrule-description): String
  [Name](#cfn-elasticmapreduce-cluster-scalingrule-name): String
  [Trigger](#cfn-elasticmapreduce-cluster-scalingrule-trigger): 
    ScalingTrigger
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-scalingrule-properties"></a>

`Action`  <a name="cfn-elasticmapreduce-cluster-scalingrule-action"></a>
The conditions that trigger an automatic scaling activity\.  
*Required*: Yes  
*Type*: [ScalingAction](aws-properties-elasticmapreduce-cluster-scalingaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-elasticmapreduce-cluster-scalingrule-description"></a>
A friendly, more verbose description of the automatic scaling rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-elasticmapreduce-cluster-scalingrule-name"></a>
The name used to identify an automatic scaling rule\. Rule names must be unique within a scaling policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Trigger`  <a name="cfn-elasticmapreduce-cluster-scalingrule-trigger"></a>
The CloudWatch alarm definition that determines when automatic scaling activity is triggered\.  
*Required*: Yes  
*Type*: [ScalingTrigger](aws-properties-elasticmapreduce-cluster-scalingtrigger.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)