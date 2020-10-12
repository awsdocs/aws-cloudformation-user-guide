# AWS::EC2::EC2Fleet FleetLaunchTemplateSpecificationRequest<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest"></a>

Specifies the launch template to use for an EC2 Fleet\. You must specify either the launch template ID or launch template name in the request\.

 `FleetLaunchTemplateSpecificationRequest` is a property of the [ FleetLaunchTemplateConfigRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest.html) property type\.

## Syntax<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplatename)" : String,
  "[Version](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-version)" : String
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-syntax.yaml"></a>

```
  [LaunchTemplateId](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplateid): String
  [LaunchTemplateName](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplatename): String
  [Version](#cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-version): String
```

## Properties<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-properties"></a>

`LaunchTemplateId`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplateid"></a>
The ID of the launch template\. If you specify the template ID, you can't specify the template name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchTemplateName`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplatename"></a>
The name of the launch template\. If you specify the template name, you can't specify the template ID\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-version"></a>
The launch template version number, `$Latest`, or `$Default`\. You must specify a value, otherwise the request fails\.  
If the value is `$Latest`, Amazon EC2 uses the latest version of the launch template\.  
If the value is `$Default`, Amazon EC2 uses the default version of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest--seealso"></a>
+  [ FleetLaunchTemplateSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateSpecificationRequest.html) in the *Amazon EC2 API Reference*