# AWS::SageMaker::ModelPackage DriftCheckModelQuality<a name="aws-properties-sagemaker-modelpackage-driftcheckmodelquality"></a>

Represents the drift check model quality baselines that can be used when the model monitor is set using the model package\. 

## Syntax<a name="aws-properties-sagemaker-modelpackage-driftcheckmodelquality-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-driftcheckmodelquality-syntax.json"></a>

```
{
  "[Constraints](#cfn-sagemaker-modelpackage-driftcheckmodelquality-constraints)" : MetricsSource,
  "[Statistics](#cfn-sagemaker-modelpackage-driftcheckmodelquality-statistics)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-driftcheckmodelquality-syntax.yaml"></a>

```
  [Constraints](#cfn-sagemaker-modelpackage-driftcheckmodelquality-constraints): 
    MetricsSource
  [Statistics](#cfn-sagemaker-modelpackage-driftcheckmodelquality-statistics): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-driftcheckmodelquality-properties"></a>

`Constraints`  <a name="cfn-sagemaker-modelpackage-driftcheckmodelquality-constraints"></a>
The drift check model quality constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statistics`  <a name="cfn-sagemaker-modelpackage-driftcheckmodelquality-statistics"></a>
The drift check model quality statistics\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)