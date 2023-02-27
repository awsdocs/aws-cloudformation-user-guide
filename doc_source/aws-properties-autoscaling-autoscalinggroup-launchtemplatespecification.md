# AWS::AutoScaling::AutoScalingGroup LaunchTemplateSpecification<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification"></a>

Specifies a launch template to use when provisioning EC2 instances for an Auto Scaling group\.

You must specify the following:
+ The ID or the name of the launch template, but not both\.
+ The version of the launch template\.

`LaunchTemplateSpecification` is property of the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\. It is also a property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) and [AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides.html) property types\.

For information about creating a launch template, see [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) and [Create a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\.

For examples of launch templates, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html) and the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples) section in the `AWS::EC2::LaunchTemplate` resource\.

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
The ID of the launch template\.  
You must specify the `LaunchTemplateID` or the `LaunchTemplateName`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
You must specify the `LaunchTemplateName` or the `LaunchTemplateID`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version"></a>
The version number of the launch template\.  
Specifying `$Latest` or `$Default` for the template version number is not supported\. However, you can specify `LatestVersionNumber` or `DefaultVersionNumber` using the `Fn::GetAtt` intrinsic function\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.  
For an example of using the `Fn::GetAtt` function, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section of the `AWS::AutoScaling::AutoScalingGroup` resource\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification--seealso"></a>
+  [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) 
+  [AWS::EC2::LaunchTemplate BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-blockdevicemapping.html) 
+ [Required KMS key policy for use with encrypted volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/key-policy-requirements-EBS-encryption.html) in the *Amazon EC2 Auto Scaling User Guide*
+ [Use encryption with EBS\-backed AMIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*

