# AWS::SageMaker::EndpointConfig DataCaptureConfig<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig"></a>

Specifies the configuration of your endpoint for model monitor data capture\. 

## Syntax<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-syntax.json"></a>

```
{
  "[CaptureContentTypeHeader](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader)" : CaptureContentTypeHeader,
  "[CaptureOptions](#cfn-sagemaker-endpointconfig-datacaptureconfig-captureoptions)" : [ CaptureOption, ... ],
  "[DestinationS3Uri](#cfn-sagemaker-endpointconfig-datacaptureconfig-destinations3uri)" : String,
  "[EnableCapture](#cfn-sagemaker-endpointconfig-datacaptureconfig-enablecapture)" : Boolean,
  "[InitialSamplingPercentage](#cfn-sagemaker-endpointconfig-datacaptureconfig-initialsamplingpercentage)" : Integer,
  "[KmsKeyId](#cfn-sagemaker-endpointconfig-datacaptureconfig-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-syntax.yaml"></a>

```
  [CaptureContentTypeHeader](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader): 
    CaptureContentTypeHeader
  [CaptureOptions](#cfn-sagemaker-endpointconfig-datacaptureconfig-captureoptions): 
    - CaptureOption
  [DestinationS3Uri](#cfn-sagemaker-endpointconfig-datacaptureconfig-destinations3uri): String
  [EnableCapture](#cfn-sagemaker-endpointconfig-datacaptureconfig-enablecapture): Boolean
  [InitialSamplingPercentage](#cfn-sagemaker-endpointconfig-datacaptureconfig-initialsamplingpercentage): Integer
  [KmsKeyId](#cfn-sagemaker-endpointconfig-datacaptureconfig-kmskeyid): String
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-properties"></a>

`CaptureContentTypeHeader`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader"></a>
A list of the JSON and CSV content type that the endpoint captures\.  
*Required*: No  
*Type*: [CaptureContentTypeHeader](aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CaptureOptions`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-captureoptions"></a>
Specifies whether the endpoint captures input data to your model, output data from your model, or both\.  
*Required*: Yes  
*Type*: List of [CaptureOption](aws-properties-sagemaker-endpointconfig-captureoption.md)  
*Maximum*: `2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationS3Uri`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-destinations3uri"></a>
The S3 bucket where model monitor stores captured data\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `^(https|s3)://([^/])/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableCapture`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-enablecapture"></a>
Set to `True` to enable data capture\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InitialSamplingPercentage`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-initialsamplingpercentage"></a>
The percentage of data to capture\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-kmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt the captured data at rest using Amazon S3 server\-side encryption\. The KmsKeyId can be any of the following formats: Key ID: 1234abcd\-12ab\-34cd\-56ef\-1234567890ab Key ARN: arn:aws:kms:us\-west\-2:111122223333:key/1234abcd\-12ab\-34cd\-56ef\-1234567890ab Alias name: alias/ExampleAlias Alias name ARN: arn:aws:kms:us\-west\-2:111122223333:alias/ExampleAlias If you don't provide a KMS key ID, Amazon SageMaker uses the default KMS key for Amazon S3 for your role's account\. For more information, see KMS\-Managed Encryption Keys \(https://docs\.aws\.amazon\.com/AmazonS3/latest/dev/UsingKMSEncryption\.html\) in the Amazon Simple Storage Service Developer Guide\. The KMS key policy must grant permission to the IAM role that you specify in your CreateModel \(https://docs\.aws\.amazon\.com/sagemaker/latest/APIReference/API\_CreateModel\.html\) request\. For more information, see Using Key Policies in AWS KMS \(http://docs\.aws\.amazon\.com/kms/latest/developerguide/key\-policies\.html\) in the AWS Key Management Service Developer Guide\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)