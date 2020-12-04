# AWS::SageMaker::MonitoringSchedule EndpointInput<a name="aws-properties-sagemaker-monitoringschedule-endpointinput"></a>

Input object for the endpoint

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-endpointinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-endpointinput-syntax.json"></a>

```
{
  "[EndpointName](#cfn-sagemaker-monitoringschedule-endpointinput-endpointname)" : String,
  "[LocalPath](#cfn-sagemaker-monitoringschedule-endpointinput-localpath)" : String,
  "[S3DataDistributionType](#cfn-sagemaker-monitoringschedule-endpointinput-s3datadistributiontype)" : String,
  "[S3InputMode](#cfn-sagemaker-monitoringschedule-endpointinput-s3inputmode)" : String
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-endpointinput-syntax.yaml"></a>

```
  [EndpointName](#cfn-sagemaker-monitoringschedule-endpointinput-endpointname): String
  [LocalPath](#cfn-sagemaker-monitoringschedule-endpointinput-localpath): String
  [S3DataDistributionType](#cfn-sagemaker-monitoringschedule-endpointinput-s3datadistributiontype): String
  [S3InputMode](#cfn-sagemaker-monitoringschedule-endpointinput-s3inputmode): String
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-endpointinput-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-monitoringschedule-endpointinput-endpointname"></a>
An endpoint in customer's account which has enabled `DataCaptureConfig` enabled\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalPath`  <a name="cfn-sagemaker-monitoringschedule-endpointinput-localpath"></a>
Path to the filesystem where the endpoint data is available to the container\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3DataDistributionType`  <a name="cfn-sagemaker-monitoringschedule-endpointinput-s3datadistributiontype"></a>
Whether input data distributed in Amazon S3 is fully replicated or sharded by an S3 key\. Defauts to `FullyReplicated`   
*Required*: No  
*Type*: String  
*Allowed values*: `FullyReplicated | ShardedByS3Key`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3InputMode`  <a name="cfn-sagemaker-monitoringschedule-endpointinput-s3inputmode"></a>
Whether the `Pipe` or `File` is used as the input mode for transfering data for the monitoring job\. `Pipe` mode is recommended for large datasets\. `File` mode is useful for small files that fit in memory\. Defaults to `File`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `File | Pipe`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)