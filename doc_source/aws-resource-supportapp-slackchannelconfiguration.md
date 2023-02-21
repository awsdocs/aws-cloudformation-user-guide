# AWS::SupportApp::SlackChannelConfiguration<a name="aws-resource-supportapp-slackchannelconfiguration"></a>

You can use the `AWS::SupportApp::SlackChannelConfiguration` resource to specify your AWS account when you configure the AWS Support App\. This resource includes the following information:
+ The Slack channel name and ID
+ The team ID in Slack
+ The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role
+ Whether you want the AWS Support App to notify you when your support cases are created, updated, resolved, or reopened
+ The case severity that you want to get notified for

For more information, see the following topics in the *AWS Support User Guide*:
+ [AWS Support App in Slack](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-app-for-slack.html)
+ [Creating AWS Support App in Slack resources with AWS CloudFormation](https://docs.aws.amazon.com/awssupport/latest/user/creating-resources-with-cloudformation.html)

## Syntax<a name="aws-resource-supportapp-slackchannelconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-supportapp-slackchannelconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::SupportApp::SlackChannelConfiguration",
  "Properties" : {
      "[ChannelId](#cfn-supportapp-slackchannelconfiguration-channelid)" : String,
      "[ChannelName](#cfn-supportapp-slackchannelconfiguration-channelname)" : String,
      "[ChannelRoleArn](#cfn-supportapp-slackchannelconfiguration-channelrolearn)" : String,
      "[NotifyOnAddCorrespondenceToCase](#cfn-supportapp-slackchannelconfiguration-notifyonaddcorrespondencetocase)" : Boolean,
      "[NotifyOnCaseSeverity](#cfn-supportapp-slackchannelconfiguration-notifyoncaseseverity)" : String,
      "[NotifyOnCreateOrReopenCase](#cfn-supportapp-slackchannelconfiguration-notifyoncreateorreopencase)" : Boolean,
      "[NotifyOnResolveCase](#cfn-supportapp-slackchannelconfiguration-notifyonresolvecase)" : Boolean,
      "[TeamId](#cfn-supportapp-slackchannelconfiguration-teamid)" : String
    }
}
```

### YAML<a name="aws-resource-supportapp-slackchannelconfiguration-syntax.yaml"></a>

```
Type: AWS::SupportApp::SlackChannelConfiguration
Properties: 
  [ChannelId](#cfn-supportapp-slackchannelconfiguration-channelid): String
  [ChannelName](#cfn-supportapp-slackchannelconfiguration-channelname): String
  [ChannelRoleArn](#cfn-supportapp-slackchannelconfiguration-channelrolearn): String
  [NotifyOnAddCorrespondenceToCase](#cfn-supportapp-slackchannelconfiguration-notifyonaddcorrespondencetocase): Boolean
  [NotifyOnCaseSeverity](#cfn-supportapp-slackchannelconfiguration-notifyoncaseseverity): String
  [NotifyOnCreateOrReopenCase](#cfn-supportapp-slackchannelconfiguration-notifyoncreateorreopencase): Boolean
  [NotifyOnResolveCase](#cfn-supportapp-slackchannelconfiguration-notifyonresolvecase): Boolean
  [TeamId](#cfn-supportapp-slackchannelconfiguration-teamid): String
```

## Properties<a name="aws-resource-supportapp-slackchannelconfiguration-properties"></a>

`ChannelId`  <a name="cfn-supportapp-slackchannelconfiguration-channelid"></a>
The channel ID in Slack\. This ID identifies a channel within a Slack workspace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ChannelName`  <a name="cfn-supportapp-slackchannelconfiguration-channelname"></a>
The channel name in Slack\. This is the channel where you invite the AWS Support App\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelRoleArn`  <a name="cfn-supportapp-slackchannelconfiguration-channelrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role for this Slack channel configuration\. The AWS Support App uses this role to perform AWS Support and Service Quotas actions on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotifyOnAddCorrespondenceToCase`  <a name="cfn-supportapp-slackchannelconfiguration-notifyonaddcorrespondencetocase"></a>
Whether to get notified when a correspondence is added to your support cases\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotifyOnCaseSeverity`  <a name="cfn-supportapp-slackchannelconfiguration-notifyoncaseseverity"></a>
The case severity for your support cases that you want to receive notifications\. You can specify `none`, `all`, or `high`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotifyOnCreateOrReopenCase`  <a name="cfn-supportapp-slackchannelconfiguration-notifyoncreateorreopencase"></a>
Whether to get notified when your support cases are created or reopened  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotifyOnResolveCase`  <a name="cfn-supportapp-slackchannelconfiguration-notifyonresolvecase"></a>
Whether to get notified when your support cases are resolved\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeamId`  <a name="cfn-supportapp-slackchannelconfiguration-teamid"></a>
The team ID in Slack\. This ID uniquely identifies a Slack workspace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-supportapp-slackchannelconfiguration--examples"></a>

The following examples can help you create AWS Support App resources using CloudFormation\.

### Example<a name="aws-resource-supportapp-slackchannelconfiguration--examples--Example"></a>

Use this template to create a Slack channel configuration and IAM role for your account or your organization\. You must replace the Slack workspace and channel IDs\.

#### JSON<a name="aws-resource-supportapp-slackchannelconfiguration--examples--Example--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Example stack to create a Slack channel configuration",
    "Resources": {
        "SlackChannelConfiguration": {
            "Type": "AWS::SupportApp::SlackChannelConfiguration",
            "Properties": {
                "TeamId": "T012ABCDEFG",
                "ChannelId": "C01234A5BCD",
                "ChannelName": "cloudformationtemplatechannel",
                "NotifyOnCreateOrReopenCase": true,
                "NotifyOnAddCorrespondenceToCase": false,
                "NotifyOnResolveCase": true,
                "NotifyOnCaseSeverity": "high",
                "ChannelRoleArn": {"Fn::GetAtt" : ["AWSSupportSlackAppCFNRole", "Arn"] }
            }
        },
        "AWSSupportSlackAppCFNRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "supportapp.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/AWSSupportAppFullAccess"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-supportapp-slackchannelconfiguration--examples--Example--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Example stack to create a Slack channel configuration
Resources:
  SlackChannelConfiguration:
    Type: AWS::SupportApp::SlackChannelConfiguration
    Properties:
      TeamId: T012ABCDEFG
      ChannelId: C01234A5BCD
      ChannelName: cfntemplatechannel
      NotifyOnCreateOrReopenCase: true
      NotifyOnAddCorrespondenceToCase: false
      NotifyOnResolveCase: true
      NotifyOnCaseSeverity: high
      ChannelRoleArn: !GetAtt 'AWSSupportSlackAppCFNRole.Arn'
  AWSSupportSlackAppCFNRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: '2012-10-17'
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - supportapp.amazonaws.com
            Action:
              - sts:AssumeRole
      ManagedPolicyArns:
        - arn:aws:iam::aws:policy/AWSSupportAppFullAccess
```