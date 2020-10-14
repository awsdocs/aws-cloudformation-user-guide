# AWS::ImageBuilder::ImagePipeline ImageTestsConfiguration<a name="aws-properties-imagebuilder-imagepipeline-imagetestsconfiguration"></a>

The image pipeline image tests configuration is the configuration of the image tests, which includes the test enablement status and timeout minutes\.

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
*Required*: No  
*Type*: Integer  
*Minimum*: `60`  
*Maximum*: `1440`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)