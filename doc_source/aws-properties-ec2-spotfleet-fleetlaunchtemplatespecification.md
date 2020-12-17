# AWS::EC2::SpotFleet FleetLaunchTemplateSpecification<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification"></a>

Describes the Amazon EC2 launch template and the launch template version that can be used by a Spot Fleet request to configure Amazon EC2 instances\. For information about launch templates, see [Launching an instance from a launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification-syntax.yaml"></a>

```
  [LaunchTemplateId](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid): String
  [LaunchTemplateName](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename): String
  [Version](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version): String
```

## Properties<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification-properties"></a>

`LaunchTemplateId`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\. If you specify the template ID, you can't specify the template name\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename"></a>
The name of the launch template\. You must specify either a template name or a template ID\.  
Minimum length of 3\. Maximum length of 128\. Names must match the following pattern: `[a-zA-Z0-9\(\)\.-/_]+`  
*Required*: Conditional  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version"></a>
The version number of the launch template\. You must specify a version number\. AWS CloudFormation does not support specifying `$Latest` or `$Default` for the template version number\.  
Minimum length of 1\. Maximum length of 255\. Versions must fit the following pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)