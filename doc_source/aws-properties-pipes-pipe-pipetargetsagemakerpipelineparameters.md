# AWS::Pipes::Pipe PipeTargetSageMakerPipelineParameters<a name="aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters"></a>

The parameters for using a SageMaker pipeline as a target\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters-syntax.json"></a>

```
{
  "[PipelineParameterList](#cfn-pipes-pipe-pipetargetsagemakerpipelineparameters-pipelineparameterlist)" : [ SageMakerPipelineParameter, ... ]
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters-syntax.yaml"></a>

```
  [PipelineParameterList](#cfn-pipes-pipe-pipetargetsagemakerpipelineparameters-pipelineparameterlist): 
    - SageMakerPipelineParameter
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters-properties"></a>

`PipelineParameterList`  <a name="cfn-pipes-pipe-pipetargetsagemakerpipelineparameters-pipelineparameterlist"></a>
List of Parameter names and values for SageMaker Model Building Pipeline execution\.  
*Required*: No  
*Type*: List of [SageMakerPipelineParameter](aws-properties-pipes-pipe-sagemakerpipelineparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)