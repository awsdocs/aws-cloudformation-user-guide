# AWS::Pinpoint::Campaign MessageConfiguration<a name="aws-properties-pinpoint-campaign-messageconfiguration"></a>

Specifies the message configuration settings for a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax.json"></a>

```
{
  "[ADMMessage](#cfn-pinpoint-campaign-messageconfiguration-admmessage)" : Message,
  "[APNSMessage](#cfn-pinpoint-campaign-messageconfiguration-apnsmessage)" : Message,
  "[BaiduMessage](#cfn-pinpoint-campaign-messageconfiguration-baidumessage)" : Message,
  "[DefaultMessage](#cfn-pinpoint-campaign-messageconfiguration-defaultmessage)" : Message,
  "[EmailMessage](#cfn-pinpoint-campaign-messageconfiguration-emailmessage)" : CampaignEmailMessage,
  "[GCMMessage](#cfn-pinpoint-campaign-messageconfiguration-gcmmessage)" : Message,
  "[SMSMessage](#cfn-pinpoint-campaign-messageconfiguration-smsmessage)" : CampaignSmsMessage
}
```

### YAML<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax.yaml"></a>

```
  [ADMMessage](#cfn-pinpoint-campaign-messageconfiguration-admmessage): 
    Message
  [APNSMessage](#cfn-pinpoint-campaign-messageconfiguration-apnsmessage): 
    Message
  [BaiduMessage](#cfn-pinpoint-campaign-messageconfiguration-baidumessage): 
    Message
  [DefaultMessage](#cfn-pinpoint-campaign-messageconfiguration-defaultmessage): 
    Message
  [EmailMessage](#cfn-pinpoint-campaign-messageconfiguration-emailmessage): 
    CampaignEmailMessage
  [GCMMessage](#cfn-pinpoint-campaign-messageconfiguration-gcmmessage): 
    Message
  [SMSMessage](#cfn-pinpoint-campaign-messageconfiguration-smsmessage): 
    CampaignSmsMessage
```

## Properties<a name="aws-properties-pinpoint-campaign-messageconfiguration-properties"></a>

`ADMMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-admmessage"></a>
The message that the campaign sends through the ADM \(Amazon Device Messaging\) channel\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`APNSMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-apnsmessage"></a>
The message that the campaign sends through the APNs \(Apple Push Notification service\) channel\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaiduMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-baidumessage"></a>
The message that the campaign sends through the Baidu \(Baidu Cloud Push\) channel\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-defaultmessage"></a>
The default message that the campaign sends through all the channels that are configured for the campaign\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-emailmessage"></a>
The message that the campaign sends through the email channel\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [CampaignEmailMessage](aws-properties-pinpoint-campaign-campaignemailmessage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GCMMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-gcmmessage"></a>
The message that the campaign sends through the GCM channel, which enables Amazon Pinpoint to send push notifications through the Firebase Cloud Messaging \(FCM\), formerly Google Cloud Messaging \(GCM\), service\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SMSMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-smsmessage"></a>
The message that the campaign sends through the SMS channel\. If specified, this message overrides the default message\.  
*Required*: No  
*Type*: [CampaignSmsMessage](aws-properties-pinpoint-campaign-campaignsmsmessage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)