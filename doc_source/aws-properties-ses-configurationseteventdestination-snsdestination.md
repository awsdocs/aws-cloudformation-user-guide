# AWS::SES::ConfigurationSetEventDestination SnsDestination<a name="aws-properties-ses-configurationseteventdestination-snsdestination"></a>

Contains the topic ARN associated with an Amazon Simple Notification Service \(Amazon SNS\) event destination\.

Event destinations, such as Amazon SNS, are associated with configuration sets, which enable you to publish email sending events\. For information about using configuration sets, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/dg/monitor-sending-activity.html)\.

## Syntax<a name="aws-properties-ses-configurationseteventdestination-snsdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationseteventdestination-snsdestination-syntax.json"></a>

```
{
  "[TopicARN](#cfn-ses-configurationseteventdestination-snsdestination-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-configurationseteventdestination-snsdestination-syntax.yaml"></a>

```
  [TopicARN](#cfn-ses-configurationseteventdestination-snsdestination-topicarn): String
```

## Properties<a name="aws-properties-ses-configurationseteventdestination-snsdestination-properties"></a>

`TopicARN`  <a name="cfn-ses-configurationseteventdestination-snsdestination-topicarn"></a>
The ARN of the Amazon SNS topic for email sending events\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) Amazon SNS operation\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)