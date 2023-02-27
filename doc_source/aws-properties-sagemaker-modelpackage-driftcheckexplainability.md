# AWS::SageMaker::ModelPackage DriftCheckExplainability<a name="aws-properties-sagemaker-modelpackage-driftcheckexplainability"></a>

Represents the drift check explainability baselines that can be used when the model monitor is set using the model package\. 

## Syntax<a name="aws-properties-sagemaker-modelpackage-driftcheckexplainability-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-driftcheckexplainability-syntax.json"></a>

```
{
  "[ConfigFile](#cfn-sagemaker-modelpackage-driftcheckexplainability-configfile)" : FileSource,
  "[Constraints](#cfn-sagemaker-modelpackage-driftcheckexplainability-constraints)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-driftcheckexplainability-syntax.yaml"></a>

```
  [ConfigFile](#cfn-sagemaker-modelpackage-driftcheckexplainability-configfile): 
    FileSource
  [Constraints](#cfn-sagemaker-modelpackage-driftcheckexplainability-constraints): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-driftcheckexplainability-properties"></a>

`ConfigFile`  <a name="cfn-sagemaker-modelpackage-driftcheckexplainability-configfile"></a>
The explainability config file for the model\.  
*Required*: No  
*Type*: [FileSource](aws-properties-sagemaker-modelpackage-filesource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Constraints`  <a name="cfn-sagemaker-modelpackage-driftcheckexplainability-constraints"></a>
The drift check explainability constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)