# AWS::ImageBuilder::Image ImageTestsConfiguration<a name="aws-properties-imagebuilder-image-imagetestsconfiguration"></a>

When you create an image or container recipe with Image Builder, you can add the build or test components that are used to create the final image\. You must have at least one build component to create a recipe, but test components are not required\. If you have added tests, they run after the image is created, to ensure that the target image is functional and can be used reliably for launching Amazon EC2 instances\.

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
Determines if tests should run after building the image\. Image Builder defaults to enable tests to run following the image build, before image distribution\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeoutMinutes`  <a name="cfn-imagebuilder-image-imagetestsconfiguration-timeoutminutes"></a>
The maximum time in minutes that tests are permitted to run\.  
The timeoutMinutes attribute is not currently active\. This value is ignored\.
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `1440`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)