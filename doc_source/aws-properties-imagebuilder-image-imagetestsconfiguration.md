# AWS::ImageBuilder::Image ImageTestsConfiguration<a name="aws-properties-imagebuilder-image-imagetestsconfiguration"></a>

The image tests configuration is the configuration of the image tests, which includes the test enablement status and timeout minutes\.

## Syntax<a name="aws-properties-imagebuilder-image-imagetestsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-image-imagetestsconfiguration-syntax.json"></a>

```
{
  "[ImageTestsEnabled](#cfn-imagebuilder-image-imagetestsconfiguration-imagetestsenabled)" : Boolean,
  "[TimeoutMinutes](#cfn-imagebuilder-image-imagetestsconfiguration-timeoutminutes)" : Integer
}
```

### YAML<a name="aws-properties-imagebuilder-image-imagetestsconfiguration-syntax.yaml"></a>

```
  [ImageTestsEnabled](#cfn-imagebuilder-image-imagetestsconfiguration-imagetestsenabled): Boolean
  [TimeoutMinutes](#cfn-imagebuilder-image-imagetestsconfiguration-timeoutminutes): Integer
```

## Properties<a name="aws-properties-imagebuilder-image-imagetestsconfiguration-properties"></a>

`ImageTestsEnabled`  <a name="cfn-imagebuilder-image-imagetestsconfiguration-imagetestsenabled"></a>
Defines if tests should be executed when building this image\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeoutMinutes`  <a name="cfn-imagebuilder-image-imagetestsconfiguration-timeoutminutes"></a>
The maximum time in minutes that tests are permitted to run\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `1440`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)