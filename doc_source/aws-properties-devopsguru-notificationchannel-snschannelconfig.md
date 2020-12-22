# AWS::DevOpsGuru::NotificationChannel SnsChannelConfig<a name="aws-properties-devopsguru-notificationchannel-snschannelconfig"></a>

 Contains the Amazon Resource Name \(ARN\) of an Amazon Simple Notification Service topic\. 

If you use an Amazon SNS topic in another account, you must attach a policy to it that grants DevOps Guru permission to it notifications\. DevOps Guru adds the required policy on your behalf to send notifications using Amazon SNS in your account\. For more information, see [Permissions for cross account Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-required-permissions.html)\.

If you use an Amazon SNS topic that is encrypted by an AWS Key Management Service customer\-managed key \(CMK\), then you must add permissions to the CMK\. For more information, see [Permissions for AWS KMS–encrypted Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-kms-permissions.html)\.

## Syntax<a name="aws-properties-devopsguru-notificationchannel-snschannelconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devopsguru-notificationchannel-snschannelconfig-syntax.json"></a>

```
{
  "[TopicArn](#cfn-devopsguru-notificationchannel-snschannelconfig-topicarn)" : String
}
```

### YAML<a name="aws-properties-devopsguru-notificationchannel-snschannelconfig-syntax.yaml"></a>

```
  [TopicArn](#cfn-devopsguru-notificationchannel-snschannelconfig-topicarn): String
```

## Properties<a name="aws-properties-devopsguru-notificationchannel-snschannelconfig-properties"></a>

`TopicArn`  <a name="cfn-devopsguru-notificationchannel-snschannelconfig-topicarn"></a>
 The Amazon Resource Name \(ARN\) of an Amazon Simple Notification Service topic\.   
*Required*: No  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `1024`  
*Pattern*: `^arn:aws[a-z0-9-]*:sns:[a-z0-9-]+:\d{12}:[^:]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)