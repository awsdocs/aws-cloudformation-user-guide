# AWS::EC2::Instance LaunchTemplateSpecification<a name="aws-properties-ec2-instance-launchtemplatespecification"></a>

Specifies a launch template to use when launching an Amazon EC2 instance\.

You must specify the following:
+ The ID or the name of the launch template, but not both\.
+ The version of the launch template\.

`LaunchTemplateSpecification` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

For information about creating a launch template, see [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) and [Create a launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html#create-launch-template) in the *Amazon EC2 User Guide*\.

For examples of launch templates, see [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples)\.

## Syntax<a name="aws-properties-ec2-instance-launchtemplatespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-launchtemplatespecification-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-ec2-instance-launchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-ec2-instance-launchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-ec2-instance-launchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-launchtemplatespecification-syntax.yaml"></a>

```
  [LaunchTemplateId](#cfn-ec2-instance-launchtemplatespecification-launchtemplateid): String
  [LaunchTemplateName](#cfn-ec2-instance-launchtemplatespecification-launchtemplatename): String
  [Version](#cfn-ec2-instance-launchtemplatespecification-version): String
```

## Properties<a name="aws-properties-ec2-instance-launchtemplatespecification-properties"></a>

`LaunchTemplateId`  <a name="cfn-ec2-instance-launchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\.  
You must specify the `LaunchTemplateId` or the `LaunchTemplateName`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-instance-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
You must specify the `LaunchTemplateName` or the `LaunchTemplateId`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-ec2-instance-launchtemplatespecification-version"></a>
The version number of the launch template\.  
Specifying `$Latest` or `$Default` for the template version number is not supported\. However, you can specify `LatestVersionNumber` or `DefaultVersionNumber` using the `Fn::GetAtt` intrinsic function\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate-return-values-fn--getatt)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-instance-launchtemplatespecification--seealso"></a>
+  [ LaunchTemplateSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpecification.html) in the *Amazon EC2 API Reference* 