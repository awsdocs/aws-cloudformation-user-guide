# AWS::SES::ReceiptRule StopAction<a name="aws-properties-ses-receiptrule-stopaction"></a>

When included in a receipt rule, this action terminates the evaluation of the receipt rule set and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\.

For information about setting a stop action in a receipt rule, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-stop.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-stopaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-stopaction-syntax.json"></a>

```
{
  "[Scope](#cfn-ses-receiptrule-stopaction-scope)" : String,
  "[TopicArn](#cfn-ses-receiptrule-stopaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-stopaction-syntax.yaml"></a>

```
  [Scope](#cfn-ses-receiptrule-stopaction-scope): String
  [TopicArn](#cfn-ses-receiptrule-stopaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-stopaction-properties"></a>

`Scope`  <a name="cfn-ses-receiptrule-stopaction-scope"></a>
The scope of the StopAction\. The only acceptable value is `RuleSet`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `RuleSet`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-stopaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the stop action is taken\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)