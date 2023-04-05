# AWS::Chatbot::MicrosoftTeamsChannelConfiguration<a name="aws-resource-chatbot-microsoftteamschannelconfiguration"></a>

The `AWS::Chatbot::MicrosoftTeamsChannelConfiguration` resource configures a Microsoft Teams channel to allow users to use AWS Chatbot with AWS CloudFormation templates\.

This resource requires some setup to be done in the AWS Chatbot console\. To provide the required Microsoft Teams team and tenant IDs, you must perform the initial authorization flow with Microsoft Teams in the AWS Chatbot console, then copy and paste the IDs from the console\. For more details, see steps 1\-4 in [Setting Up AWS Chatbot with Microsoft Teams](https://docs.aws.amazon.com/chatbot/latest/adminguide/teams-setup.html#teams-client-setup) in the *AWS Chatbot Administrator Guide*\.

## Syntax<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::Chatbot::MicrosoftTeamsChannelConfiguration",
  "Properties" : {
      "[ConfigurationName](#cfn-chatbot-microsoftteamschannelconfiguration-configurationname)" : String,
      "[GuardrailPolicies](#cfn-chatbot-microsoftteamschannelconfiguration-guardrailpolicies)" : [ String, ... ],
      "[IamRoleArn](#cfn-chatbot-microsoftteamschannelconfiguration-iamrolearn)" : String,
      "[LoggingLevel](#cfn-chatbot-microsoftteamschannelconfiguration-logginglevel)" : String,
      "[SnsTopicArns](#cfn-chatbot-microsoftteamschannelconfiguration-snstopicarns)" : [ String, ... ],
      "[TeamId](#cfn-chatbot-microsoftteamschannelconfiguration-teamid)" : String,
      "[TeamsChannelId](#cfn-chatbot-microsoftteamschannelconfiguration-teamschannelid)" : String,
      "[TeamsTenantId](#cfn-chatbot-microsoftteamschannelconfiguration-teamstenantid)" : String,
      "[UserRoleRequired](#cfn-chatbot-microsoftteamschannelconfiguration-userrolerequired)" : Boolean
    }
}
```

### YAML<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-syntax.yaml"></a>

```
Type: AWS::Chatbot::MicrosoftTeamsChannelConfiguration
Properties: 
  [ConfigurationName](#cfn-chatbot-microsoftteamschannelconfiguration-configurationname): String
  [GuardrailPolicies](#cfn-chatbot-microsoftteamschannelconfiguration-guardrailpolicies): 
    - String
  [IamRoleArn](#cfn-chatbot-microsoftteamschannelconfiguration-iamrolearn): String
  [LoggingLevel](#cfn-chatbot-microsoftteamschannelconfiguration-logginglevel): String
  [SnsTopicArns](#cfn-chatbot-microsoftteamschannelconfiguration-snstopicarns): 
    - String
  [TeamId](#cfn-chatbot-microsoftteamschannelconfiguration-teamid): String
  [TeamsChannelId](#cfn-chatbot-microsoftteamschannelconfiguration-teamschannelid): String
  [TeamsTenantId](#cfn-chatbot-microsoftteamschannelconfiguration-teamstenantid): String
  [UserRoleRequired](#cfn-chatbot-microsoftteamschannelconfiguration-userrolerequired): Boolean
```

## Properties<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-properties"></a>

`ConfigurationName`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-configurationname"></a>
The name of the configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GuardrailPolicies`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-guardrailpolicies"></a>
The list of IAM policy ARNs that are applied as channel guardrails\. The AWS managed 'AdministratorAccess' policy is applied as a default if this is not set\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoleArn`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-iamrolearn"></a>
The ARN of the IAM role that defines the permissions for AWS Chatbot\.  
This is a user\-defined role that AWS Chatbot will assume\. This is not the service\-linked role\. For more information, see [IAM Policies for AWS Chatbot](https://docs.aws.amazon.com/chatbot/latest/adminguide/chatbot-iam-policies.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-logginglevel"></a>
Specifies the logging level for this configuration\. This property affects the log entries pushed to Amazon CloudWatch Logs\.  
Logging levels include `ERROR`, `INFO`, or `NONE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicArns`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-snstopicarns"></a>
The ARNs of the SNS topics that deliver notifications to AWS Chatbot\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-teamid"></a>
The ID of the Microsoft Team authorized with AWS Chatbot\.  
To get the team ID, you must perform the initial authorization flow with Microsoft Teams in the AWS Chatbot console\. Then you can copy and paste the team ID from the console\. For more details, see steps 1\-4 in [Get started with Microsoft Teams ](https://docs.aws.amazon.com/chatbot/latest/adminguide/teams-setup.html#teams-client-setup) in the *AWS Chatbot Administrator Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TeamsChannelId`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-teamschannelid"></a>
The ID of the Microsoft Teams channel\.  
To get the channel ID, open Microsoft Teams, right click on the channel name in the left pane, then choose Copy\. An example of the channel ID syntax is: `19%3ab6ef35dc342d56ba5654e6fc6d25a071%40thread.tacv2`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamsTenantId`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-teamstenantid"></a>
The ID of the Microsoft Teams tenant\.  
To get the tenant ID, you must perform the initial authorization flow with Microsoft Teams in the AWS Chatbot console\. Then you can copy and paste the tenant ID from the console\. For more details, see steps 1\-4 in [Get started with Microsoft Teams ](https://docs.aws.amazon.com/chatbot/latest/adminguide/teams-setup.html#teams-client-setup) in the *AWS Chatbot Administrator Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserRoleRequired`  <a name="cfn-chatbot-microsoftteamschannelconfiguration-userrolerequired"></a>
Enables use of a user role requirement in your chat configuration\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-return-values"></a>

### Ref<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic Ref function, Ref returns the ARN of the configuration created\.

### Fn::GetAtt<a name="aws-resource-chatbot-microsoftteamschannelconfiguration-return-values-fn--getatt"></a>

#### <a name="aws-resource-chatbot-microsoftteamschannelconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

## Remarks<a name="aws-resource-chatbot-microsoftteamschannelconfiguration--remarks"></a>

Common troubleshooting scenarios:
+ *I don't have a teams, tenant, or channel ID\.*

  If you don't have one or any of the aforementioned IDs, you must perform the initial authorization flow in the AWS Chatbot console\. Then you will be able to copy and paste the IDs from the console\. For more details, see steps 1\-4 in [Setting Up AWS Chatbot with Microsoft Teams](https://docs.aws.amazon.com/chatbot/latest/adminguide/teams-setup.html#teams-client-setup) in the *AWS Chatbot Administrator Guide*\.
+ *I have already done the initial authorization for my workspace\. Do I need to do it again?*

  No, you can use your existing workspace\. You must log into the AWS Chatbot console to get the workspace ID\.