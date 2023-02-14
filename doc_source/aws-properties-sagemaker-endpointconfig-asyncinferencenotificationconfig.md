# AWS::SageMaker::EndpointConfig AsyncInferenceNotificationConfig<a name="aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig"></a>

Specifies the configuration for notifications of inference results for asynchronous inference\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig-syntax.json"></a>

```
{
  "[ErrorTopic](#cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-errortopic)" : String,
  "[SuccessTopic](#cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-successtopic)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig-syntax.yaml"></a>

```
  [ErrorTopic](#cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-errortopic): String
  [SuccessTopic](#cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-successtopic): String
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig-properties"></a>

`ErrorTopic`  <a name="cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-errortopic"></a>
Amazon SNS topic to post a notification to when an inference fails\. If no topic is provided, no notification is sent on failure\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SuccessTopic`  <a name="cfn-sagemaker-endpointconfig-asyncinferencenotificationconfig-successtopic"></a>
Amazon SNS topic to post a notification to when an inference completes successfully\. If no topic is provided, no notification is sent on success\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)