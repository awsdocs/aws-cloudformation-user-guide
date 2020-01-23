# AWS::AutoScaling::AutoScalingGroup LaunchTemplateSpecification<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification"></a>

 `LaunchTemplateSpecification` is a property of [AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) that specifies the launch template to use to launch instances\. 

For information about creating a launch template, see [Creating a Launch Template for an Auto Scaling Group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification-syntax.yaml"></a>

```
  [LaunchTemplateId](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplateid): String
  [LaunchTemplateName](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename): String
  [Version](#cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification-properties"></a>

`LaunchTemplateId`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\. You must specify either a template ID or a template name\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\. You must specify either a template name or a template ID\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.-/_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version"></a>
The version number\. AWS CloudFormation does not support specifying $Latest, or $Default for the template version number\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)