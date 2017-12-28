# AWS::Batch::JobDefinition<a name="aws-resource-batch-jobdefinition"></a>

The `AWS::Batch::JobDefinition` resource specifies the parameters for an AWS Batch job definition\. For more information, see [Job Definitions](http://docs.aws.amazon.com/batch/latest/userguide/job_definitions.html) in the *AWS Batch User Guide*\. 


+ [Syntax](#aws-resource-batch-jobdefinition-syntax)
+ [Properties](#aws-resource-batch-jobdefinition-properties)
+ [Return Values](#aws-resource-batch-jobdefinition-returnvalues)
+ [Examples](#aws-resource-batch-jobdefinition-examples)

## Syntax<a name="aws-resource-batch-jobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-batch-jobdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Batch::JobDefinition",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-type)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-parameters)" : Json object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties)" : ContainerProperties,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-jobdefinitionname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-retrystrategy)" : RetryStrategy
  }
}
```

### YAML<a name="aws-resource-batch-jobdefinition-syntax.yaml"></a>

```
Type: "AWS::Batch::JobDefinition"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-type): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-parameters): Json object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties): 
    ContainerProperties
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-jobdefinitionname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-retrystrategy): 
    RetryStrategy
```

## Properties<a name="aws-resource-batch-jobdefinition-properties"></a>

`Type`  
The type of job definition\.  
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 

`Parameters`  
Default parameters or parameter substitution placeholders that are set in the job definition\. Parameters are specified as a key\-value pair mapping\.  
 *Required*: yes  
*Type*: JSON object  
 *Update requires*: No Interruption 

`JobDefinitionName`  
The name of the job definition\.  
 *Required*: no  
*Type*: String  
 *Update requires*: Replacement 

`ContainerProperties`  
An object with various properties specific to container\-based jobs\.  
 *Required*: yes  
 *Type*: [AWS Batch JobDefinition ContainerProperties](aws-properties-batch-jobdefinition-containerproperties.md)  
 *Update requires*: No Interruption 

`RetryStrategy`  
The retry strategy to use for failed jobs that are submitted with this job definition\.  
 *Required*: no  
 *Type*: [AWS Batch JobDefinition RetryStrategy](aws-properties-batch-jobdefinition-retrystrategy.md)  
 *Update requires*: No Interruption 

## Return Values<a name="aws-resource-batch-jobdefinition-returnvalues"></a>

### Ref<a name="w3ab2c21c10d134c10b2"></a>

When you pass the logical ID of an `AWS::Batch::JobDefinition` resource to the intrinsic `Ref` function, the function returns the job definition ARN, such as `arn:aws:batch:us-east-1:111122223333:job-definition/test-gpu:2`\. 

For more information about using the `Ref` function, see Ref\.

## Examples<a name="aws-resource-batch-jobdefinition-examples"></a>

### Test nvidia\-smi<a name="aws-resource-batch-jobdefinition-example1"></a>

The following example tests the nvidia\-smi command on a GPU instance to verify that the GPU is working inside the container\. For more information, see [Test GPU Functionality](http://docs.aws.amazon.com/batch/latest/userguide/example-job-definitions.html#example-test-gpu) in the *AWS Batch User Guide*\.

#### JSON<a name="aws-resource-batch-jobdefinition-example1.json"></a>

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

#### YAML<a name="aws-resource-batch-jobdefinition-example1.yaml"></a>

```
JobDefinition:
  Type: 'AWS::Batch::JobDefinition'
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