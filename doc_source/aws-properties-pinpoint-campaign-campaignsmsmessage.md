# AWS::Pinpoint::Campaign CampaignSmsMessage<a name="aws-properties-pinpoint-campaign-campaignsmsmessage"></a>

Specifies the content and settings for an SMS message that's sent to recipients of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax.json"></a>

```
{
  "[Body](#cfn-pinpoint-campaign-campaignsmsmessage-body)" : String,
  "[MessageType](#cfn-pinpoint-campaign-campaignsmsmessage-messagetype)" : String,
  "[SenderId](#cfn-pinpoint-campaign-campaignsmsmessage-senderid)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-syntax.yaml"></a>

```
  [Body](#cfn-pinpoint-campaign-campaignsmsmessage-body): String
  [MessageType](#cfn-pinpoint-campaign-campaignsmsmessage-messagetype): String
  [SenderId](#cfn-pinpoint-campaign-campaignsmsmessage-senderid): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaignsmsmessage-properties"></a>

`Body`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-body"></a>
The body of the SMS message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MessageType`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-messagetype"></a>
The SMS message type\. Valid values are `TRANSACTIONAL` \(for messages that are critical or time\-sensitive, such as a one\-time passwords\) and `PROMOTIONAL` \(for messsages that aren't critical or time\-sensitive, such as marketing messages\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SenderId`  <a name="cfn-pinpoint-campaign-campaignsmsmessage-senderid"></a>
The sender ID to display on recipients' devices when they receive the SMS message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)