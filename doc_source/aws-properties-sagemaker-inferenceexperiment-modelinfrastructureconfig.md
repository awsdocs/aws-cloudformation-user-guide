# AWS::SageMaker::InferenceExperiment ModelInfrastructureConfig<a name="aws-properties-sagemaker-inferenceexperiment-modelinfrastructureconfig"></a>

The configuration for the infrastructure that the model will be deployed to\.

## Syntax<a name="aws-properties-sagemaker-inferenceexperiment-modelinfrastructureconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-inferenceexperiment-modelinfrastructureconfig-syntax.json"></a>

```
{
  "[InfrastructureType](#cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-infrastructuretype)" : String,
  "[RealTimeInferenceConfig](#cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-realtimeinferenceconfig)" : RealTimeInferenceConfig
}
```

### YAML<a name="aws-properties-sagemaker-inferenceexperiment-modelinfrastructureconfig-syntax.yaml"></a>

```
  [InfrastructureType](#cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-infrastructuretype): String
  [RealTimeInferenceConfig](#cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-realtimeinferenceconfig): 
    RealTimeInferenceConfig
```

## Properties<a name="aws-properties-sagemaker-inferenceexperiment-modelinfrastructureconfig-properties"></a>

`InfrastructureType`  <a name="cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-infrastructuretype"></a>
The inference option to which to deploy your model\. Possible values are the following:  
+  `RealTime`: Deploy to real\-time inference\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `RealTimeInference`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RealTimeInferenceConfig`  <a name="cfn-sagemaker-inferenceexperiment-modelinfrastructureconfig-realtimeinferenceconfig"></a>
The infrastructure configuration for deploying the model to real\-time inference\.  
*Required*: Yes  
*Type*: [RealTimeInferenceConfig](aws-properties-sagemaker-inferenceexperiment-realtimeinferenceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)