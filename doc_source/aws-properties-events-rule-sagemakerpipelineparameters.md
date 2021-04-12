# AWS::Events::Rule SageMakerPipelineParameters<a name="aws-properties-events-rule-sagemakerpipelineparameters"></a>

Contains the SageMaker Model Building Pipeline parameters to start execution of a SageMaker Model Building Pipeline\.

If you specify a SageMaker Model Building Pipeline as a target, you can use this to specify parameters to start a pipeline execution based on EventBridge events\.

## Syntax<a name="aws-properties-events-rule-sagemakerpipelineparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-sagemakerpipelineparameters-syntax.json"></a>

```
{
  "[PipelineParameterList](#cfn-events-rule-sagemakerpipelineparameters-pipelineparameterlist)" : [ SageMakerPipelineParameter, ... ]
}
```

### YAML<a name="aws-properties-events-rule-sagemakerpipelineparameters-syntax.yaml"></a>

```
  [PipelineParameterList](#cfn-events-rule-sagemakerpipelineparameters-pipelineparameterlist): 
    - SageMakerPipelineParameter
```

## Properties<a name="aws-properties-events-rule-sagemakerpipelineparameters-properties"></a>

`PipelineParameterList`  <a name="cfn-events-rule-sagemakerpipelineparameters-pipelineparameterlist"></a>
List of Parameter names and values for SageMaker Model Building Pipeline execution\.  
*Required*: No  
*Type*: List of [SageMakerPipelineParameter](aws-properties-events-rule-sagemakerpipelineparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)