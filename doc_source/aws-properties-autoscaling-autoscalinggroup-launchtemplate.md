# AWS::AutoScaling::AutoScalingGroup LaunchTemplate<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate"></a>

 `LaunchTemplate` is a property of the [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html) property type that describes a launch template and overrides\. The overrides are used to override the instance type specified by the launch template with multiple instance types that can be used to launch On\-Demand Instances and Spot Instances\. 

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax.json"></a>

```
{
  "[LaunchTemplateSpecification](#cfn-as-group-launchtemplate-launchtemplatespecification)" : LaunchTemplateSpecification,
  "[Overrides](#cfn-as-group-launchtemplate-overrides)" : [ LaunchTemplateOverrides, ... ]
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-syntax.yaml"></a>

```
  [LaunchTemplateSpecification](#cfn-as-group-launchtemplate-launchtemplatespecification): 
    LaunchTemplateSpecification
  [Overrides](#cfn-as-group-launchtemplate-overrides): 
    - LaunchTemplateOverrides
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplate-properties"></a>

`LaunchTemplateSpecification`  <a name="cfn-as-group-launchtemplate-launchtemplatespecification"></a>
The EC2 launch template to use\.  
*Required*: Yes  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overrides`  <a name="cfn-as-group-launchtemplate-overrides"></a>
Any properties that you specify override the same properties in the launch template\. The maximum number of instance types that can be associated with an Auto Scaling group is 40\. The maximum number of distinct launch templates you can define for an Auto Scaling group is 20\. For more information about configuring overrides, see [Configuring overrides](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-override-options.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
If not provided, Amazon EC2 Auto Scaling will use the instance type specified in the launch template to launch instances\.   
*Required*: No  
*Type*: List of [LaunchTemplateOverrides](aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)