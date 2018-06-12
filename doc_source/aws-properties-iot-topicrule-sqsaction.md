# AWS IoT TopicRule SqsAction<a name="aws-properties-iot-topicrule-sqsaction"></a>

`Sqs` is a property of the `Actions` property that describes an action that publishes data to an SQS queue\.

## Syntax<a name="w3ab2c21c14e1380b5"></a>

### JSON<a name="aws-properties-iot-topicrule-sqsaction-syntax.json"></a>

```
{
  "[QueueUrl](#cfn-iot-topicrule-sqsaction-queueurl)": String,
  "[RoleArn](#cfn-iot-topicrule-sqsaction-rolearn)": String,
  "[UseBase64](#cfn-iot-topicrule-sqsaction-usebase64)": Boolean
}
```

### YAML<a name="aws-properties-iot-topicrule-sqsaction-syntax.yaml"></a>

```
[QueueUrl](#cfn-iot-topicrule-sqsaction-queueurl): String
[RoleArn](#cfn-iot-topicrule-sqsaction-rolearn): String
[UseBase64](#cfn-iot-topicrule-sqsaction-usebase64): Boolean
```

## Properties<a name="w3ab2c21c14e1380b7"></a>

`QueueUrl`  <a name="cfn-iot-topicrule-sqsaction-queueurl"></a>
The URL of the Amazon Simple Queue Service \(Amazon SQS\) queue\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-sqsaction-rolearn"></a>
The ARN of the IAM role that grants access to Amazon SQS\.  
*Required*: Yes  
*Type*: String

`UseBase64`  <a name="cfn-iot-topicrule-sqsaction-usebase64"></a>
Specifies whether Base64 encoding should be used\.  
*Required*: No  
*Type*: Boolean