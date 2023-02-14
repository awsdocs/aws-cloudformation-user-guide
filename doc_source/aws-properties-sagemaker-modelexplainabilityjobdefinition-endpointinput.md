# AWS::SageMaker::ModelExplainabilityJobDefinition EndpointInput<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-endpointinput"></a>

Input object for the endpoint

## Syntax<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-endpointinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-endpointinput-syntax.json"></a>

```
{
  "[EndpointName](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-endpointname)" : String,
  "[FeaturesAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-featuresattribute)" : String,
  "[InferenceAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-inferenceattribute)" : String,
  "[LocalPath](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-localpath)" : String,
  "[ProbabilityAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-probabilityattribute)" : String,
  "[S3DataDistributionType](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3datadistributiontype)" : String,
  "[S3InputMode](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3inputmode)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-endpointinput-syntax.yaml"></a>

```
  [EndpointName](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-endpointname): String
  [FeaturesAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-featuresattribute): String
  [InferenceAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-inferenceattribute): String
  [LocalPath](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-localpath): String
  [ProbabilityAttribute](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-probabilityattribute): String
  [S3DataDistributionType](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3datadistributiontype): String
  [S3InputMode](#cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3inputmode): String
```

## Properties<a name="aws-properties-sagemaker-modelexplainabilityjobdefinition-endpointinput-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-endpointname"></a>
An endpoint in customer's account which has enabled `DataCaptureConfig` enabled\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeaturesAttribute`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-featuresattribute"></a>
The attributes of the input data that are the input features\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InferenceAttribute`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-inferenceattribute"></a>
The attribute of the input data that represents the ground truth label\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalPath`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-localpath"></a>
Path to the filesystem where the endpoint data is available to the container\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityAttribute`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-probabilityattribute"></a>
In a classification problem, the attribute that represents the class probability\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3DataDistributionType`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3datadistributiontype"></a>
Whether input data distributed in Amazon S3 is fully replicated or sharded by an S3 key\. Defaults to `FullyReplicated`   
*Required*: No  
*Type*: String  
*Allowed values*: `FullyReplicated | ShardedByS3Key`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3InputMode`  <a name="cfn-sagemaker-modelexplainabilityjobdefinition-endpointinput-s3inputmode"></a>
Whether the `Pipe` or `File` is used as the input mode for transferring data for the monitoring job\. `Pipe` mode is recommended for large datasets\. `File` mode is useful for small files that fit in memory\. Defaults to `File`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `File | Pipe`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)