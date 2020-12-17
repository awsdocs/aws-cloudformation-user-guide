# AWS::EC2::SpotFleet LaunchTemplateConfig<a name="aws-properties-ec2-spotfleet-launchtemplateconfig"></a>

Specifies a launch template and overrides\.

## Syntax<a name="aws-properties-ec2-spotfleet-launchtemplateconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-launchtemplateconfig-syntax.json"></a>

```
{
  "[LaunchTemplateSpecification](#cfn-ec2-spotfleet-launchtemplateconfig-launchtemplatespecification)" : FleetLaunchTemplateSpecification,
  "[Overrides](#cfn-ec2-spotfleet-launchtemplateconfig-overrides)" : [ LaunchTemplateOverrides, ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-launchtemplateconfig-syntax.yaml"></a>

```
  [LaunchTemplateSpecification](#cfn-ec2-spotfleet-launchtemplateconfig-launchtemplatespecification): 
    FleetLaunchTemplateSpecification
  [Overrides](#cfn-ec2-spotfleet-launchtemplateconfig-overrides): 
    - LaunchTemplateOverrides
```

## Properties<a name="aws-properties-ec2-spotfleet-launchtemplateconfig-properties"></a>

`LaunchTemplateSpecification`  <a name="cfn-ec2-spotfleet-launchtemplateconfig-launchtemplatespecification"></a>
The launch template\.  
*Required*: No  
*Type*: [FleetLaunchTemplateSpecification](aws-properties-ec2-spotfleet-fleetlaunchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overrides`  <a name="cfn-ec2-spotfleet-launchtemplateconfig-overrides"></a>
Any parameters that you specify override the same parameters in the launch template\.  
*Required*: No  
*Type*: List of [LaunchTemplateOverrides](aws-properties-ec2-spotfleet-launchtemplateoverrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)