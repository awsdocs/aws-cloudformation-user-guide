# AWS::SageMaker::ModelQualityJobDefinition StoppingCondition<a name="aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition"></a>

Specifies a limit to how long a model training or compilation job can run\. It also specifies how long you are willing to wait for a managed spot training job to complete\. When the job reaches the time limit, Amazon SageMaker ends the training or compilation job\. Use this API to cap model training costs\.

To stop a job, Amazon SageMaker sends the algorithm the `SIGTERM` signal, which delays job termination for 120 seconds\. Algorithms can use this 120\-second window to save the model artifacts, so the results of training are not lost\. 

The training algorithms provided by Amazon SageMaker automatically save the intermediate results of a model training job when possible\. This attempt to save artifacts is only a best effort case as model might not be in a state from which it can be saved\. For example, if training has just started, the model might not be ready to save\. When saved, this intermediate data is a valid model artifact\. You can use it to create a model with `CreateModel`\.

**Note**  
The Neural Topic Model \(NTM\) currently does not support saving intermediate model artifacts\. When training NTMs, make sure that the maximum runtime is sufficient for the training job to complete\.

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition-syntax.json"></a>

```
{
  "[MaxRuntimeInSeconds](#cfn-sagemaker-modelqualityjobdefinition-stoppingcondition-maxruntimeinseconds)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition-syntax.yaml"></a>

```
  [MaxRuntimeInSeconds](#cfn-sagemaker-modelqualityjobdefinition-stoppingcondition-maxruntimeinseconds): Integer
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition-properties"></a>

`MaxRuntimeInSeconds`  <a name="cfn-sagemaker-modelqualityjobdefinition-stoppingcondition-maxruntimeinseconds"></a>
The maximum length of time, in seconds, that the training or compilation job can run\. If job does not complete during this time, Amazon SageMaker ends the job\. If value is not specified, default value is 1 day\. The maximum value is 28 days\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)