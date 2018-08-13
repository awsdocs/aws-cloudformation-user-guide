# AWS IoT TopicRule SnsAction<a name="aws-properties-iot-topicrule-snsaction"></a>

`Sns` is a property of the `Actions` property that describes an action that publishes data to an SNS topic\.

## Syntax<a name="w3ab2c21c14e1375b5"></a>

### JSON<a name="aws-properties-iot-topicrule-snsaction-syntax.json"></a>

```
{
  "[MessageFormat](#cfn-iot-topicrule-snsaction-messageformat)": String,
  "[RoleArn](#cfn-iot-topicrule-snsaction-rolearn)": String,
  "[TargetArn](#cfn-iot-topicrule-snsaction-targetarn)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-snsaction-syntax.yaml"></a>

```
[MessageFormat](#cfn-iot-topicrule-snsaction-messageformat): String
[RoleArn](#cfn-iot-topicrule-snsaction-rolearn): String
[TargetArn](#cfn-iot-topicrule-snsaction-targetarn): String
```

## Properties<a name="w3ab2c21c14e1375b7"></a>

`MessageFormat`  <a name="cfn-iot-topicrule-snsaction-messageformat"></a>
The format of the published message\. Amazon SNS uses this setting to determine whether it should parse the payload and extract the platform\-specific bits from the payload\.  
For more information, see [Appendix: Message and JSON Formats](http://docs.aws.amazon.com/sns/latest/dg/json-formats.html) in the *Amazon Simple Notification Service Developer Guide*\.  
*Required*: No  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-snsaction-rolearn"></a>
The ARN of the IAM role that grants access to Amazon SNS\.  
*Required*: Yes  
*Type*: String

`TargetArn`  <a name="cfn-iot-topicrule-snsaction-targetarn"></a>
The ARN of the Amazon SNS topic\.  
*Required*: Yes  
*Type*: String