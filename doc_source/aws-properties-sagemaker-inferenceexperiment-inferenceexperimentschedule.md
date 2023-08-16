# AWS::SageMaker::InferenceExperiment InferenceExperimentSchedule<a name="aws-properties-sagemaker-inferenceexperiment-inferenceexperimentschedule"></a>

The start and end times of an inference experiment\.

The maximum duration that you can set for an inference experiment is 30 days\.

## Syntax<a name="aws-properties-sagemaker-inferenceexperiment-inferenceexperimentschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-inferenceexperiment-inferenceexperimentschedule-syntax.json"></a>

```
{
  "[EndTime](#cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-endtime)" : String,
  "[StartTime](#cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-starttime)" : String
}
```

### YAML<a name="aws-properties-sagemaker-inferenceexperiment-inferenceexperimentschedule-syntax.yaml"></a>

```
  [EndTime](#cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-endtime): String
  [StartTime](#cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-starttime): String
```

## Properties<a name="aws-properties-sagemaker-inferenceexperiment-inferenceexperimentschedule-properties"></a>

`EndTime`  <a name="cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-endtime"></a>
The timestamp at which the inference experiment ended or will end\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-sagemaker-inferenceexperiment-inferenceexperimentschedule-starttime"></a>
The timestamp at which the inference experiment started or will start\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)