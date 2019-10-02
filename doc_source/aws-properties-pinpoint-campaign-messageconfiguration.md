# AWS::Pinpoint::Campaign MessageConfiguration<a name="aws-properties-pinpoint-campaign-messageconfiguration"></a>

Specifies the message configuration settings for a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax.json"></a>

```
{
  "[ADMMessage](#cfn-pinpoint-campaign-messageconfiguration-admmessage)" : [Message](aws-properties-pinpoint-campaign-message.md),
  "[APNSMessage](#cfn-pinpoint-campaign-messageconfiguration-apnsmessage)" : [Message](aws-properties-pinpoint-campaign-message.md),
  "[BaiduMessage](#cfn-pinpoint-campaign-messageconfiguration-baidumessage)" : [Message](aws-properties-pinpoint-campaign-message.md),
  "[DefaultMessage](#cfn-pinpoint-campaign-messageconfiguration-defaultmessage)" : [Message](aws-properties-pinpoint-campaign-message.md),
  "[EmailMessage](#cfn-pinpoint-campaign-messageconfiguration-emailmessage)" : [CampaignEmailMessage](aws-properties-pinpoint-campaign-campaignemailmessage.md),
  "[GCMMessage](#cfn-pinpoint-campaign-messageconfiguration-gcmmessage)" : [Message](aws-properties-pinpoint-campaign-message.md),
  "[SMSMessage](#cfn-pinpoint-campaign-messageconfiguration-smsmessage)" : [CampaignSmsMessage](aws-properties-pinpoint-campaign-campaignsmsmessage.md)
}
```

### YAML<a name="aws-properties-pinpoint-campaign-messageconfiguration-syntax.yaml"></a>

```
  [ADMMessage](#cfn-pinpoint-campaign-messageconfiguration-admmessage): 
    [Message](aws-properties-pinpoint-campaign-message.md)
  [APNSMessage](#cfn-pinpoint-campaign-messageconfiguration-apnsmessage): 
    [Message](aws-properties-pinpoint-campaign-message.md)
  [BaiduMessage](#cfn-pinpoint-campaign-messageconfiguration-baidumessage): 
    [Message](aws-properties-pinpoint-campaign-message.md)
  [DefaultMessage](#cfn-pinpoint-campaign-messageconfiguration-defaultmessage): 
    [Message](aws-properties-pinpoint-campaign-message.md)
  [EmailMessage](#cfn-pinpoint-campaign-messageconfiguration-emailmessage): 
    [CampaignEmailMessage](aws-properties-pinpoint-campaign-campaignemailmessage.md)
  [GCMMessage](#cfn-pinpoint-campaign-messageconfiguration-gcmmessage): 
    [Message](aws-properties-pinpoint-campaign-message.md)
  [SMSMessage](#cfn-pinpoint-campaign-messageconfiguration-smsmessage): 
    [CampaignSmsMessage](aws-properties-pinpoint-campaign-campaignsmsmessage.md)
```

## Properties<a name="aws-properties-pinpoint-campaign-messageconfiguration-properties"></a>

`ADMMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-admmessage"></a>
The message that the campaign sends through the ADM \(Amazon Device Messaging\) channel\. This message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`APNSMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-apnsmessage"></a>
The message that the campaign sends through the APNS \(Apple Push Notification service\) channel\. This message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaiduMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-baidumessage"></a>
The message that the campaign sends through the Baidu \(Baidu Cloud Push\) channel\. This message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-defaultmessage"></a>
The default message that the campaign sends through all the channels that are configured for the campaign\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-emailmessage"></a>
The message that the campaign sends through the email channel\.  
*Required*: No  
*Type*: [CampaignEmailMessage](aws-properties-pinpoint-campaign-campaignemailmessage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GCMMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-gcmmessage"></a>
The message that the campaign sends through the GCM channel, which enables Amazon Pinpoint to send push notifications through the Firebase Cloud Messaging \(FCM\), formerly Google Cloud Messaging \(GCM\), service\. This message overrides the default message\.  
*Required*: No  
*Type*: [Message](aws-properties-pinpoint-campaign-message.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SMSMessage`  <a name="cfn-pinpoint-campaign-messageconfiguration-smsmessage"></a>
The message that the campaign sends through the SMS channel\.  
*Required*: No  
*Type*: [CampaignSmsMessage](aws-properties-pinpoint-campaign-campaignsmsmessage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
