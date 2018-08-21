# AWS Batch JobQueue ComputeEnvironmentOrder<a name="aws-properties-batch-jobqueue-computeenvironmentorder"></a>

The `ComputeEnvironmentOrder` property type specifies the order in which compute environments are tried for job placement within a queue\. Compute environments are tried in ascending order\. For example, if two compute environments are associated with a job queue, the compute environment with a lower order integer value is tried for job placement first\.

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
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 

`Order`  <a name="cfn-batch-jobqueue-computeenvironmentorder-order"></a>
The order of the compute environment\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 