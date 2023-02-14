# AWS::SageMaker::EndpointConfig CaptureContentTypeHeader<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader"></a>

Specifies the JSON and CSV content types of the data that the endpoint captures\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-syntax.json"></a>

```
{
  "[CsvContentTypes](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-csvcontenttypes)" : [ String, ... ],
  "[JsonContentTypes](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-jsoncontenttypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-syntax.yaml"></a>

```
  [CsvContentTypes](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-csvcontenttypes): 
    - String
  [JsonContentTypes](#cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-jsoncontenttypes): 
    - String
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-properties"></a>

`CsvContentTypes`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-csvcontenttypes"></a>
A list of the CSV content types of the data that the endpoint captures\. For the endpoint to capture the data, you must also specify the content type when you invoke the endpoint\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JsonContentTypes`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig-capturecontenttypeheader-jsoncontenttypes"></a>
A list of the JSON content types of the data that the endpoint captures\. For the endpoint to capture the data, you must also specify the content type when you invoke the endpoint\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)