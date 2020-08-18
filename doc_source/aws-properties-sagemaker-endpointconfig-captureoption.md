# AWS::SageMaker::EndpointConfig CaptureOption<a name="aws-properties-sagemaker-endpointconfig-captureoption"></a>

Specifies whether the endpoint captures input data or output data\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-captureoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-captureoption-syntax.json"></a>

```
{
  "[CaptureMode](#cfn-sagemaker-endpointconfig-captureoption-capturemode)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-captureoption-syntax.yaml"></a>

```
  [CaptureMode](#cfn-sagemaker-endpointconfig-captureoption-capturemode): String
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-captureoption-properties"></a>

`CaptureMode`  <a name="cfn-sagemaker-endpointconfig-captureoption-capturemode"></a>
Specifies whether the endpoint captures input data or output data\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Input | Output`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)