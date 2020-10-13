# AWS::MediaLive::Channel EmbeddedSourceSettings<a name="aws-properties-medialive-channel-embeddedsourcesettings"></a>

Specifies how MediaLive will extract the embedded captions from the input\. This element belongs to CaptionSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-embeddedsourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-embeddedsourcesettings-syntax.json"></a>

```
{
  "[Convert608To708](#cfn-medialive-channel-embeddedsourcesettings-convert608to708)" : String,
  "[Scte20Detection](#cfn-medialive-channel-embeddedsourcesettings-scte20detection)" : String,
  "[Source608ChannelNumber](#cfn-medialive-channel-embeddedsourcesettings-source608channelnumber)" : Integer,
  "[Source608TrackNumber](#cfn-medialive-channel-embeddedsourcesettings-source608tracknumber)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-embeddedsourcesettings-syntax.yaml"></a>

```
  [Convert608To708](#cfn-medialive-channel-embeddedsourcesettings-convert608to708): String
  [Scte20Detection](#cfn-medialive-channel-embeddedsourcesettings-scte20detection): String
  [Source608ChannelNumber](#cfn-medialive-channel-embeddedsourcesettings-source608channelnumber): Integer
  [Source608TrackNumber](#cfn-medialive-channel-embeddedsourcesettings-source608tracknumber): Integer
```

## Properties<a name="aws-properties-medialive-channel-embeddedsourcesettings-properties"></a>

`Convert608To708`  <a name="cfn-medialive-channel-embeddedsourcesettings-convert608to708"></a>
If upconvert, 608 data is both passed through via the "608 compatibility bytes" fields of the 708 wrapper as well as translated into 708\. 708 data present in the source content will be discarded\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte20Detection`  <a name="cfn-medialive-channel-embeddedsourcesettings-scte20detection"></a>
Set to "auto" to handle streams with intermittent and/or non\-aligned SCTE\-20 and Embedded captions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source608ChannelNumber`  <a name="cfn-medialive-channel-embeddedsourcesettings-source608channelnumber"></a>
Specifies the 608/708 channel number within the video track from which to extract captions\. Unused for passthrough\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source608TrackNumber`  <a name="cfn-medialive-channel-embeddedsourcesettings-source608tracknumber"></a>
This field is unused and deprecated\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)