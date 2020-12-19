# AWS::Batch::JobDefinition<a name="aws-resource-batch-jobdefinition"></a>

The `AWS::Batch::JobDefinition` resource specifies the parameters for an AWS Batch job definition\. For more information, see [Job Definitions](https://docs.aws.amazon.com/batch/latest/userguide/job_definitions.html) in the *AWS Batch User Guide*\.

## Syntax<a name="aws-resource-batch-jobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-jobdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::JobDefinition",
  "Properties" : {
      "[ContainerProperties](#cfn-batch-jobdefinition-containerproperties)" : ContainerProperties,
      "[JobDefinitionName](#cfn-batch-jobdefinition-jobdefinitionname)" : String,
      "[NodeProperties](#cfn-batch-jobdefinition-nodeproperties)" : NodeProperties,
      "[Parameters](#cfn-batch-jobdefinition-parameters)" : Json,
      "[PlatformCapabilities](#cfn-batch-jobdefinition-platformcapabilities)" : [ String, ... ],
      "[PropagateTags](#cfn-batch-jobdefinition-propagatetags)" : Boolean,
      "[RetryStrategy](#cfn-batch-jobdefinition-retrystrategy)" : RetryStrategy,
      "[Tags](#cfn-batch-jobdefinition-tags)" : Json,
      "[Timeout](#cfn-batch-jobdefinition-timeout)" : Timeout,
      "[Type](#cfn-batch-jobdefinition-type)" : String
    }
}
```

### YAML<a name="aws-resource-batch-jobdefinition-syntax.yaml"></a>

```
Type: AWS::Batch::JobDefinition
Properties: 
  [ContainerProperties](#cfn-batch-jobdefinition-containerproperties): 
    ContainerProperties
  [JobDefinitionName](#cfn-batch-jobdefinition-jobdefinitionname): String
  [NodeProperties](#cfn-batch-jobdefinition-nodeproperties): 
    NodeProperties
  [Parameters](#cfn-batch-jobdefinition-parameters): Json
  [PlatformCapabilities](#cfn-batch-jobdefinition-platformcapabilities): 
    - String
  [PropagateTags](#cfn-batch-jobdefinition-propagatetags): Boolean
  [RetryStrategy](#cfn-batch-jobdefinition-retrystrategy): 
    RetryStrategy
  [Tags](#cfn-batch-jobdefinition-tags): Json
  [Timeout](#cfn-batch-jobdefinition-timeout): 
    Timeout
  [Type](#cfn-batch-jobdefinition-type): String
```

## Properties<a name="aws-resource-batch-jobdefinition-properties"></a>

`ContainerProperties`  <a name="cfn-batch-jobdefinition-containerproperties"></a>
An object with various properties specific to container\-based jobs\.  
*Required*: No  
*Type*: [ContainerProperties](aws-properties-batch-jobdefinition-containerproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobDefinitionName`  <a name="cfn-batch-jobdefinition-jobdefinitionname"></a>
The name of the job definition\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NodeProperties`  <a name="cfn-batch-jobdefinition-nodeproperties"></a>
An object with various properties specific to multi\-node parallel jobs\.  
If the job runs on Fargate resources, then you must not specify `nodeProperties`; use `containerProperties` instead\.
*Required*: No  
*Type*: [NodeProperties](aws-properties-batch-jobdefinition-nodeproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-batch-jobdefinition-parameters"></a>
Default parameters or parameter substitution placeholders that are set in the job definition\. Parameters are specified as a key\-value pair mapping\. Parameters in a `SubmitJob` request override any corresponding parameter defaults from the job definition\. For more information about specifying parameters, see [Job Definition Parameters](https://docs.aws.amazon.com/batch/latest/userguide/job_definition_parameters.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlatformCapabilities`  <a name="cfn-batch-jobdefinition-platformcapabilities"></a>
The platform capabilities required by the job definition\. If no value is specified, it defaults to `EC2`\. Jobs run on Fargate resources specify `FARGATE`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropagateTags`  <a name="cfn-batch-jobdefinition-propagatetags"></a>
Specifies whether to propagate the tags from the job or job definition to the corresponding Amazon ECS task\. If no value is specified, the tags aren't propagated\. Tags can only be propagated to the tasks during task creation\. For tags with the same name, job tags are given priority over job definitions tags\. If the total number of combined tags from the job and job definition is over 50, the job is moved to the `FAILED` state\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryStrategy`  <a name="cfn-batch-jobdefinition-retrystrategy"></a>
The retry strategy to use for failed jobs that are submitted with this job definition\.  
*Required*: No  
*Type*: [RetryStrategy](aws-properties-batch-jobdefinition-retrystrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-batch-jobdefinition-tags"></a>
The tags applied to the job definition\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Timeout`  <a name="cfn-batch-jobdefinition-timeout"></a>
The timeout configuration for jobs that are submitted with this job definition\. You can specify a timeout duration after which AWS Batch terminates your jobs if they haven't finished\.  
*Required*: No  
*Type*: [Timeout](aws-properties-batch-jobdefinition-timeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-batch-jobdefinition-type"></a>
The type of job definition\. For more information about multi\-node parallel jobs, see [Creating a multi\-node parallel job definition](https://docs.aws.amazon.com/batch/latest/userguide/multi-node-job-def.html) in the *AWS Batch User Guide*\.  
If the job is run on Fargate resources, then `multinode` isn't supported\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `container | multinode`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-batch-jobdefinition-return-values"></a>

### Ref<a name="aws-resource-batch-jobdefinition-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the job definition ARN, such as `arn:aws:batch:us-east-1:111122223333:job-definition/test-gpu:2`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-batch-jobdefinition--examples"></a>



### Test nvidia\-smi<a name="aws-resource-batch-jobdefinition--examples--Test_nvidia-smi"></a>

The following example tests the `nvidia-smi` command on a GPU instance to verify that the GPU is working inside the container\. For more information, see [Test GPU Functionality](https://docs.aws.amazon.com/batch/latest/userguide/example-job-definitions.html#example-test-gpu) in the *AWS Batch User Guide*\.

#### JSON<a name="aws-resource-batch-jobdefinition--examples--Test_nvidia-smi--json"></a>

```
{
 "JobDefinition": {
  "Type": "AWS::Batch::JobDefinition",
  "Properties": {
   "Type": "container",
   "JobDefinitionName": "nvidia-smi",
   "ContainerProperties": {
    "MountPoints": [
     {
      "ReadOnly": false,
      "SourceVolume": "nvidia",
      "ContainerPath": "/usr/local/nvidia"
     }
    ],
    "Volumes": [
     {
      "Host": {
        "SourcePath": "/var/lib/nvidia-docker/volumes/nvidia_driver/latest"
      },
      "Name": "nvidia"
     }
    ],
    "Command": [
      "nvidia-smi"
    ],
    "Memory": 2000,
    "Privileged": true,
    "JobRoleArn": "String",
    "ReadonlyRootFilesystem": true,
    "Vcpus": 2,
    "Image": "nvidia/cuda"
   }
  }
 }
}
```

#### YAML<a name="aws-resource-batch-jobdefinition--examples--Test_nvidia-smi--yaml"></a>

```
JobDefinition:
  Type: AWS::Batch::JobDefinition
  Properties:
    Type: container
    JobDefinitionName: nvidia-smi
    ContainerProperties:
      MountPoints:
        - ReadOnly: false
          SourceVolume: nvidia
          ContainerPath: /usr/local/nvidia
      Volumes:
        - Host:
            SourcePath: /var/lib/nvidia-docker/volumes/nvidia_driver/latest
          Name: nvidia
      Command:
        - nvidia-smi
      Memory: 2000
      Privileged: true
      JobRoleArn: String
      ReadonlyRootFilesystem: true
      Vcpus: 2
      Image: nvidia/cuda
```

## See also<a name="aws-resource-batch-jobdefinition--seealso"></a>
+  [Job Definition Parameters](https://docs.aws.amazon.com/batch/latest/userguide/job_definition_parameters.html) in the *AWS Batch User Guide*\.