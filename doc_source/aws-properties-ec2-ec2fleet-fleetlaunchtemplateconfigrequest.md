# Amazon EC2 EC2Fleet FleetLaunchTemplateConfigRequest<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest"></a>

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-description"></a>The `FleetLaunchTemplateConfigRequest` property type specifies a launch template and overrides for an EC2 Fleet\.

<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-inheritance"></a> `FleetLaunchTemplateConfigRequest` is a property of the [AWS::EC2::EC2Fleet](aws-resource-ec2-ec2fleet.md) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax.json"></a>

```
{
  "[LaunchTemplateSpecification](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification)" : [*FleetLaunchTemplateSpecificationRequest*](aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest.md),
  "[Overrides](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides)" : [ [*FleetLaunchTemplateOverridesRequest*](aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax.yaml"></a>

```
[LaunchTemplateSpecification](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification): 
  [*FleetLaunchTemplateSpecificationRequest*](aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest.md)
[Overrides](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides): 
  - [*FleetLaunchTemplateOverridesRequest*](aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest.md)
```

## Properties<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-properties"></a>

`LaunchTemplateSpecification`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification"></a>
The launch template to use\. You must specify either the launch template ID or launch template name in the request\.  
 *Required*: No  
 *Type*: [FleetLaunchTemplateSpecificationRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Overrides`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides"></a>
Any parameters that you specify override the same parameters in the launch template\.  
 *Required*: No  
 *Type*: List of [FleetLaunchTemplateOverridesRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-seealso"></a>
+ [FleetLaunchTemplateConfigRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateConfigRequest.html) in the *Amazon EC2 API Reference*