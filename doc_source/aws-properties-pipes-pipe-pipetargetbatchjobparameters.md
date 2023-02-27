# AWS::Pipes::Pipe PipeTargetBatchJobParameters<a name="aws-properties-pipes-pipe-pipetargetbatchjobparameters"></a>

The parameters for using an AWS Batch job as a target\.

## Syntax<a name="aws-properties-pipes-pipe-pipetargetbatchjobparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipetargetbatchjobparameters-syntax.json"></a>

```
{
  "[ArrayProperties](#cfn-pipes-pipe-pipetargetbatchjobparameters-arrayproperties)" : BatchArrayProperties,
  "[ContainerOverrides](#cfn-pipes-pipe-pipetargetbatchjobparameters-containeroverrides)" : BatchContainerOverrides,
  "[DependsOn](#cfn-pipes-pipe-pipetargetbatchjobparameters-dependson)" : [ BatchJobDependency, ... ],
  "[JobDefinition](#cfn-pipes-pipe-pipetargetbatchjobparameters-jobdefinition)" : String,
  "[JobName](#cfn-pipes-pipe-pipetargetbatchjobparameters-jobname)" : String,
  "[Parameters](#cfn-pipes-pipe-pipetargetbatchjobparameters-parameters)" : {Key : Value, ...},
  "[RetryStrategy](#cfn-pipes-pipe-pipetargetbatchjobparameters-retrystrategy)" : BatchRetryStrategy
}
```

### YAML<a name="aws-properties-pipes-pipe-pipetargetbatchjobparameters-syntax.yaml"></a>

```
  [ArrayProperties](#cfn-pipes-pipe-pipetargetbatchjobparameters-arrayproperties): 
    BatchArrayProperties
  [ContainerOverrides](#cfn-pipes-pipe-pipetargetbatchjobparameters-containeroverrides): 
    BatchContainerOverrides
  [DependsOn](#cfn-pipes-pipe-pipetargetbatchjobparameters-dependson): 
    - BatchJobDependency
  [JobDefinition](#cfn-pipes-pipe-pipetargetbatchjobparameters-jobdefinition): String
  [JobName](#cfn-pipes-pipe-pipetargetbatchjobparameters-jobname): String
  [Parameters](#cfn-pipes-pipe-pipetargetbatchjobparameters-parameters): 
    Key : Value
  [RetryStrategy](#cfn-pipes-pipe-pipetargetbatchjobparameters-retrystrategy): 
    BatchRetryStrategy
```

## Properties<a name="aws-properties-pipes-pipe-pipetargetbatchjobparameters-properties"></a>

`ArrayProperties`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-arrayproperties"></a>
The array properties for the submitted job, such as the size of the array\. The array size can be between 2 and 10,000\. If you specify array properties for a job, it becomes an array job\. This parameter is used only if the target is an AWS Batch job\.  
*Required*: No  
*Type*: [BatchArrayProperties](aws-properties-pipes-pipe-batcharrayproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainerOverrides`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-containeroverrides"></a>
The overrides that are sent to a container\.  
*Required*: No  
*Type*: [BatchContainerOverrides](aws-properties-pipes-pipe-batchcontaineroverrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DependsOn`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-dependson"></a>
A list of dependencies for the job\. A job can depend upon a maximum of 20 jobs\. You can specify a `SEQUENTIAL` type dependency without specifying a job ID for array jobs so that each child array job completes sequentially, starting at index 0\. You can also specify an `N_TO_N` type dependency with a job ID for array jobs\. In that case, each index child of this job must wait for the corresponding index child of each dependency to complete before it can begin\.  
*Required*: No  
*Type*: List of [BatchJobDependency](aws-properties-pipes-pipe-batchjobdependency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobDefinition`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-jobdefinition"></a>
The job definition used by this job\. This value can be one of `name`, `name:revision`, or the Amazon Resource Name \(ARN\) for the job definition\. If name is specified without a revision then the latest active revision is used\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobName`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-jobname"></a>
The name of the job\. It can be up to 128 letters long\. The first character must be alphanumeric, can contain uppercase and lowercase letters, numbers, hyphens \(\-\), and underscores \(\_\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-parameters"></a>
Additional parameters passed to the job that replace parameter substitution placeholders that are set in the job definition\. Parameters are specified as a key and value pair mapping\. Parameters included here override any corresponding parameter defaults from the job definition\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryStrategy`  <a name="cfn-pipes-pipe-pipetargetbatchjobparameters-retrystrategy"></a>
The retry strategy to use for failed jobs\. When a retry strategy is specified here, it overrides the retry strategy defined in the job definition\.  
*Required*: No  
*Type*: [BatchRetryStrategy](aws-properties-pipes-pipe-batchretrystrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)