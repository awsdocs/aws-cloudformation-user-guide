# AWS::SageMaker::ModelPackage DriftCheckBias<a name="aws-properties-sagemaker-modelpackage-driftcheckbias"></a>

Represents the drift check bias baselines that can be used when the model monitor is set using the model package\.

## Syntax<a name="aws-properties-sagemaker-modelpackage-driftcheckbias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelpackage-driftcheckbias-syntax.json"></a>

```
{
  "[ConfigFile](#cfn-sagemaker-modelpackage-driftcheckbias-configfile)" : FileSource,
  "[PostTrainingConstraints](#cfn-sagemaker-modelpackage-driftcheckbias-posttrainingconstraints)" : MetricsSource,
  "[PreTrainingConstraints](#cfn-sagemaker-modelpackage-driftcheckbias-pretrainingconstraints)" : MetricsSource
}
```

### YAML<a name="aws-properties-sagemaker-modelpackage-driftcheckbias-syntax.yaml"></a>

```
  [ConfigFile](#cfn-sagemaker-modelpackage-driftcheckbias-configfile): 
    FileSource
  [PostTrainingConstraints](#cfn-sagemaker-modelpackage-driftcheckbias-posttrainingconstraints): 
    MetricsSource
  [PreTrainingConstraints](#cfn-sagemaker-modelpackage-driftcheckbias-pretrainingconstraints): 
    MetricsSource
```

## Properties<a name="aws-properties-sagemaker-modelpackage-driftcheckbias-properties"></a>

`ConfigFile`  <a name="cfn-sagemaker-modelpackage-driftcheckbias-configfile"></a>
The bias config file for a model\.  
*Required*: No  
*Type*: [FileSource](aws-properties-sagemaker-modelpackage-filesource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PostTrainingConstraints`  <a name="cfn-sagemaker-modelpackage-driftcheckbias-posttrainingconstraints"></a>
The post\-training constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreTrainingConstraints`  <a name="cfn-sagemaker-modelpackage-driftcheckbias-pretrainingconstraints"></a>
The pre\-training constraints\.  
*Required*: No  
*Type*: [MetricsSource](aws-properties-sagemaker-modelpackage-metricssource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)