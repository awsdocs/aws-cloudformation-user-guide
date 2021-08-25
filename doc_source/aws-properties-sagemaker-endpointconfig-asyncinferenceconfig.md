# AWS::SageMaker::EndpointConfig AsyncInferenceConfig<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceconfig"></a>

Specifies configuration for how an endpoint performs asynchronous inference\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceconfig-syntax.json"></a>

```
{
  "[ClientConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig-clientconfig)" : AsyncInferenceClientConfig,
  "[OutputConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig-outputconfig)" : AsyncInferenceOutputConfig
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceconfig-syntax.yaml"></a>

```
  [ClientConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig-clientconfig): 
    AsyncInferenceClientConfig
  [OutputConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig-outputconfig): 
    AsyncInferenceOutputConfig
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceconfig-properties"></a>

`ClientConfig`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceconfig-clientconfig"></a>
Configures the behavior of the client used by SageMaker to interact with the model container during asynchronous inference\.  
*Required*: No  
*Type*: [AsyncInferenceClientConfig](aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutputConfig`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceconfig-outputconfig"></a>
Specifies the configuration for asynchronous inference invocation outputs\.  
*Required*: Yes  
*Type*: [AsyncInferenceOutputConfig](aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)