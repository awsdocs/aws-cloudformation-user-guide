# AWS::ImageBuilder::ContainerRecipe InstanceConfiguration<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration"></a>

<a name="aws-properties-imagebuilder-containerrecipe-instanceconfiguration-description"></a>The `InstanceConfiguration` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::ImageBuilder::ContainerRecipe](aws-resource-imagebuilder-containerrecipe.md)\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [InstanceBlockDeviceMapping](aws-properties-imagebuilder-containerrecipe-instanceblockdevicemapping.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Image`  <a name="cfn-imagebuilder-containerrecipe-instanceconfiguration-image"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)