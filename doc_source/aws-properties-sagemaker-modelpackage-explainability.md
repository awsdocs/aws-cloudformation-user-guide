# AWS::SageMaker::ModelPackage Explainability<a name="aws-properties-sagemaker-modelpackage-explainability"></a>

Contains explainability metrics for a model\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-explainability-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-explainability-syntax.json"></a>

```
{
  "[Report](#cfn-sagemaker-modelpackage-explainability-report)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-explainability-syntax.yaml"></a>

```
  [Report](#cfn-sagemaker-modelpackage-explainability-report): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-explainability-properties"></a>

`Report`  <a name="cfn-sagemaker-modelpackage-explainability-report"></a>
The explainability report for a model\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)