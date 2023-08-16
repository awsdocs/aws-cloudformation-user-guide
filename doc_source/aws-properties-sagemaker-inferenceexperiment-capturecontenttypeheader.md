# AWS::SageMaker::InferenceExperiment CaptureContentTypeHeader<a name="aws-properties-sagemaker-inferenceexperiment-capturecontenttypeheader"></a>

Configuration specifying how to treat different headers\. If no headers are specified SageMaker will by default base64 encode when capturing the data\.

## Syntax<a name="aws-properties-sagemaker-inferenceexperiment-capturecontenttypeheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-inferenceexperiment-capturecontenttypeheader-syntax.json"></a>

```
{
  "[CsvContentTypes](#cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-csvcontenttypes)" : [ String, ... ],
  "[JsonContentTypes](#cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-jsoncontenttypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-inferenceexperiment-capturecontenttypeheader-syntax.yaml"></a>

```
  [CsvContentTypes](#cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-csvcontenttypes): 
    - String
  [JsonContentTypes](#cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-jsoncontenttypes): 
    - String
```

## Properties<a name="aws-properties-sagemaker-inferenceexperiment-capturecontenttypeheader-properties"></a>

`CsvContentTypes`  <a name="cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-csvcontenttypes"></a>
The list of all content type headers that SageMaker will treat as CSV and capture accordingly\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonContentTypes`  <a name="cfn-sagemaker-inferenceexperiment-capturecontenttypeheader-jsoncontenttypes"></a>
The list of all content type headers that SageMaker will treat as JSON and capture accordingly\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)