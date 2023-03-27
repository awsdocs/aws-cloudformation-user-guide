# AWS::SageMaker::ModelBiasJobDefinition BatchTransformInput<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput"></a>

<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput-description"></a>The `BatchTransformInput` property type specifies Property description not available\. for an [AWS::SageMaker::ModelBiasJobDefinition](aws-resource-sagemaker-modelbiasjobdefinition.md)\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput-syntax.json"></a>

```
{
  "[DataCapturedDestinationS3Uri](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datacaptureddestinations3uri)" : String,
  "[DatasetFormat](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datasetformat)" : DatasetFormat,
  "[EndTimeOffset](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-endtimeoffset)" : String,
  "[FeaturesAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-featuresattribute)" : String,
  "[InferenceAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-inferenceattribute)" : String,
  "[LocalPath](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-localpath)" : String,
  "[ProbabilityAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilityattribute)" : String,
  "[ProbabilityThresholdAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilitythresholdattribute)" : Double,
  "[S3DataDistributionType](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3datadistributiontype)" : String,
  "[S3InputMode](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3inputmode)" : String,
  "[StartTimeOffset](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-starttimeoffset)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput-syntax.yaml"></a>

```
  [DataCapturedDestinationS3Uri](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datacaptureddestinations3uri): String
  [DatasetFormat](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datasetformat): 
    DatasetFormat
  [EndTimeOffset](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-endtimeoffset): String
  [FeaturesAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-featuresattribute): String
  [InferenceAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-inferenceattribute): String
  [LocalPath](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-localpath): String
  [ProbabilityAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilityattribute): String
  [ProbabilityThresholdAttribute](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilitythresholdattribute): Double
  [S3DataDistributionType](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3datadistributiontype): String
  [S3InputMode](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3inputmode): String
  [StartTimeOffset](#cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-starttimeoffset): String
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-batchtransforminput-properties"></a>

`DataCapturedDestinationS3Uri`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datacaptureddestinations3uri"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatasetFormat`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-datasetformat"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [DatasetFormat](aws-properties-sagemaker-modelbiasjobdefinition-datasetformat.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndTimeOffset`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-endtimeoffset"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeaturesAttribute`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-featuresattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InferenceAttribute`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-inferenceattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalPath`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-localpath"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityAttribute`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilityattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityThresholdAttribute`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-probabilitythresholdattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3DataDistributionType`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3datadistributiontype"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3InputMode`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-s3inputmode"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartTimeOffset`  <a name="cfn-sagemaker-modelbiasjobdefinition-batchtransforminput-starttimeoffset"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)