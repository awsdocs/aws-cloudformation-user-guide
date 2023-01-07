# AWS::EMR::InstanceGroupConfig AutoScalingPolicy<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy"></a>

`AutoScalingPolicy` defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\. For more information, see [Using Automatic Scaling in Amazon EMR](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-automatic-scaling.html) in the *Amazon EMR Management Guide*\.

## Syntax<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-syntax.json"></a>

```
{
  "[Constraints](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints)" : ScalingConstraints,
  "[Rules](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules)" : [ ScalingRule, ... ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-syntax.yaml"></a>

```
  [Constraints](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints): 
    ScalingConstraints
  [Rules](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules): 
    - ScalingRule
```

## Properties<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-properties"></a>

`Constraints`  <a name="cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints"></a>
The upper and lower EC2 instance limits for an automatic scaling policy\. Automatic scaling activity will not cause an instance group to grow above or below these limits\.  
*Required*: Yes  
*Type*: [ScalingConstraints](aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules"></a>
The scale\-in and scale\-out rules that comprise the automatic scaling policy\.  
*Required*: Yes  
*Type*: List of [ScalingRule](aws-properties-elasticmapreduce-instancegroupconfig-scalingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)