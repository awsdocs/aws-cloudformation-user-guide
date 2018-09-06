# Amazon Elastic Compute Cloud SpotFleet FleetLaunchTemplateSpecification<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification"></a>

`FleetLaunchTemplateSpecification` is a property of the [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md) property that describes a launch template\.

## Syntax<a name="w3ab2c21c14d786b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-launchtemplateconfig-syntax.yaml"></a>

```
[LaunchTemplateId](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid): String
[LaunchTemplateName](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename): String
[Version](#cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version): String
```

## Properties<a name="w3ab2c21c14d786b7"></a>

`LaunchTemplateId`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\. You must specify either a template ID or a template name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-launchtemplatename"></a>
The name of the launch template\. You must specify either a template name or a template ID\.   
Minimum length of 3\. Maximum length of 128\. Names must match the following pattern: `[a-zA-Z0-9\(\)\.-/_]+`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Version`  <a name="cfn-ec2-spotfleet-fleetlaunchtemplatespecification-version"></a>
The version number\. By default, the default version of the launch template is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)