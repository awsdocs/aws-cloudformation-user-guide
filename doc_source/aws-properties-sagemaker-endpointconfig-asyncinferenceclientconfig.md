# AWS::SageMaker::EndpointConfig AsyncInferenceClientConfig<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig"></a>

Configures the behavior of the client used by SageMaker to interact with the model container during asynchronous inference\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig-syntax.json"></a>

```
{
  "[MaxConcurrentInvocationsPerInstance](#cfn-sagemaker-endpointconfig-asyncinferenceclientconfig-maxconcurrentinvocationsperinstance)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig-syntax.yaml"></a>

```
  [MaxConcurrentInvocationsPerInstance](#cfn-sagemaker-endpointconfig-asyncinferenceclientconfig-maxconcurrentinvocationsperinstance): Integer
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig-properties"></a>

`MaxConcurrentInvocationsPerInstance`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceclientconfig-maxconcurrentinvocationsperinstance"></a>
The maximum number of concurrent requests sent by the SageMaker client to the model container\. If no value is provided, SageMaker will choose an optimal value for you\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)