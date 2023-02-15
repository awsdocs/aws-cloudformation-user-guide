# AWS::EC2::SpotFleet FleetLaunchTemplateSpecification<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification"></a>

Specifies the launch template to be used by the Spot Fleet request for configuring Amazon EC2 instances\.

You must specify the following:
+ The ID or the name of the launch template, but not both\.
+ The version of the launch template\.

`FleetLaunchTemplateSpecification` is a property of the [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html) resource\.

For information about creating a launch template, see [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) and [Create a launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html#create-launch-template) in the *Amazon EC2 User Guide*\.

For examples of launch templates, see [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples)\.

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
The ID of the launch template\.  
You must specify the `LaunchTemplateId` or the `LaunchTemplateName`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplateName`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename"></a>
The name of the launch template\.  
You must specify the `LaunchTemplateName` or the `LaunchTemplateId`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version"></a>
The version number of the launch template\.  
Specifying `$Latest` or `$Default` for the template version number is not supported\. However, you can specify `LatestVersionNumber` or `DefaultVersionNumber` using the `Fn::GetAtt` intrinsic function\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate-return-values-fn--getatt)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)