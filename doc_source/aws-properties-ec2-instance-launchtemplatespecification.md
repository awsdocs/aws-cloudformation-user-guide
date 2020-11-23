# AWS::EC2::Instance LaunchTemplateSpecification<a name="aws-properties-ec2-instance-launchtemplatespecification"></a>

Specifies a launch template\. You must specify either the launch template ID or launch template name\.

 `LaunchTemplateSpecification` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

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
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-instance-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-ec2-instance-launchtemplatespecification-version"></a>
The version number of the launch template\.AWS CloudFormation does not support specifying `$Latest`, or `$Default` for the template version number\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-instance-launchtemplatespecification--seealso"></a>
+  [ LaunchTemplateSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpecification.html) in the *Amazon EC2 API Reference* 