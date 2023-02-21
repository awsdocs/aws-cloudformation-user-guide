# AWS::SupportApp::SlackWorkspaceConfiguration<a name="aws-resource-supportapp-slackworkspaceconfiguration"></a>

You can use the `AWS::SupportApp::SlackWorkspaceConfiguration` resource to specify your Slack workspace configuration\. This resource configures your AWS account so that you can use the specified Slack workspace in the AWS Support App\. This resource includes the following information:
+ The team ID for the Slack workspace
+ The version ID of the resource to use with AWS CloudFormation

For more information, see the following topics in the *AWS Support User Guide*:
+ [AWS Support App in Slack](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-app-for-slack.html)
+ [Creating AWS Support App in Slack resources with AWS CloudFormation](https://docs.aws.amazon.com/awssupport/latest/user/creating-resources-with-cloudformation.html)

## Syntax<a name="aws-resource-supportapp-slackworkspaceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-supportapp-slackworkspaceconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::SupportApp::SlackWorkspaceConfiguration",
  "Properties" : {
      "[TeamId](#cfn-supportapp-slackworkspaceconfiguration-teamid)" : String,
      "[VersionId](#cfn-supportapp-slackworkspaceconfiguration-versionid)" : String
    }
}
```

### YAML<a name="aws-resource-supportapp-slackworkspaceconfiguration-syntax.yaml"></a>

```
Type: AWS::SupportApp::SlackWorkspaceConfiguration
Properties: 
  [TeamId](#cfn-supportapp-slackworkspaceconfiguration-teamid): String
  [VersionId](#cfn-supportapp-slackworkspaceconfiguration-versionid): String
```

## Properties<a name="aws-resource-supportapp-slackworkspaceconfiguration-properties"></a>

`TeamId`  <a name="cfn-supportapp-slackworkspaceconfiguration-teamid"></a>
The team ID in Slack\. This ID uniquely identifies a Slack workspace, such as `T012ABCDEFG`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VersionId`  <a name="cfn-supportapp-slackworkspaceconfiguration-versionid"></a>
An identifier used to update an existing Slack workspace configuration in AWS CloudFormation, such as `100`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-supportapp-slackworkspaceconfiguration-return-values"></a>

### Ref<a name="aws-resource-supportapp-slackworkspaceconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Slack workspace, such as `T012ABCDEFG`\.

For the AWS Support App Slack workspace configuration, `Ref` returns the value of the Slack workspace ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-supportapp-slackworkspaceconfiguration--examples"></a>

The following examples can help you create AWS Support App resources using CloudFormation\.

### Example<a name="aws-resource-supportapp-slackworkspaceconfiguration--examples--Example"></a>

Use this template to create a Slack workspace configuration for your account or your organization\. You must replace the Slack workspace ID\.

#### JSON<a name="aws-resource-supportapp-slackworkspaceconfiguration--examples--Example--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Example stack to create a Slack workspace configuration",
    "Resources": {
        "SlackWorkspaceConfiguration": {
            "Type": "AWS::SupportApp::SlackWorkspaceConfiguration",
            "Properties": {
                "TeamId": "T012ABCDEFG",
                "VersionId": "1"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-supportapp-slackworkspaceconfiguration--examples--Example--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Example stack to create a Slack workspace configuration
Resources:
  SlackWorkspaceConfiguration:
    Type: AWS::SupportApp::SlackWorkspaceConfiguration
    Properties:
      TeamId: T012ABCDEFG
      VersionId: '1'
```