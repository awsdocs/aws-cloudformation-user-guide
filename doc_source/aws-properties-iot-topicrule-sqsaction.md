# AWS IoT TopicRule SqsAction<a name="aws-properties-iot-topicrule-sqsaction"></a>

`Sqs` is a property of the `Actions` property that describes an action that publishes data to an SQS queue\.

## Syntax<a name="w3ab2c21c14e1183b5"></a>

### JSON<a name="aws-properties-iot-topicrule-sqsaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-queueurl)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-rolearn)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-usebase64)": Boolean
}
```

### YAML<a name="aws-properties-iot-topicrule-sqsaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-queueurl): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-sqsaction-usebase64): Boolean
```

## Properties<a name="w3ab2c21c14e1183b7"></a>

`QueueUrl`  
The URL of the Amazon Simple Queue Service \(Amazon SQS\) queue\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
The ARN of the IAM role that grants access to Amazon SQS\.  
*Required: *Yes  
*Type*: String

`UseBase64`  
Specifies whether Base64 encoding should be used\.  
*Required: *No  
*Type*: Boolean