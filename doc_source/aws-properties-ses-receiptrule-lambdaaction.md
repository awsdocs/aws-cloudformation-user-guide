# AWS::SES::ReceiptRule LambdaAction<a name="aws-properties-ses-receiptrule-lambdaaction"></a>

When included in a receipt rule, this action calls an AWS Lambda function and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\.

To enable Amazon SES to call your AWS Lambda function or to publish to an Amazon SNS topic of another account, Amazon SES must have permission to access those resources\. For information about giving permissions, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-permissions.html)\.

For information about using AWS Lambda actions in receipt rules, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-lambda.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-lambdaaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-lambdaaction-syntax.json"></a>

```
{
  "[FunctionArn](#cfn-ses-receiptrule-lambdaaction-functionarn)" : String,
  "[InvocationType](#cfn-ses-receiptrule-lambdaaction-invocationtype)" : String,
  "[TopicArn](#cfn-ses-receiptrule-lambdaaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-lambdaaction-syntax.yaml"></a>

```
  [FunctionArn](#cfn-ses-receiptrule-lambdaaction-functionarn): String
  [InvocationType](#cfn-ses-receiptrule-lambdaaction-invocationtype): String
  [TopicArn](#cfn-ses-receiptrule-lambdaaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-lambdaaction-properties"></a>

`FunctionArn`  <a name="cfn-ses-receiptrule-lambdaaction-functionarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function\. An example of an AWS Lambda function ARN is `arn:aws:lambda:us-west-2:account-id:function:MyFunction`\. For more information about AWS Lambda, see the [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationType`  <a name="cfn-ses-receiptrule-lambdaaction-invocationtype"></a>
The invocation type of the AWS Lambda function\. An invocation type of `RequestResponse` means that the execution of the function immediately results in a response, and a value of `Event` means that the function is invoked asynchronously\. The default value is `Event`\. For information about AWS Lambda invocation types, see the [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/API_Invoke.html)\.  
There is a 30\-second timeout on `RequestResponse` invocations\. You should use `Event` invocation in most cases\. Use `RequestResponse` only when you want to make a mail flow decision, such as whether to stop the receipt rule or the receipt rule set\.
*Required*: No  
*Type*: String  
*Allowed values*: `Event | RequestResponse`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-lambdaaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the Lambda action is executed\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)