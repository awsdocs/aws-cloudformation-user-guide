# AWS::SageMaker::ModelPackage ModelDataQuality<a name="aws-properties-sagemaker-modelpackage-modeldataquality"></a>

Data quality constraints and statistics for a model\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-modeldataquality-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-modeldataquality-syntax.json"></a>

```
{
  "[Constraints](#cfn-sagemaker-modelpackage-modeldataquality-constraints)" : MetricsSource,
  "[Statistics](#cfn-sagemaker-modelpackage-modeldataquality-statistics)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-modeldataquality-syntax.yaml"></a>

```
  [Constraints](#cfn-sagemaker-modelpackage-modeldataquality-constraints): 
    MetricsSource
  [Statistics](#cfn-sagemaker-modelpackage-modeldataquality-statistics): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-modeldataquality-properties"></a>

`Constraints`  <a name="cfn-sagemaker-modelpackage-modeldataquality-constraints"></a>
Data quality constraints for a model\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statistics`  <a name="cfn-sagemaker-modelpackage-modeldataquality-statistics"></a>
Data quality statistics for a model\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)