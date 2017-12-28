# AWS::Batch::JobQueue<a name="aws-resource-batch-jobqueue"></a>

The `AWS::Batch::JobQueue` resource defines your AWS Batch job queue\. For more information, see [Job Queues](http://docs.aws.amazon.com/batch/latest/userguide/job_queues.html) in the *AWS Batch User Guide*\. 


+ [Syntax](#aws-resource-batch-jobqueue-syntax)
+ [Properties](#aws-resource-batch-jobqueue-properties)
+ [Return Values](#aws-resource-batch-jobqueue-returnvalues)
+ [Examples](#aws-resource-batch-jobqueue-examples)

## Syntax<a name="aws-resource-batch-jobqueue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-jobqueue-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::JobQueue",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-computeenvironmentorder)" : [ ComputeEnvironmentOrder, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-priority)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-state)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-jobqueuename)" : String
  }
}
```

### YAML<a name="aws-resource-batch-jobqueue-syntax.yaml"></a>

```
Type: "AWS::Batch::JobQueue"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-computeenvironmentorder): 
    - ComputeEnvironmentOrder 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-priority): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-state): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-jobqueuename): String
```

## Properties<a name="aws-resource-batch-jobqueue-properties"></a>

`ComputeEnvironmentOrder`  
The compute environments that are attached to the job queue and the order in which job placement is preferred\. Compute environments are selected for job placement in ascending order\.  
 *Required*: yes  
 *Type*: List of [AWS Batch JobQueue ComputeEnvironmentOrder](aws-properties-batch-jobqueue-computeenvironmentorder.md)  
 *Update requires*: No Interruption 

`State`  
The status of the job queue \(for example, `CREATING` or `VALID`\)\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 

`Priority`  
The priority of the job queue\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`JobQueueName`  
The name of the job queue\.  
 *Required*: no  
*Type*: String  
 *Update requires*: Replacement 

## Return Values<a name="aws-resource-batch-jobqueue-returnvalues"></a>

### Ref<a name="w3ab2c21c10d138c10b2"></a>

When you pass the logical ID of an `AWS::Batch::JobQueue` resource to the intrinsic `Ref` function, the function returns the job queue ARN, such as `arn:aws:batch:us-east-1:111122223333:job-queue/HighPriority`\. 

For more information about using the `Ref` function, see Ref\.

## Examples<a name="aws-resource-batch-jobqueue-examples"></a>

### Job queue with two compute environments<a name="aws-resource-batch-jobqueue-example1"></a>

The following example defines a job queue called `HighPriority` that has two compute environments mapped to it\.

#### JSON<a name="aws-resource-batch-jobqueue-example1.json"></a>

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

#### YAML<a name="aws-resource-batch-jobqueue-example1.yaml"></a>

```
JobQueue:
  Type: AWS::Batch::JobQueue
  Properties:
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-computeenvironmentorder):
      - [[ERROR] BAD/MISSING LINK TEXT](aws-properties-batch-jobqueue-computeenvironmentorder.md#cfn-batch-jobqueue-computeenvironmentorder-order): 1
        [[ERROR] BAD/MISSING LINK TEXT](aws-properties-batch-jobqueue-computeenvironmentorder.md#cfn-batch-jobqueue-computeenvironmentorder-computeenvironment): C4OnDemand
      - [[ERROR] BAD/MISSING LINK TEXT](aws-properties-batch-jobqueue-computeenvironmentorder.md#cfn-batch-jobqueue-computeenvironmentorder-order): 2
        [[ERROR] BAD/MISSING LINK TEXT](aws-properties-batch-jobqueue-computeenvironmentorder.md#cfn-batch-jobqueue-computeenvironmentorder-computeenvironment): M4Spot
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-state): ENABLED
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-priority): 1
    [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobqueue-jobqueuename): HighPriority
```