# AWS::MediaLive::Channel VideoCodecSettings<a name="aws-properties-medialive-channel-videocodecsettings"></a>

This element configures one output video encode\. In this element, include only one of the child elements\. This element belongs to VideoDescription\.

## Syntax<a name="aws-properties-medialive-channel-videocodecsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videocodecsettings-syntax.json"></a>

```
{
  "[FrameCaptureSettings](#cfn-medialive-channel-videocodecsettings-framecapturesettings)" : FrameCaptureSettings,
  "[H264Settings](#cfn-medialive-channel-videocodecsettings-h264settings)" : H264Settings,
  "[H265Settings](#cfn-medialive-channel-videocodecsettings-h265settings)" : H265Settings
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
```

## Properties<a name="aws-properties-medialive-channel-videocodecsettings-properties"></a>

`FrameCaptureSettings`  <a name="cfn-medialive-channel-videocodecsettings-framecapturesettings"></a>
Include this element if you want to set up the video encode as a framecapture \(set of JPEG files\)\.  
*Required*: No  
*Type*: [FrameCaptureSettings](aws-properties-medialive-channel-framecapturesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`H264Settings`  <a name="cfn-medialive-channel-videocodecsettings-h264settings"></a>
Include this element if you want to set up the video encode to use the H264 codec\.  
*Required*: No  
*Type*: [H264Settings](aws-properties-medialive-channel-h264settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`H265Settings`  <a name="cfn-medialive-channel-videocodecsettings-h265settings"></a>
Include this element if you want to set up the video encode to use the H265 codec\.  
*Required*: No  
*Type*: [H265Settings](aws-properties-medialive-channel-h265settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)