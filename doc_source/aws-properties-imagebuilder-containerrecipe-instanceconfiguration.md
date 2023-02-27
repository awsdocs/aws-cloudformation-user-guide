# AWS::ImageBuilder::ContainerRecipe InstanceConfiguration<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration"></a>

Defines a custom base AMI and block device mapping configurations of an instance used for building and testing container images\.

## Syntax<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration-syntax.json"></a>

```
{
  "[BlockDeviceMappings](#cfn-imagebuilder-containerrecipe-instanceconfiguration-blockdevicemappings)" : [ InstanceBlockDeviceMapping, ... ],
  "[Image](#cfn-imagebuilder-containerrecipe-instanceconfiguration-image)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration-syntax.yaml"></a>

```
  [BlockDeviceMappings](#cfn-imagebuilder-containerrecipe-instanceconfiguration-blockdevicemappings): 
    - InstanceBlockDeviceMapping
  [Image](#cfn-imagebuilder-containerrecipe-instanceconfiguration-image): String
```

## Properties<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration-properties"></a>

`BlockDeviceMappings`  <a name="cfn-imagebuilder-containerrecipe-instanceconfiguration-blockdevicemappings"></a>
Defines the block devices to attach for building an instance from this Image Builder AMI\.  
*Required*: No  
*Type*: List of [InstanceBlockDeviceMapping](aws-properties-imagebuilder-containerrecipe-instanceblockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Image`  <a name="cfn-imagebuilder-containerrecipe-instanceconfiguration-image"></a>
The AMI ID to use as the base image for a container build and test instance\. If not specified, Image Builder will use the appropriate ECS\-optimized AMI as a base image\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)