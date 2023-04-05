# AWS::ImageBuilder::ImagePipeline ImageScanningConfiguration<a name="aws-properties-imagebuilder-imagepipeline-imagescanningconfiguration"></a>

Contains settings for Image Builder image resource and container image scans\.

## Syntax<a name="aws-properties-imagebuilder-imagepipeline-imagescanningconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagepipeline-imagescanningconfiguration-syntax.json"></a>

```
{
  "[EcrConfiguration](#cfn-imagebuilder-imagepipeline-imagescanningconfiguration-ecrconfiguration)" : EcrConfiguration,
  "[ImageScanningEnabled](#cfn-imagebuilder-imagepipeline-imagescanningconfiguration-imagescanningenabled)" : Boolean
}
```

### YAML<a name="aws-properties-imagebuilder-imagepipeline-imagescanningconfiguration-syntax.yaml"></a>

```
  [EcrConfiguration](#cfn-imagebuilder-imagepipeline-imagescanningconfiguration-ecrconfiguration): 
    EcrConfiguration
  [ImageScanningEnabled](#cfn-imagebuilder-imagepipeline-imagescanningconfiguration-imagescanningenabled): Boolean
```

## Properties<a name="aws-properties-imagebuilder-imagepipeline-imagescanningconfiguration-properties"></a>

`EcrConfiguration`  <a name="cfn-imagebuilder-imagepipeline-imagescanningconfiguration-ecrconfiguration"></a>
Contains Amazon ECR settings for vulnerability scans\.  
*Required*: No  
*Type*: [EcrConfiguration](aws-properties-imagebuilder-imagepipeline-ecrconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageScanningEnabled`  <a name="cfn-imagebuilder-imagepipeline-imagescanningconfiguration-imagescanningenabled"></a>
A setting that indicates whether Image Builder keeps a snapshot of the vulnerability scans that Amazon Inspector runs against the build instance when you create a new image\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)