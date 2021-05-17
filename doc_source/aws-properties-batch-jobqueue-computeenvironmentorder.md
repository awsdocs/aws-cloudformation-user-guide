# AWS::Batch::JobQueue ComputeEnvironmentOrder<a name="aws-properties-batch-jobqueue-computeenvironmentorder"></a>

The order in which compute environments are tried for job placement within a queue\. Compute environments are tried in ascending order\. For example, if two compute environments are associated with a job queue, the compute environment with a lower order integer value is tried for job placement first\. Compute environments must be in the `VALID` state before you can associate them with a job queue\. All of the compute environments must be either EC2 \(`EC2` or `SPOT`\) or Fargate \(`FARGATE` or `FARGATE_SPOT`\); EC2 and Fargate compute environments can't be mixed\.

**Note**  
All compute environments that are associated with a job queue must share the same architecture\. AWS Batch doesn't support mixing compute environment architecture types in a single job queue\.

## Syntax<a name="aws-properties-batch-jobqueue-computeenvironmentorder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobqueue-computeenvironmentorder-syntax.json"></a>

```
{
  "[ComputeEnvironment](#cfn-batch-jobqueue-computeenvironmentorder-computeenvironment)" : String,
  "[Order](#cfn-batch-jobqueue-computeenvironmentorder-order)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobqueue-computeenvironmentorder-syntax.yaml"></a>

```
  [ComputeEnvironment](#cfn-batch-jobqueue-computeenvironmentorder-computeenvironment): String
  [Order](#cfn-batch-jobqueue-computeenvironmentorder-order): Integer
```

## Properties<a name="aws-properties-batch-jobqueue-computeenvironmentorder-properties"></a>

`ComputeEnvironment`  <a name="cfn-batch-jobqueue-computeenvironmentorder-computeenvironment"></a>
The Amazon Resource Name \(ARN\) of the compute environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Order`  <a name="cfn-batch-jobqueue-computeenvironmentorder-order"></a>
The order of the compute environment\. Compute environments are tried in ascending order\. For example, if two compute environments are associated with a job queue, the compute environment with a lower `order` integer value is tried for job placement first\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)