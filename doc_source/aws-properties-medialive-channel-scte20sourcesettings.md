# AWS::MediaLive::Channel Scte20SourceSettings<a name="aws-properties-medialive-channel-scte20sourcesettings"></a>

Scte20 Source Settings

## Syntax<a name="aws-properties-medialive-channel-scte20sourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-scte20sourcesettings-syntax.json"></a>

```
{
  "[Convert608To708](#cfn-medialive-channel-scte20sourcesettings-convert608to708)" : String,
  "[Source608ChannelNumber](#cfn-medialive-channel-scte20sourcesettings-source608channelnumber)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-scte20sourcesettings-syntax.yaml"></a>

```
  [Convert608To708](#cfn-medialive-channel-scte20sourcesettings-convert608to708): String
  [Source608ChannelNumber](#cfn-medialive-channel-scte20sourcesettings-source608channelnumber): Integer
```

## Properties<a name="aws-properties-medialive-channel-scte20sourcesettings-properties"></a>

`Convert608To708`  <a name="cfn-medialive-channel-scte20sourcesettings-convert608to708"></a>
If upconvert, 608 data is both passed through via the "608 compatibility bytes" fields of the 708 wrapper as well as translated into 708\. 708 data present in the source content will be discarded\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source608ChannelNumber`  <a name="cfn-medialive-channel-scte20sourcesettings-source608channelnumber"></a>
Specifies the 608/708 channel number within the video track from which to extract captions\. Unused for passthrough\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)