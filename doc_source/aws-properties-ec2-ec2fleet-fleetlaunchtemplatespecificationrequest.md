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
The ID of the launch template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplatename"></a>
The name of the launch template\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-version"></a>
The version number of the launch template\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest--seealso"></a>
+  [ FleetLaunchTemplateSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateSpecificationRequest.html) in the *Amazon EC2 API Reference*

## Supported Regions

This PropertyType is supported by ***all*** regions.