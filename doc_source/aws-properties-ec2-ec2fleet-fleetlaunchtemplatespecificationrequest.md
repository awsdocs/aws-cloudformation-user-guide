# Amazon EC2 EC2Fleet FleetLaunchTemplateSpecificationRequest<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest"></a>

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-description"></a>The `FleetLaunchTemplateSpecificationRequest` property type specifies the launch template to use for an EC2 Fleet\. You must specify either the launch template ID or launch template name in the request\. 

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-inheritance"></a> `FleetLaunchTemplateSpecificationRequest` is a property of the [FleetLaunchTemplateConfigRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest.md) property type\.

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LaunchTemplateName`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-launchtemplatename"></a>
The name of the launch template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-version"></a>
The version number of the launch template\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest-seealso"></a>
+ [FleetLaunchTemplateSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateSpecificationRequest.html) in the *Amazon EC2 API Reference*