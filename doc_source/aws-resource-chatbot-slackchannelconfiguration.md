# AWS::Chatbot::SlackChannelConfiguration<a name="aws-resource-chatbot-slackchannelconfiguration"></a>

The `AWS::Chatbot::SlackChannelConfiguration` resource configures a Slack channel to allow users to use AWS Chatbot with AWS CloudFormation templates\.

This resource requires some setup to be done in the AWS Chatbot console\. To provide the required Slack workspace ID, you must perform the initial authorization flow with Slack in the AWS Chatbot console, then copy and paste the workspace ID from the console\. For more details, see steps 1\-4 in [Setting Up AWS Chatbot with Slack](https://docs.aws.amazon.com/chatbot/latest/adminguide/setting-up.html#Setup_intro) in the *AWS Chatbot User Guide*\.

## Syntax<a name="aws-resource-chatbot-slackchannelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-chatbot-slackchannelconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::Chatbot::SlackChannelConfiguration",
  "Properties" : {
      "[ConfigurationName](#cfn-chatbot-slackchannelconfiguration-configurationname)" : String,
      "[IamRoleArn](#cfn-chatbot-slackchannelconfiguration-iamrolearn)" : String,
      "[LoggingLevel](#cfn-chatbot-slackchannelconfiguration-logginglevel)" : String,
      "[SlackChannelId](#cfn-chatbot-slackchannelconfiguration-slackchannelid)" : String,
      "[SlackWorkspaceId](#cfn-chatbot-slackchannelconfiguration-slackworkspaceid)" : String,
      "[SnsTopicArns](#cfn-chatbot-slackchannelconfiguration-snstopicarns)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-chatbot-slackchannelconfiguration-syntax.yaml"></a>

```
Type: AWS::Chatbot::SlackChannelConfiguration
Properties: 
  [ConfigurationName](#cfn-chatbot-slackchannelconfiguration-configurationname): String
  [IamRoleArn](#cfn-chatbot-slackchannelconfiguration-iamrolearn): String
  [LoggingLevel](#cfn-chatbot-slackchannelconfiguration-logginglevel): String
  [SlackChannelId](#cfn-chatbot-slackchannelconfiguration-slackchannelid): String
  [SlackWorkspaceId](#cfn-chatbot-slackchannelconfiguration-slackworkspaceid): String
  [SnsTopicArns](#cfn-chatbot-slackchannelconfiguration-snstopicarns): 
    - String
```

## Properties<a name="aws-resource-chatbot-slackchannelconfiguration-properties"></a>

`ConfigurationName`  <a name="cfn-chatbot-slackchannelconfiguration-configurationname"></a>
The name of the configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamRoleArn`  <a name="cfn-chatbot-slackchannelconfiguration-iamrolearn"></a>
The ARN of the IAM role that defines the permissions for AWS Chatbot\.  
This is a user\-defined role that AWS Chatbot will assume\. This is not the service\-linked role\. For more information, see [IAM Policies for AWS Chatbot](https://docs.aws.amazon.com/chatbot/latest/adminguide/chatbot-iam-policies.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-chatbot-slackchannelconfiguration-logginglevel"></a>
Specifies the logging level for this configuration\. This property affects the log entries pushed to Amazon CloudWatch Logs\.  
Logging levels include `ERROR`, `INFO`, or `NONE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlackChannelId`  <a name="cfn-chatbot-slackchannelconfiguration-slackchannelid"></a>
The ID of the Slack channel\.  
To get the ID, open Slack, right click on the channel name in the left pane, then choose Copy Link\. The channel ID is the 9\-character string at the end of the URL\. For example, `ABCBBLZZZ`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlackWorkspaceId`  <a name="cfn-chatbot-slackchannelconfiguration-slackworkspaceid"></a>
The ID of the Slack workspace authorized with AWS Chatbot\.  
To get the workspace ID, you must perform the initial authorization flow with Slack in the AWS Chatbot console\. Then you can copy and paste the workspace ID from the console\. For more details, see steps 1\-4 in [Setting Up AWS Chatbot with Slack](https://docs.aws.amazon.com/chatbot/latest/adminguide/setting-up.html#Setup_intro) in the *AWS Chatbot User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnsTopicArns`  <a name="cfn-chatbot-slackchannelconfiguration-snstopicarns"></a>
The ARNs of the SNS topics that deliver notifications to AWS Chatbot\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-chatbot-slackchannelconfiguration-return-values"></a>

### Ref<a name="aws-resource-chatbot-slackchannelconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic Ref function, Ref returns the ARN of the configuration created\.

### Fn::GetAtt<a name="aws-resource-chatbot-slackchannelconfiguration-return-values-fn--getatt"></a>

#### <a name="aws-resource-chatbot-slackchannelconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Remarks<a name="aws-resource-chatbot-slackchannelconfiguration--remarks"></a>

Common troubleshooting scenarios:
+ *I don't have a workspace ID\.*

  If you don't have a workspace ID, you must perform the initial authorization flow in the AWS Chatbot console\. Then you will be able to copy and paste the workspace ID from the console\. For more details, see steps 1\-4 in [Setting Up AWS Chatbot with Slack](https://docs.aws.amazon.com/chatbot/latest/adminguide/setting-up.html#Setup_intro) in the *AWS Chatbot User Guide*\. 
+ *I have already done the initial authorization for my workspace\. Do I need to do it again?*

  No, you can use your existing workspace\. You must log into the AWS Chatbot console to get the workspace ID\.