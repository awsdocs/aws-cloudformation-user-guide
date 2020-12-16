# AWS::EC2::EC2Fleet FleetLaunchTemplateConfigRequest<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest"></a>

Specifies a launch template and overrides for an EC2 Fleet\.

 `FleetLaunchTemplateConfigRequest` is a property of the [AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax.json"></a>

```
{
  "[LaunchTemplateSpecification](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification)" : FleetLaunchTemplateSpecificationRequest,
  "[Overrides](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides)" : [ FleetLaunchTemplateOverridesRequest, ... ]
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-syntax.yaml"></a>

```
  [LaunchTemplateSpecification](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification): 
    FleetLaunchTemplateSpecificationRequest
  [Overrides](#cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides): 
    - FleetLaunchTemplateOverridesRequest
```

## Properties<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-properties"></a>

`LaunchTemplateSpecification`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-launchtemplatespecification"></a>
The launch template to use\. You must specify either the launch template ID or launch template name in the request\.   
*Required*: No  
*Type*: [FleetLaunchTemplateSpecificationRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplatespecificationrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Overrides`  <a name="cfn-ec2-ec2fleet-fleetlaunchtemplateconfigrequest-overrides"></a>
Any parameters that you specify override the same parameters in the launch template\.  
*Required*: No  
*Type*: List of [FleetLaunchTemplateOverridesRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplateoverridesrequest.md)  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest--seealso"></a>
+  [ FleetLaunchTemplateConfigRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_FleetLaunchTemplateConfigRequest.html) in the *Amazon EC2 API Reference* 