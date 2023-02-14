# AWS::Batch::ComputeEnvironment UpdatePolicy<a name="aws-properties-batch-computeenvironment-updatepolicy"></a>

Specifies the infrastructure update policy for the compute environment\. For more information about infrastructure updates, see [Updating compute environments](https://docs.aws.amazon.com/batch/latest/userguide/updating-compute-environments.html) in the * AWS Batch User Guide*\.

## Syntax<a name="aws-properties-batch-computeenvironment-updatepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-computeenvironment-updatepolicy-syntax.json"></a>

```
{
  "[JobExecutionTimeoutMinutes](#cfn-batch-computeenvironment-updatepolicy-jobexecutiontimeoutminutes)" : Integer,
  "[TerminateJobsOnUpdate](#cfn-batch-computeenvironment-updatepolicy-terminatejobsonupdate)" : Boolean
}
```

### YAML<a name="aws-properties-batch-computeenvironment-updatepolicy-syntax.yaml"></a>

```
  [JobExecutionTimeoutMinutes](#cfn-batch-computeenvironment-updatepolicy-jobexecutiontimeoutminutes): Integer
  [TerminateJobsOnUpdate](#cfn-batch-computeenvironment-updatepolicy-terminatejobsonupdate): Boolean
```

## Properties<a name="aws-properties-batch-computeenvironment-updatepolicy-properties"></a>

`JobExecutionTimeoutMinutes`  <a name="cfn-batch-computeenvironment-updatepolicy-jobexecutiontimeoutminutes"></a>
Specifies the job timeout \(in minutes\) when the compute environment infrastructure is updated\. The default value is 30\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminateJobsOnUpdate`  <a name="cfn-batch-computeenvironment-updatepolicy-terminatejobsonupdate"></a>
Specifies whether jobs are automatically terminated when the computer environment infrastructure is updated\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)