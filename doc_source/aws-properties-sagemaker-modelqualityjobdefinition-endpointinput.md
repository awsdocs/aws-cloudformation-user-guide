# AWS::SageMaker::ModelQualityJobDefinition EndpointInput<a name="aws-properties-sagemaker-modelqualityjobdefinition-endpointinput"></a>

Input object for the endpoint

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-endpointinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-endpointinput-syntax.json"></a>

```
{
  "[EndpointName](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-endpointname)" : String,
  "[EndTimeOffset](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-endtimeoffset)" : String,
  "[InferenceAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-inferenceattribute)" : String,
  "[LocalPath](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-localpath)" : String,
  "[ProbabilityAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilityattribute)" : String,
  "[ProbabilityThresholdAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilitythresholdattribute)" : Double,
  "[S3DataDistributionType](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3datadistributiontype)" : String,
  "[S3InputMode](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3inputmode)" : String,
  "[StartTimeOffset](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-starttimeoffset)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-endpointinput-syntax.yaml"></a>

```
  [EndpointName](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-endpointname): String
  [EndTimeOffset](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-endtimeoffset): String
  [InferenceAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-inferenceattribute): String
  [LocalPath](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-localpath): String
  [ProbabilityAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilityattribute): String
  [ProbabilityThresholdAttribute](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilitythresholdattribute): Double
  [S3DataDistributionType](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3datadistributiontype): String
  [S3InputMode](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3inputmode): String
  [StartTimeOffset](#cfn-sagemaker-modelqualityjobdefinition-endpointinput-starttimeoffset): String
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-endpointinput-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-endpointname"></a>
An endpoint in customer's account which has enabled `DataCaptureConfig` enabled\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndTimeOffset`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-endtimeoffset"></a>
If specified, monitoring jobs substract this time from the end time\. For information about using offsets for scheduling monitoring jobs, see [Schedule Model Quality Monitoring Jobs](https://docs.aws.amazon.com/sagemaker/latest/dg/model-monitor-model-quality-schedule.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `15`  
*Pattern*: `^.?P.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InferenceAttribute`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-inferenceattribute"></a>
The attribute of the input data that represents the ground truth label\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalPath`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-localpath"></a>
Path to the filesystem where the endpoint data is available to the container\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityAttribute`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilityattribute"></a>
In a classification problem, the attribute that represents the class probability\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityThresholdAttribute`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-probabilitythresholdattribute"></a>
The threshold for the class probability to be evaluated as a positive result\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3DataDistributionType`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3datadistributiontype"></a>
Whether input data distributed in Amazon S3 is fully replicated or sharded by an S3 key\. Defaults to `FullyReplicated`   
*Required*: No  
*Type*: String  
*Allowed values*: `FullyReplicated | ShardedByS3Key`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3InputMode`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-s3inputmode"></a>
Whether the `Pipe` or `File` is used as the input mode for transferring data for the monitoring job\. `Pipe` mode is recommended for large datasets\. `File` mode is useful for small files that fit in memory\. Defaults to `File`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `File | Pipe`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartTimeOffset`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointinput-starttimeoffset"></a>
If specified, monitoring jobs substract this time from the start time\. For information about using offsets for scheduling monitoring jobs, see [Schedule Model Quality Monitoring Jobs](https://docs.aws.amazon.com/sagemaker/latest/dg/model-monitor-model-quality-schedule.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `15`  
*Pattern*: `^.?P.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)