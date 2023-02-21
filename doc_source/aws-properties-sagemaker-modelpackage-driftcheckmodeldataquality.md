# AWS::SageMaker::ModelPackage DriftCheckModelDataQuality<a name="aws-properties-sagemaker-modelpackage-driftcheckmodeldataquality"></a>

Represents the drift check data quality baselines that can be used when the model monitor is set using the model package\. 

## Syntax<a name="aws-properties-sagemaker-modelpackage-driftcheckmodeldataquality-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-driftcheckmodeldataquality-syntax.json"></a>

```
{
  "[Constraints](#cfn-sagemaker-modelpackage-driftcheckmodeldataquality-constraints)" : MetricsSource,
  "[Statistics](#cfn-sagemaker-modelpackage-driftcheckmodeldataquality-statistics)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-driftcheckmodeldataquality-syntax.yaml"></a>

```
  [Constraints](#cfn-sagemaker-modelpackage-driftcheckmodeldataquality-constraints): 
    MetricsSource
  [Statistics](#cfn-sagemaker-modelpackage-driftcheckmodeldataquality-statistics): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-driftcheckmodeldataquality-properties"></a>

`Constraints`  <a name="cfn-sagemaker-modelpackage-driftcheckmodeldataquality-constraints"></a>
The drift check model data quality constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statistics`  <a name="cfn-sagemaker-modelpackage-driftcheckmodeldataquality-statistics"></a>
The drift check model data quality statistics\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)