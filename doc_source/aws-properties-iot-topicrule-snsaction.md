# AWS::IoT::TopicRule SnsAction<a name="aws-properties-iot-topicrule-snsaction"></a>

Describes an action to publish to an Amazon SNS topic\.

## Syntax<a name="aws-properties-iot-topicrule-snsaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-snsaction-syntax.json"></a>

```
{
  "[MessageFormat](#cfn-iot-topicrule-snsaction-messageformat)" : String,
  "[RoleArn](#cfn-iot-topicrule-snsaction-rolearn)" : String,
  "[TargetArn](#cfn-iot-topicrule-snsaction-targetarn)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-snsaction-syntax.yaml"></a>

```
  [MessageFormat](#cfn-iot-topicrule-snsaction-messageformat): String
  [RoleArn](#cfn-iot-topicrule-snsaction-rolearn): String
  [TargetArn](#cfn-iot-topicrule-snsaction-targetarn): String
```

## Properties<a name="aws-properties-iot-topicrule-snsaction-properties"></a>

`MessageFormat`  <a name="cfn-iot-topicrule-snsaction-messageformat"></a>
\(Optional\) The message format of the message to publish\. Accepted values are "JSON" and "RAW"\. The default value of the attribute is "RAW"\. SNS uses this setting to determine if the payload should be parsed and relevant platform\-specific bits of the payload should be extracted\. For more information, see [Amazon SNS Message and JSON Formats](https://docs.aws.amazon.com/sns/latest/dg/json-formats.html) in the *Amazon Simple Notification Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-snsaction-rolearn"></a>
The ARN of the IAM role that grants access\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iot-topicrule-snsaction-targetarn"></a>
The ARN of the SNS topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)