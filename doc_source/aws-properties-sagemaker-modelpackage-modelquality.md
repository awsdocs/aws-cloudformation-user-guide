# AWS::SageMaker::ModelPackage ModelQuality<a name="aws-properties-sagemaker-modelpackage-modelquality"></a>

Model quality statistics and constraints\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-modelquality-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-modelquality-syntax.json"></a>

```
{
  "[Constraints](#cfn-sagemaker-modelpackage-modelquality-constraints)" : MetricsSource,
  "[Statistics](#cfn-sagemaker-modelpackage-modelquality-statistics)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-modelquality-syntax.yaml"></a>

```
  [Constraints](#cfn-sagemaker-modelpackage-modelquality-constraints): 
    MetricsSource
  [Statistics](#cfn-sagemaker-modelpackage-modelquality-statistics): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-modelquality-properties"></a>

`Constraints`  <a name="cfn-sagemaker-modelpackage-modelquality-constraints"></a>
Model quality constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statistics`  <a name="cfn-sagemaker-modelpackage-modelquality-statistics"></a>
Model quality statistics\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)