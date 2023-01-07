# AWS::MediaLive::Channel Scte35SpliceInsert<a name="aws-properties-medialive-channel-scte35spliceinsert"></a>

The setup of SCTE\-35 splice insert handling\.

The parent of this entity is AvailSettings\.

## Syntax<a name="aws-properties-medialive-channel-scte35spliceinsert-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-scte35spliceinsert-syntax.json"></a>

```
{
  "[AdAvailOffset](#cfn-medialive-channel-scte35spliceinsert-adavailoffset)" : Integer,
  "[NoRegionalBlackoutFlag](#cfn-medialive-channel-scte35spliceinsert-noregionalblackoutflag)" : String,
  "[WebDeliveryAllowedFlag](#cfn-medialive-channel-scte35spliceinsert-webdeliveryallowedflag)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-scte35spliceinsert-syntax.yaml"></a>

```
  [AdAvailOffset](#cfn-medialive-channel-scte35spliceinsert-adavailoffset): Integer
  [NoRegionalBlackoutFlag](#cfn-medialive-channel-scte35spliceinsert-noregionalblackoutflag): String
  [WebDeliveryAllowedFlag](#cfn-medialive-channel-scte35spliceinsert-webdeliveryallowedflag): String
```

## Properties<a name="aws-properties-medialive-channel-scte35spliceinsert-properties"></a>

`AdAvailOffset`  <a name="cfn-medialive-channel-scte35spliceinsert-adavailoffset"></a>
When specified, this offset \(in milliseconds\) is added to the input ad avail PTS time\. This applies only to embedded SCTE 104/35 messages\. It doesn't apply to OOB messages\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoRegionalBlackoutFlag`  <a name="cfn-medialive-channel-scte35spliceinsert-noregionalblackoutflag"></a>
When set to ignore, segment descriptors with noRegionalBlackoutFlag set to 0 no longer trigger blackouts or ad avail slates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebDeliveryAllowedFlag`  <a name="cfn-medialive-channel-scte35spliceinsert-webdeliveryallowedflag"></a>
When set to ignore, segment descriptors with webDeliveryAllowedFlag set to 0 no longer trigger blackouts or ad avail slates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)