# AWS::PinpointEmail::ConfigurationSetEventDestination SnsDestination<a name="aws-properties-pinpointemail-configurationseteventdestination-snsdestination"></a>

An object that defines an Amazon SNS destination for email events\. You can use Amazon SNS to send notification when certain email events occur\.

## Syntax<a name="aws-properties-pinpointemail-configurationseteventdestination-snsdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationseteventdestination-snsdestination-syntax.json"></a>

```
{
  "[TopicArn](#cfn-pinpointemail-configurationseteventdestination-snsdestination-topicarn)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-configurationseteventdestination-snsdestination-syntax.yaml"></a>

```
  [TopicArn](#cfn-pinpointemail-configurationseteventdestination-snsdestination-topicarn): String
```

## Properties<a name="aws-properties-pinpointemail-configurationseteventdestination-snsdestination-properties"></a>

`TopicArn`  <a name="cfn-pinpointemail-configurationseteventdestination-snsdestination-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic that you want to publish email events to\. For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)