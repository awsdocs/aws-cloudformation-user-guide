# AWS::DevOpsGuru::NotificationChannel NotificationChannelConfig<a name="aws-properties-devopsguru-notificationchannel-notificationchannelconfig"></a>

 Information about notification channels you have configured with DevOps Guru\. The one supported notification channel is Amazon Simple Notification Service \(Amazon SNS\)\.

## Syntax<a name="aws-properties-devopsguru-notificationchannel-notificationchannelconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devopsguru-notificationchannel-notificationchannelconfig-syntax.json"></a>

```
{
  "[Filters](#cfn-devopsguru-notificationchannel-notificationchannelconfig-filters)" : NotificationFilterConfig,
  "[Sns](#cfn-devopsguru-notificationchannel-notificationchannelconfig-sns)" : SnsChannelConfig
}
```

### YAML<a name="aws-properties-devopsguru-notificationchannel-notificationchannelconfig-syntax.yaml"></a>

```
  [Filters](#cfn-devopsguru-notificationchannel-notificationchannelconfig-filters): 
    NotificationFilterConfig
  [Sns](#cfn-devopsguru-notificationchannel-notificationchannelconfig-sns): 
    SnsChannelConfig
```

## Properties<a name="aws-properties-devopsguru-notificationchannel-notificationchannelconfig-properties"></a>

`Filters`  <a name="cfn-devopsguru-notificationchannel-notificationchannelconfig-filters"></a>
 The filter configurations for the Amazon SNS notification topic you use with DevOps Guru\. If you do not provide filter configurations, the default configurations are to receive notifications for all message types of `High` or `Medium` severity\.   
*Required*: No  
*Type*: [NotificationFilterConfig](aws-properties-devopsguru-notificationchannel-notificationfilterconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Sns`  <a name="cfn-devopsguru-notificationchannel-notificationchannelconfig-sns"></a>
 Information about a notification channel configured in DevOps Guru to send notifications when insights are created\.   
If you use an Amazon SNS topic in another account, you must attach a policy to it that grants DevOps Guru permission to send it notifications\. DevOps Guru adds the required policy on your behalf to send notifications using Amazon SNS in your account\. DevOps Guru only supports standard SNS topics\. For more information, see [Permissions for Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-required-permissions.html)\.  
If you use an Amazon SNS topic that is encrypted by an AWS Key Management Service customer\-managed key \(CMK\), then you must add permissions to the CMK\. For more information, see [Permissions for AWS KMS–encrypted Amazon SNS topics](https://docs.aws.amazon.com/devops-guru/latest/userguide/sns-kms-permissions.html)\.  
*Required*: No  
*Type*: [SnsChannelConfig](aws-properties-devopsguru-notificationchannel-snschannelconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)