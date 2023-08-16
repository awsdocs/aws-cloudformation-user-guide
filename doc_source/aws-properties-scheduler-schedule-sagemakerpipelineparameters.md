# AWS::Scheduler::Schedule SageMakerPipelineParameters<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameters"></a>

The templated target type for the Amazon SageMaker [https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_StartPipelineExecution.html](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_StartPipelineExecution.html) API operation\.

## Syntax<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameters-syntax.json"></a>

```
{
  "[PipelineParameterList](#cfn-scheduler-schedule-sagemakerpipelineparameters-pipelineparameterlist)" : [ SageMakerPipelineParameter, ... ]
}
```

### YAML<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameters-syntax.yaml"></a>

```
  [PipelineParameterList](#cfn-scheduler-schedule-sagemakerpipelineparameters-pipelineparameterlist): 
    - SageMakerPipelineParameter
```

## Properties<a name="aws-properties-scheduler-schedule-sagemakerpipelineparameters-properties"></a>

`PipelineParameterList`  <a name="cfn-scheduler-schedule-sagemakerpipelineparameters-pipelineparameterlist"></a>
List of parameter names and values to use when executing the SageMaker Model Building Pipeline\.  
*Required*: No  
*Type*: List of [SageMakerPipelineParameter](aws-properties-scheduler-schedule-sagemakerpipelineparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)