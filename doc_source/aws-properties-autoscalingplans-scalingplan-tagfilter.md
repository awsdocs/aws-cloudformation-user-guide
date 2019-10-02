# AWS::AutoScalingPlans::ScalingPlan TagFilter<a name="aws-properties-autoscalingplans-scalingplan-tagfilter"></a>

 `TagFilter` is a subproperty of [ApplicationSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-applicationsource.html) that specifies a tag for an application source to use with AWS Auto Scaling\. 

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax.json"></a>

```
{
  "[Key](#cfn-autoscalingplans-scalingplan-tagfilter-key)" : String,
  "[Values](#cfn-autoscalingplans-scalingplan-tagfilter-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-syntax.yaml"></a>

```
  [Key](#cfn-autoscalingplans-scalingplan-tagfilter-key): String
  [Values](#cfn-autoscalingplans-scalingplan-tagfilter-values): 
    - String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-tagfilter-properties"></a>

`Key`  <a name="cfn-autoscalingplans-scalingplan-tagfilter-key"></a>
The tag key\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-autoscalingplans-scalingplan-tagfilter-values"></a>
The tag values \(0 to 20\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-autoscalingplans-scalingplan-tagfilter--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
