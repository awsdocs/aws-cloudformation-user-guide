# AWS::AutoScaling::AutoScalingGroup LaunchTemplateSpecification<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification"></a>

The `LaunchTemplateSpecification` property specifies the Amazon EC2 launch template and the launch template version that can be used by an Auto Scaling group to configure Amazon EC2 instances\. 

The launch template that is specified must be configured for use with an Auto Scaling group\. For information about creating a launch template, see [Creating a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can find a sample template snippet in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section of the `AWS::AutoScaling::AutoScalingGroup` documentation\. 

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
The ID of the [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)\. You must specify either a `LaunchTemplateName` or a `LaunchTemplateId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-launchtemplatename"></a>
The name of the [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)\. You must specify either a `LaunchTemplateName` or a `LaunchTemplateId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplatespecification-version"></a>
The version number\. AWS CloudFormation does not support specifying $Latest, or $Default for the template version number\. However, you can specify `LatestVersionNumber` or `DefaultVersionNumber` using the `Fn::GetAtt` function\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate-return-values-fn--getatt) in the `AWS::EC2::LaunchTemplate` documentation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification--seealso"></a>
+ [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)
+ [AWS::EC2::LaunchTemplate BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-blockdevicemapping.html)
+ [Required CMK key policy for use with encrypted volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/key-policy-requirements-EBS-encryption.html) in the *Amazon EC2 Auto Scaling User Guide*
+ [Using encryption with EBS\-backed AMIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*

