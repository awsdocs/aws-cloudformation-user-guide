# AWS::SageMaker::Pipeline<a name="aws-resource-sagemaker-pipeline"></a>

The `AWS::SageMaker::Pipeline` resource creates shell scripts that run when you create and/or start a SageMaker Pipeline\. For information about SageMaker Pipelines, see [SageMaker Pipelines](https://docs.aws.amazon.com/sagemaker/latest/dg/pipelines.html) in the *Amazon SageMaker Developer Guide*\.

## Syntax<a name="aws-resource-sagemaker-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Pipeline",
  "Properties" : {
      "[ParallelismConfiguration](#cfn-sagemaker-pipeline-parallelismconfiguration)" : ParallelismConfiguration,
      "[PipelineDefinition](#cfn-sagemaker-pipeline-pipelinedefinition)" : PipelineDefinition,
      "[PipelineDescription](#cfn-sagemaker-pipeline-pipelinedescription)" : String,
      "[PipelineDisplayName](#cfn-sagemaker-pipeline-pipelinedisplayname)" : String,
      "[PipelineName](#cfn-sagemaker-pipeline-pipelinename)" : String,
      "[RoleArn](#cfn-sagemaker-pipeline-rolearn)" : String,
      "[Tags](#cfn-sagemaker-pipeline-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-pipeline-syntax.yaml"></a>

```
Type: AWS::SageMaker::Pipeline
Properties: 
  [ParallelismConfiguration](#cfn-sagemaker-pipeline-parallelismconfiguration): 
    ParallelismConfiguration
  [PipelineDefinition](#cfn-sagemaker-pipeline-pipelinedefinition): 
    PipelineDefinition
  [PipelineDescription](#cfn-sagemaker-pipeline-pipelinedescription): String
  [PipelineDisplayName](#cfn-sagemaker-pipeline-pipelinedisplayname): String
  [PipelineName](#cfn-sagemaker-pipeline-pipelinename): String
  [RoleArn](#cfn-sagemaker-pipeline-rolearn): String
  [Tags](#cfn-sagemaker-pipeline-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-pipeline-properties"></a>

`ParallelismConfiguration`  <a name="cfn-sagemaker-pipeline-parallelismconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [ParallelismConfiguration](aws-properties-sagemaker-pipeline-parallelismconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineDefinition`  <a name="cfn-sagemaker-pipeline-pipelinedefinition"></a>
The definition of the pipeline\. This can be either a JSON string or an Amazon S3 location\.  
*Required*: Yes  
*Type*: [PipelineDefinition](aws-properties-sagemaker-pipeline-pipelinedefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineDescription`  <a name="cfn-sagemaker-pipeline-pipelinedescription"></a>
The description of the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `3072`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineDisplayName`  <a name="cfn-sagemaker-pipeline-pipelinedisplayname"></a>
The display name of the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,255}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineName`  <a name="cfn-sagemaker-pipeline-pipelinename"></a>
The name of the pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,255}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-sagemaker-pipeline-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used to execute the pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-pipeline-tags"></a>
The tags of the pipeline\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-pipeline-return-values"></a>

### Ref<a name="aws-resource-sagemaker-pipeline-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the PipelineName of the pipeline\. 

## Examples<a name="aws-resource-sagemaker-pipeline--examples"></a>

### SageMaker Pipeline Example<a name="aws-resource-sagemaker-pipeline--examples--SageMaker_Pipeline_Example"></a>

The following example creates a Pipeline with an associated lifecycle configuration\.

#### JSON<a name="aws-resource-sagemaker-pipeline--examples--SageMaker_Pipeline_Example--json"></a>

```
# Pipeline definition given as a JSON string
{
  "Resources": {
    "MyPipeline": {
      "Type": "AWS::SageMaker::Pipeline",
      "Properties": {
        "PipelineName": "<pipeline-name>"
        "PipelineDisplayName": "<pipeline-display-name>",
        "PipelineDescription": "<pipeline-description>",
        "PipelineDefinition": {
          "PipelineDefinitionBody": "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}"
        },
        "RoleArn": "arn:aws:iam::<account-id>:root"
      }
    }
  }
}
```

#### JSON<a name="aws-resource-sagemaker-pipeline--examples--SageMaker_Pipeline_Example--json"></a>

```
# Pipeline definition given as an S3 string
{
  "Resources": {
    "MyPipeline": {
      "Type": "AWS::SageMaker::Pipeline",
      "Properties": {
        "PipelineName": "<pipeline-name>",
        "PipelineDisplayName": "<pipeline-display-name>",
        "PipelineDescription": "<pipeline-description>",
        "PipelineDefinition": {
          "PipelineDefinitionS3Location": {
            "Bucket": "<S3-bucket-location>",
            "Key": "<S3-bucket-key>"
          }
        },
        "RoleArn": "arn:aws:iam::<account-id>:root"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-sagemaker-pipeline--examples--SageMaker_Pipeline_Example--yaml"></a>

```
# Pipeline definition given as a JSON string
Resources:
  MyPipeline:
    Type: AWS::SageMaker::Pipeline
    Properties:
      PipelineName: "<pipeline-name>" 
      PipelineDisplayName: "<pipeline-display-name>"
      PipelineDescription: "<pipeline-description>"
      PipelineDefinition:
        PipelineDefinitionBody: "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}"
      RoleArn: "arn:aws:iam::<account-id>:root"
```

#### YAML<a name="aws-resource-sagemaker-pipeline--examples--SageMaker_Pipeline_Example--yaml"></a>

```
# Pipeline definition given as an S3 location
Resources:
  MyPipeline:
    Type: AWS::SageMaker::Pipeline
    Properties:
      PipelineName: "<pipeline-name>"
      PipelineDisplayName:"<pipeline-display-name>"
      PipelineDescription: "<pipeline-description>"
      PipelineDefinition:
	    PipelineDefinitionS3Location:
          Bucket: "<S3-bucket-location>"
          Key: "<S3-bucket-key>"
      RoleArn: "arn:aws:iam::<account-id>:root"
```