# AWS::SageMaker::ModelQualityJobDefinition S3Output<a name="aws-properties-sagemaker-modelqualityjobdefinition-s3output"></a>

The Amazon S3 storage location where the results of a monitoring job are saved\.

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-s3output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-s3output-syntax.json"></a>

```
{
  "[LocalPath](#cfn-sagemaker-modelqualityjobdefinition-s3output-localpath)" : String,
  "[S3UploadMode](#cfn-sagemaker-modelqualityjobdefinition-s3output-s3uploadmode)" : String,
  "[S3Uri](#cfn-sagemaker-modelqualityjobdefinition-s3output-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-s3output-syntax.yaml"></a>

```
  [LocalPath](#cfn-sagemaker-modelqualityjobdefinition-s3output-localpath): String
  [S3UploadMode](#cfn-sagemaker-modelqualityjobdefinition-s3output-s3uploadmode): String
  [S3Uri](#cfn-sagemaker-modelqualityjobdefinition-s3output-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-s3output-properties"></a>

`LocalPath`  <a name="cfn-sagemaker-modelqualityjobdefinition-s3output-localpath"></a>
The local path to the Amazon S3 storage location where Amazon SageMaker saves the results of a monitoring job\. LocalPath is an absolute path for the output data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3UploadMode`  <a name="cfn-sagemaker-modelqualityjobdefinition-s3output-s3uploadmode"></a>
Whether to upload the results of the monitoring job continuously or after the job completes\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Uri`  <a name="cfn-sagemaker-modelqualityjobdefinition-s3output-s3uri"></a>
A URI that identifies the Amazon S3 storage location where Amazon SageMaker saves the results of a monitoring job\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)