# AWS::SageMaker::ModelPackage Bias<a name="aws-properties-sagemaker-modelpackage-bias"></a>

Contains bias metrics for a model\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-bias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-bias-syntax.json"></a>

```
{
  "[PostTrainingReport](#cfn-sagemaker-modelpackage-bias-posttrainingreport)" : MetricsSource,
  "[PreTrainingReport](#cfn-sagemaker-modelpackage-bias-pretrainingreport)" : MetricsSource,
  "[Report](#cfn-sagemaker-modelpackage-bias-report)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-bias-syntax.yaml"></a>

```
  [PostTrainingReport](#cfn-sagemaker-modelpackage-bias-posttrainingreport): 
    MetricsSource
  [PreTrainingReport](#cfn-sagemaker-modelpackage-bias-pretrainingreport): 
    MetricsSource
  [Report](#cfn-sagemaker-modelpackage-bias-report): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-bias-properties"></a>

`PostTrainingReport`  <a name="cfn-sagemaker-modelpackage-bias-posttrainingreport"></a>
The post\-training bias report for a model\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreTrainingReport`  <a name="cfn-sagemaker-modelpackage-bias-pretrainingreport"></a>
The pre\-training bias report for a model\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Report`  <a name="cfn-sagemaker-modelpackage-bias-report"></a>
The bias report for a model  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)