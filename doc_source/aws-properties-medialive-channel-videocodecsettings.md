# AWS::MediaLive::Channel VideoCodecSettings<a name="aws-properties-medialive-channel-videocodecsettings"></a>

The settings for the video codec in the output\.

The parent of this entity is VideoDescription\.

## Syntax<a name="aws-properties-medialive-channel-videocodecsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videocodecsettings-syntax.json"></a>

```
{
  "[FrameCaptureSettings](#cfn-medialive-channel-videocodecsettings-framecapturesettings)" : FrameCaptureSettings,
  "[H264Settings](#cfn-medialive-channel-videocodecsettings-h264settings)" : H264Settings,
  "[H265Settings](#cfn-medialive-channel-videocodecsettings-h265settings)" : H265Settings,
  "[Mpeg2Settings](#cfn-medialive-channel-videocodecsettings-mpeg2settings)" : Mpeg2Settings
}
```

### YAML<a name="aws-properties-medialive-channel-videocodecsettings-syntax.yaml"></a>

```
  [FrameCaptureSettings](#cfn-medialive-channel-videocodecsettings-framecapturesettings): 
    FrameCaptureSettings
  [H264Settings](#cfn-medialive-channel-videocodecsettings-h264settings): 
    H264Settings
  [H265Settings](#cfn-medialive-channel-videocodecsettings-h265settings): 
    H265Settings
  [Mpeg2Settings](#cfn-medialive-channel-videocodecsettings-mpeg2settings): 
    Mpeg2Settings
```

## Properties<a name="aws-properties-medialive-channel-videocodecsettings-properties"></a>

`FrameCaptureSettings`  <a name="cfn-medialive-channel-videocodecsettings-framecapturesettings"></a>
The settings for the video codec in a frame capture output\.  
*Required*: No  
*Type*: [FrameCaptureSettings](aws-properties-medialive-channel-framecapturesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`H264Settings`  <a name="cfn-medialive-channel-videocodecsettings-h264settings"></a>
The settings for the H\.264 codec in the output\.  
*Required*: No  
*Type*: [H264Settings](aws-properties-medialive-channel-h264settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`H265Settings`  <a name="cfn-medialive-channel-videocodecsettings-h265settings"></a>
Settings for video encoded with the H265 codec\.  
*Required*: No  
*Type*: [H265Settings](aws-properties-medialive-channel-h265settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mpeg2Settings`  <a name="cfn-medialive-channel-videocodecsettings-mpeg2settings"></a>
Settings for video encoded with the MPEG\-2 codec\.  
*Required*: No  
*Type*: [Mpeg2Settings](aws-properties-medialive-channel-mpeg2settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)