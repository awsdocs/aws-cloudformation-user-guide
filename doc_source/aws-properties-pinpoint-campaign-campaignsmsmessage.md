# AWS::Pinpoint::Campaign CampaignSmsMessage<a name="aws-properties-pinpoint-campaign-campaignsmsmessage"></a>

Specifies the content and settings for an SMS message that's sent to recipients of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax.json"></a>

```
{
  "[Body](#cfn-pinpoint-campaign-campaignsmsmessage-body)" : String,
  "[EntityId](#cfn-pinpoint-campaign-campaignsmsmessage-entityid)" : String,
  "[MessageType](#cfn-pinpoint-campaign-campaignsmsmessage-messagetype)" : String,
  "[OriginationNumber](#cfn-pinpoint-campaign-campaignsmsmessage-originationnumber)" : String,
  "[SenderId](#cfn-pinpoint-campaign-campaignsmsmessage-senderid)" : String,
  "[TemplateId](#cfn-pinpoint-campaign-campaignsmsmessage-templateid)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax.yaml"></a>

```
  [Body](#cfn-pinpoint-campaign-campaignsmsmessage-body): String
  [EntityId](#cfn-pinpoint-campaign-campaignsmsmessage-entityid): String
  [MessageType](#cfn-pinpoint-campaign-campaignsmsmessage-messagetype): String
  [OriginationNumber](#cfn-pinpoint-campaign-campaignsmsmessage-originationnumber): String
  [SenderId](#cfn-pinpoint-campaign-campaignsmsmessage-senderid): String
  [TemplateId](#cfn-pinpoint-campaign-campaignsmsmessage-templateid): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-properties"></a>

`Body`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-body"></a>
The body of the SMS message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityId`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-entityid"></a>
The entity ID or Principal Entity \(PE\) id received from the regulatory body for sending SMS in your country\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageType`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-messagetype"></a>
The SMS message type\. Valid values are `TRANSACTIONAL` \(for messages that are critical or time\-sensitive, such as a one\-time passwords\) and `PROMOTIONAL` \(for messsages that aren't critical or time\-sensitive, such as marketing messages\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginationNumber`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-originationnumber"></a>
The long code to send the SMS message from\. This value should be one of the dedicated long codes that's assigned to your AWS account\. Although it isn't required, we recommend that you specify the long code using an E\.164 format to ensure prompt and accurate delivery of the message\. For example, \+12065550100\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SenderId`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-senderid"></a>
The alphabetic Sender ID to display as the sender of the message on a recipient's device\. Support for sender IDs varies by country or region\. To specify a phone number as the sender, omit this parameter and use `OriginationNumber` instead\. For more information about support for Sender ID by country, see the [Amazon Pinpoint User Guide](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-sms-countries.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateId`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-templateid"></a>
The template ID received from the regulatory body for sending SMS in your country\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)