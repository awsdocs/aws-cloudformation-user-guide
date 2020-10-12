# AWS::MediaLive::Channel Scte35TimeSignalApos<a name="aws-properties-medialive-channel-scte35timesignalapos"></a>

Configures the handling of time signals that are in the inputs\. This element belongs to AvailSettings\.

## Syntax<a name="aws-properties-medialive-channel-scte35timesignalapos-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-scte35timesignalapos-syntax.json"></a>

```
{
  "[AdAvailOffset](#cfn-medialive-channel-scte35timesignalapos-adavailoffset)" : Integer,
  "[NoRegionalBlackoutFlag](#cfn-medialive-channel-scte35timesignalapos-noregionalblackoutflag)" : String,
  "[WebDeliveryAllowedFlag](#cfn-medialive-channel-scte35timesignalapos-webdeliveryallowedflag)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-scte35timesignalapos-syntax.yaml"></a>

```
  [AdAvailOffset](#cfn-medialive-channel-scte35timesignalapos-adavailoffset): Integer
  [NoRegionalBlackoutFlag](#cfn-medialive-channel-scte35timesignalapos-noregionalblackoutflag): String
  [WebDeliveryAllowedFlag](#cfn-medialive-channel-scte35timesignalapos-webdeliveryallowedflag): String
```

## Properties<a name="aws-properties-medialive-channel-scte35timesignalapos-properties"></a>

`AdAvailOffset`  <a name="cfn-medialive-channel-scte35timesignalapos-adavailoffset"></a>
When specified, this offset \(in milliseconds\) is added to the input Ad Avail PTS time\. This only applies to embedded SCTE 104/35 messages and does not apply to OOB messages\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoRegionalBlackoutFlag`  <a name="cfn-medialive-channel-scte35timesignalapos-noregionalblackoutflag"></a>
When set to ignore, Segment Descriptors with noRegionalBlackoutFlag set to 0 will no longer trigger blackouts or Ad Avail slates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebDeliveryAllowedFlag`  <a name="cfn-medialive-channel-scte35timesignalapos-webdeliveryallowedflag"></a>
When set to ignore, Segment Descriptors with webDeliveryAllowedFlag set to 0 will no longer trigger blackouts or Ad Avail slates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)