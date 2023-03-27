# AWS::Pipes::Pipe PipeTargetParameters<a name="aws-properties-pipes-pipe-pipetargetparameters"></a>

The parameters required to set up a target for your pipe\.

For more information about pipe target parameters, including how to use dynamic path parameters, see [Target parameters](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-pipes-event-target.html) in the *Amazon EventBridge User Guide*\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetparameters-syntax.json"></a>

```
{
  "[BatchJobParameters](#cfn-pipes-pipe-pipetargetparameters-batchjobparameters)" : PipeTargetBatchJobParameters,
  "[CloudWatchLogsParameters](#cfn-pipes-pipe-pipetargetparameters-cloudwatchlogsparameters)" : PipeTargetCloudWatchLogsParameters,
  "[EcsTaskParameters](#cfn-pipes-pipe-pipetargetparameters-ecstaskparameters)" : PipeTargetEcsTaskParameters,
  "[EventBridgeEventBusParameters](#cfn-pipes-pipe-pipetargetparameters-eventbridgeeventbusparameters)" : PipeTargetEventBridgeEventBusParameters,
  "[HttpParameters](#cfn-pipes-pipe-pipetargetparameters-httpparameters)" : PipeTargetHttpParameters,
  "[InputTemplate](#cfn-pipes-pipe-pipetargetparameters-inputtemplate)" : String,
  "[KinesisStreamParameters](#cfn-pipes-pipe-pipetargetparameters-kinesisstreamparameters)" : PipeTargetKinesisStreamParameters,
  "[LambdaFunctionParameters](#cfn-pipes-pipe-pipetargetparameters-lambdafunctionparameters)" : PipeTargetLambdaFunctionParameters,
  "[RedshiftDataParameters](#cfn-pipes-pipe-pipetargetparameters-redshiftdataparameters)" : PipeTargetRedshiftDataParameters,
  "[SageMakerPipelineParameters](#cfn-pipes-pipe-pipetargetparameters-sagemakerpipelineparameters)" : PipeTargetSageMakerPipelineParameters,
  "[SqsQueueParameters](#cfn-pipes-pipe-pipetargetparameters-sqsqueueparameters)" : PipeTargetSqsQueueParameters,
  "[StepFunctionStateMachineParameters](#cfn-pipes-pipe-pipetargetparameters-stepfunctionstatemachineparameters)" : PipeTargetStateMachineParameters
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetparameters-syntax.yaml"></a>

```
  [BatchJobParameters](#cfn-pipes-pipe-pipetargetparameters-batchjobparameters): 
    PipeTargetBatchJobParameters
  [CloudWatchLogsParameters](#cfn-pipes-pipe-pipetargetparameters-cloudwatchlogsparameters): 
    PipeTargetCloudWatchLogsParameters
  [EcsTaskParameters](#cfn-pipes-pipe-pipetargetparameters-ecstaskparameters): 
    PipeTargetEcsTaskParameters
  [EventBridgeEventBusParameters](#cfn-pipes-pipe-pipetargetparameters-eventbridgeeventbusparameters): 
    PipeTargetEventBridgeEventBusParameters
  [HttpParameters](#cfn-pipes-pipe-pipetargetparameters-httpparameters): 
    PipeTargetHttpParameters
  [InputTemplate](#cfn-pipes-pipe-pipetargetparameters-inputtemplate): String
  [KinesisStreamParameters](#cfn-pipes-pipe-pipetargetparameters-kinesisstreamparameters): 
    PipeTargetKinesisStreamParameters
  [LambdaFunctionParameters](#cfn-pipes-pipe-pipetargetparameters-lambdafunctionparameters): 
    PipeTargetLambdaFunctionParameters
  [RedshiftDataParameters](#cfn-pipes-pipe-pipetargetparameters-redshiftdataparameters): 
    PipeTargetRedshiftDataParameters
  [SageMakerPipelineParameters](#cfn-pipes-pipe-pipetargetparameters-sagemakerpipelineparameters): 
    PipeTargetSageMakerPipelineParameters
  [SqsQueueParameters](#cfn-pipes-pipe-pipetargetparameters-sqsqueueparameters): 
    PipeTargetSqsQueueParameters
  [StepFunctionStateMachineParameters](#cfn-pipes-pipe-pipetargetparameters-stepfunctionstatemachineparameters): 
    PipeTargetStateMachineParameters
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetparameters-properties"></a>

`BatchJobParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-batchjobparameters"></a>
The parameters for using an AWS Batch job as a target\.  
*Required*: No  
*Type*: [PipeTargetBatchJobParameters](aws-properties-pipes-pipe-pipetargetbatchjobparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchLogsParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-cloudwatchlogsparameters"></a>
The parameters for using an CloudWatch Logs log stream as a target\.  
*Required*: No  
*Type*: [PipeTargetCloudWatchLogsParameters](aws-properties-pipes-pipe-pipetargetcloudwatchlogsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcsTaskParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-ecstaskparameters"></a>
The parameters for using an Amazon ECS task as a target\.  
*Required*: No  
*Type*: [PipeTargetEcsTaskParameters](aws-properties-pipes-pipe-pipetargetecstaskparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBridgeEventBusParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-eventbridgeeventbusparameters"></a>
The parameters for using an EventBridge event bus as a target\.  
*Required*: No  
*Type*: [PipeTargetEventBridgeEventBusParameters](aws-properties-pipes-pipe-pipetargeteventbridgeeventbusparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-httpparameters"></a>
These are custom parameter to be used when the target is an API Gateway REST APIs or EventBridge ApiDestinations\.  
*Required*: No  
*Type*: [PipeTargetHttpParameters](aws-properties-pipes-pipe-pipetargethttpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputTemplate`  <a name="cfn-pipes-pipe-pipetargetparameters-inputtemplate"></a>
Valid JSON text passed to the target\. In this case, nothing from the event itself is passed to the target\. For more information, see [The JavaScript Object Notation \(JSON\) Data Interchange Format](http://www.rfc-editor.org/rfc/rfc7159.txt)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-kinesisstreamparameters"></a>
The parameters for using a Kinesis stream as a source\.  
*Required*: No  
*Type*: [PipeTargetKinesisStreamParameters](aws-properties-pipes-pipe-pipetargetkinesisstreamparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaFunctionParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-lambdafunctionparameters"></a>
The parameters for using a Lambda function as a target\.  
*Required*: No  
*Type*: [PipeTargetLambdaFunctionParameters](aws-properties-pipes-pipe-pipetargetlambdafunctionparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftDataParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-redshiftdataparameters"></a>
These are custom parameters to be used when the target is a Amazon Redshift cluster to invoke the Amazon Redshift Data API BatchExecuteStatement\.  
*Required*: No  
*Type*: [PipeTargetRedshiftDataParameters](aws-properties-pipes-pipe-pipetargetredshiftdataparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SageMakerPipelineParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-sagemakerpipelineparameters"></a>
The parameters for using a SageMaker pipeline as a target\.  
*Required*: No  
*Type*: [PipeTargetSageMakerPipelineParameters](aws-properties-pipes-pipe-pipetargetsagemakerpipelineparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqsQueueParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-sqsqueueparameters"></a>
The parameters for using a Amazon SQS stream as a source\.  
*Required*: No  
*Type*: [PipeTargetSqsQueueParameters](aws-properties-pipes-pipe-pipetargetsqsqueueparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepFunctionStateMachineParameters`  <a name="cfn-pipes-pipe-pipetargetparameters-stepfunctionstatemachineparameters"></a>
The parameters for using a Step Functions state machine as a target\.  
*Required*: No  
*Type*: [PipeTargetStateMachineParameters](aws-properties-pipes-pipe-pipetargetstatemachineparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)