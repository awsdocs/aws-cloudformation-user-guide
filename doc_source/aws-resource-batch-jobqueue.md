# AWS::Batch::JobQueue<a name="aws-resource-batch-jobqueue"></a>

The `AWS::Batch::JobQueue` resource specifies the parameters for an AWS Batch job queue definition\. For more information, see [Job Queues](https://docs.aws.amazon.com/batch/latest/userguide/job_queues.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-resource-batch-jobqueue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-jobqueue-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::JobQueue",
  "Properties" : {
      "[ComputeEnvironmentOrder](#cfn-batch-jobqueue-computeenvironmentorder)" : [ ComputeEnvironmentOrder, ... ],
      "[JobQueueName](#cfn-batch-jobqueue-jobqueuename)" : String,
      "[Priority](#cfn-batch-jobqueue-priority)" : Integer,
      "[State](#cfn-batch-jobqueue-state)" : String,
      "[Tags](#cfn-batch-jobqueue-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-batch-jobqueue-syntax.yaml"></a>

```
Type: AWS::Batch::JobQueue
Properties: 
  [ComputeEnvironmentOrder](#cfn-batch-jobqueue-computeenvironmentorder): 
    - ComputeEnvironmentOrder
  [JobQueueName](#cfn-batch-jobqueue-jobqueuename): String
  [Priority](#cfn-batch-jobqueue-priority): Integer
  [State](#cfn-batch-jobqueue-state): String
  [Tags](#cfn-batch-jobqueue-tags): Json
```

## Properties<a name="aws-resource-batch-jobqueue-properties"></a>

`ComputeEnvironmentOrder`  <a name="cfn-batch-jobqueue-computeenvironmentorder"></a>
The set of compute environments mapped to a job queue and their order relative to each other\. The job scheduler uses this parameter to determine which compute environment should run a specific job\. Compute environments must be in the `VALID` state before you can associate them with a job queue\. You can associate up to three compute environments with a job queue\. All of the compute environments must be either EC2 \(`EC2` or `SPOT`\) or Fargate \(`FARGATE` or `FARGATE_SPOT`\); EC2 and Fargate compute environments can't be mixed\.  
All compute environments that are associated with a job queue must share the same architecture\. AWS Batch doesn't support mixing compute environment architecture types in a single job queue\.
*Required*: Yes  
*Type*: [List](aws-properties-batch-jobqueue-computeenvironmentorder.md) of [ComputeEnvironmentOrder](aws-properties-batch-jobqueue-computeenvironmentorder.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobQueueName`  <a name="cfn-batch-jobqueue-jobqueuename"></a>
The name of the job queue\. Up to 128 letters \(uppercase and lowercase\), numbers, and underscores are allowed\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-batch-jobqueue-priority"></a>
The priority of the job queue\. Job queues with a higher priority \(or a higher integer value for the `priority` parameter\) are evaluated first when associated with the same compute environment\. Priority is determined in descending order\. For example, a job queue with a priority value of `10` is given scheduling preference over a job queue with a priority value of `1`\. All of the compute environments must be either EC2 \(`EC2` or `SPOT`\) or Fargate \(`FARGATE` or `FARGATE_SPOT`\); EC2 and Fargate compute environments cannot be mixed\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-batch-jobqueue-state"></a>
The state of the job queue\. If the job queue state is `ENABLED`, it is able to accept jobs\. If the job queue state is `DISABLED`, new jobs can't be added to the queue, but jobs already in the queue can finish\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-batch-jobqueue-tags"></a>
The tags applied to the job queue\. For more information, see [Tagging your AWS Batch resources](https://docs.aws.amazon.com/batch/latest/userguide/using-tags.html) in *AWS Batch User Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-batch-jobqueue-return-values"></a>

### Ref<a name="aws-resource-batch-jobqueue-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the job queue ARN, such as `arn:aws:batch:us-east-1:111122223333:job-queue/HighPriority`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-batch-jobqueue--examples"></a>



### Job queue with two compute environments<a name="aws-resource-batch-jobqueue--examples--Job_queue_with_two_compute_environments"></a>

The following example defines a job queue called HighPriority that has two compute environments mapped to it\.

#### JSON<a name="aws-resource-batch-jobqueue--examples--Job_queue_with_two_compute_environments--json"></a>

```
{
  "JobQueue": {
    "Type": "AWS::Batch::JobQueue",
    "Properties": {
      "ComputeEnvironmentOrder": [
        {
         "Order": 1,
         "ComputeEnvironment": "C4OnDemand"
        },
        {
          "Order": 2,
          "ComputeEnvironment": "M4Spot"
        }
      ],
      "State": "ENABLED",
      "Priority": 1,
      "JobQueueName": "HighPriority"
    }
  }
}
```

#### YAML<a name="aws-resource-batch-jobqueue--examples--Job_queue_with_two_compute_environments--yaml"></a>

```
JobQueue:
  Type: AWS::Batch::JobQueue
  Properties:
    ComputeEnvironmentOrder:
      - Order: 1
        ComputeEnvironment: C4OnDemand
      - Order: 2
        ComputeEnvironment: M4Spot
    State: ENABLED
    Priority: 1
    JobQueueName: HighPriority
```

## See also<a name="aws-resource-batch-jobqueue--seealso"></a>
+  [Job Queue Parameters](https://docs.aws.amazon.com/batch/latest/userguide/job_queue_parameters.html) in the *AWS Batch User Guide*\.