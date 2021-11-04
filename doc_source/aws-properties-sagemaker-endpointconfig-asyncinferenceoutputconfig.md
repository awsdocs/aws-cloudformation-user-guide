# AWS::SageMaker::EndpointConfig AsyncInferenceOutputConfig<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig"></a>

Specifies the configuration for asynchronous inference invocation outputs\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-kmskeyid)" : String,
  "[NotificationConfig](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-notificationconfig)" : AsyncInferenceNotificationConfig,
  "[S3OutputPath](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-s3outputpath)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-kmskeyid): String
  [NotificationConfig](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-notificationconfig): 
    AsyncInferenceNotificationConfig
  [S3OutputPath](#cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-s3outputpath): String
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-kmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt the asynchronous inference output in Amazon S3\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NotificationConfig`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-notificationconfig"></a>
Specifies the configuration for notifications of inference results for asynchronous inference\.  
*Required*: No  
*Type*: [AsyncInferenceNotificationConfig](aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3OutputPath`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceoutputconfig-s3outputpath"></a>
The Amazon S3 location to upload inference responses to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)