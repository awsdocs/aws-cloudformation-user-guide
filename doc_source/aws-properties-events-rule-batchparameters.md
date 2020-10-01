# AWS::Events::Rule BatchParameters<a name="aws-properties-events-rule-batchparameters"></a>

The custom parameters to be used when the target is an AWS Batch job\.

## Syntax<a name="aws-properties-events-rule-batchparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-batchparameters-syntax.json"></a>

```
{
  "[ArrayProperties](#cfn-events-rule-batchparameters-arrayproperties)" : BatchArrayProperties,
  "[JobDefinition](#cfn-events-rule-batchparameters-jobdefinition)" : String,
  "[JobName](#cfn-events-rule-batchparameters-jobname)" : String,
  "[RetryStrategy](#cfn-events-rule-batchparameters-retrystrategy)" : BatchRetryStrategy
}
```

### YAML<a name="aws-properties-events-rule-batchparameters-syntax.yaml"></a>

```
  [ArrayProperties](#cfn-events-rule-batchparameters-arrayproperties): 
    BatchArrayProperties
  [JobDefinition](#cfn-events-rule-batchparameters-jobdefinition): String
  [JobName](#cfn-events-rule-batchparameters-jobname): String
  [RetryStrategy](#cfn-events-rule-batchparameters-retrystrategy): 
    BatchRetryStrategy
```

## Properties<a name="aws-properties-events-rule-batchparameters-properties"></a>

`ArrayProperties`  <a name="cfn-events-rule-batchparameters-arrayproperties"></a>
The array properties for the submitted job, such as the size of the array\. The array size can be between 2 and 10,000\. If you specify array properties for a job, it becomes an array job\. This parameter is used only if the target is an AWS Batch job\.  
*Required*: No  
*Type*: [BatchArrayProperties](aws-properties-events-rule-batcharrayproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobDefinition`  <a name="cfn-events-rule-batchparameters-jobdefinition"></a>
The ARN or name of the job definition to use if the event target is an AWS Batch job\. This job definition must already exist\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobName`  <a name="cfn-events-rule-batchparameters-jobname"></a>
The name to use for this execution of the job, if the target is an AWS Batch job\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryStrategy`  <a name="cfn-events-rule-batchparameters-retrystrategy"></a>
The retry strategy to use for failed jobs, if the target is an AWS Batch job\. The retry strategy is the number of times to retry the failed job execution\. Valid values are 1–10\. When you specify a retry strategy here, it overrides the retry strategy defined in the job definition\.  
*Required*: No  
*Type*: [BatchRetryStrategy](aws-properties-events-rule-batchretrystrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)