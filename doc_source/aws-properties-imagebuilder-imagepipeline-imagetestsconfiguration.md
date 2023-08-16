# AWS::ImageBuilder::ImagePipeline ImageTestsConfiguration<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration"></a>

When you create an image or container recipe with Image Builder, you can add the build or test components that your image pipeline uses to create the final image\. You must have at least one build component to create a recipe, but test components are not required\. Your pipeline runs tests after it builds the image, to ensure that the target image is functional and can be used reliably for launching Amazon EC2 instances\.

## Syntax<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration-syntax.json"></a>

```
{
  "[ImageTestsEnabled](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration-imagetestsenabled)" : Boolean,
  "[TimeoutMinutes](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration-timeoutminutes)" : Integer
}
```

### YAML<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration-syntax.yaml"></a>

```
  [ImageTestsEnabled](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration-imagetestsenabled): Boolean
  [TimeoutMinutes](#cfn-imagebuilder-imagepipeline-imagetestsconfiguration-timeoutminutes): Integer
```

## Properties<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration-properties"></a>

`ImageTestsEnabled`  <a name="cfn-imagebuilder-imagepipeline-imagetestsconfiguration-imagetestsenabled"></a>
Defines if tests should be executed when building this image\. For example, `true` or `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutMinutes`  <a name="cfn-imagebuilder-imagepipeline-imagetestsconfiguration-timeoutminutes"></a>
The maximum time in minutes that tests are permitted to run\.  
The timeoutMinutes attribute is not currently active\. This value is ignored\.
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `1440`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)