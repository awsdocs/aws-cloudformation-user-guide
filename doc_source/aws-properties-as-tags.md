# AWS::AutoScaling::AutoScalingGroup TagProperty<a name="aws-properties-as-tags"></a>

 `TagProperty` specifies a list of tags for the `Tag` property of [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\. `TagProperty` adds tags to all associated instances in an Auto Scaling group\. 

For more information, see [Tagging Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\. You can find a sample template snippet in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section of the `AWS::AutoScaling::AutoScalingGroup` documentation\.

AWS CloudFormation adds the following tags to all Auto Scaling groups and associated instances: 
+ aws:cloudformation:stack\-name
+ aws:cloudformation:stack\-id
+ aws:cloudformation:logical\-id 

## Syntax<a name="aws-properties-as-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-tags-syntax.json"></a>

```
{
  "[Key](#cfn-as-tags-Key)" : String,
  "[PropagateAtLaunch](#cfn-as-tags-PropagateAtLaunch)" : Boolean,
  "[Value](#cfn-as-tags-Value)" : String
}
```

### YAML<a name="aws-properties-as-tags-syntax.yaml"></a>

```
  [Key](#cfn-as-tags-Key): String
  [PropagateAtLaunch](#cfn-as-tags-PropagateAtLaunch): Boolean
  [Value](#cfn-as-tags-Value): String
```

## Properties<a name="aws-properties-as-tags-properties"></a>

`Key`  <a name="cfn-as-tags-Key"></a>
The tag key\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropagateAtLaunch`  <a name="cfn-as-tags-PropagateAtLaunch"></a>
Set to `true` if you want AWS CloudFormation to copy the tag to EC2 instances that are launched as part of the Auto Scaling group\. Set to `false` if you want the tag attached only to the Auto Scaling group and not copied to any instances launched as part of the Auto Scaling group\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-as-tags-Value"></a>
The tag value\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)