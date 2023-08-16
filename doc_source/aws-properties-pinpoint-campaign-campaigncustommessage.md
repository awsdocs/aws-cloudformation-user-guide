# AWS::Pinpoint::Campaign CampaignCustomMessage<a name="aws-properties-pinpoint-campaign-campaigncustommessage"></a>

Specifies the contents of a message that's sent through a custom channel to recipients of a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-campaigncustommessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-campaigncustommessage-syntax.json"></a>

```
{
  "[Data](#cfn-pinpoint-campaign-campaigncustommessage-data)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-campaigncustommessage-syntax.yaml"></a>

```
  [Data](#cfn-pinpoint-campaign-campaigncustommessage-data): String
```

## Properties<a name="aws-properties-pinpoint-campaign-campaigncustommessage-properties"></a>

`Data`  <a name="cfn-pinpoint-campaign-campaigncustommessage-data"></a>
The raw, JSON\-formatted string to use as the payload for the message\. The maximum size is 5 KB\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)