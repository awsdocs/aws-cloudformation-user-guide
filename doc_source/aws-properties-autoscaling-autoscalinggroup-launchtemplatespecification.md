# Amazon EC2 Auto Scaling AutoScalingGroup LaunchTemplateSpecification<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification"></a>

`LaunchTemplateSpecification` is a property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource that specifies the launch template to use to launch instances\.

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

## Properties<a name="w3ab2c21c14d104b7"></a>

`LaunchTemplateId`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\. You must specify either a template ID or a template name\.   
Minimum length of 1\. Maximum length of 255\. IDs must fit the following pattern:   
`[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\. You must specify either a template name or a template ID\.  
Minimum length of 3\. Maximum length of 128\. Names must fit the following pattern:   
`[a-zA-Z0-9\(\)\.-/_]+ `  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Version`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version"></a>
The version number\. AWS CloudFormation does not support specifying `$Latest`, or `$Default` for the template version number\.  
Minimum length of 1\. Maximum length of 255\. Versions must fit the following pattern:   
`[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]* `  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)