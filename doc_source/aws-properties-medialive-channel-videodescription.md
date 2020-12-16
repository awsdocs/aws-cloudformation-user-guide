# AWS::MediaLive::Channel VideoDescription<a name="aws-properties-medialive-channel-videodescription"></a>

Video settings for this stream\.

## Syntax<a name="aws-properties-medialive-channel-videodescription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videodescription-syntax.json"></a>

```
{
  "[CodecSettings](#cfn-medialive-channel-videodescription-codecsettings)" : VideoCodecSettings,
  "[Height](#cfn-medialive-channel-videodescription-height)" : Integer,
  "[Name](#cfn-medialive-channel-videodescription-name)" : String,
  "[RespondToAfd](#cfn-medialive-channel-videodescription-respondtoafd)" : String,
  "[ScalingBehavior](#cfn-medialive-channel-videodescription-scalingbehavior)" : String,
  "[Sharpness](#cfn-medialive-channel-videodescription-sharpness)" : Integer,
  "[Width](#cfn-medialive-channel-videodescription-width)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-videodescription-syntax.yaml"></a>

```
  [CodecSettings](#cfn-medialive-channel-videodescription-codecsettings): 
    VideoCodecSettings
  [Height](#cfn-medialive-channel-videodescription-height): Integer
  [Name](#cfn-medialive-channel-videodescription-name): String
  [RespondToAfd](#cfn-medialive-channel-videodescription-respondtoafd): String
  [ScalingBehavior](#cfn-medialive-channel-videodescription-scalingbehavior): String
  [Sharpness](#cfn-medialive-channel-videodescription-sharpness): Integer
  [Width](#cfn-medialive-channel-videodescription-width): Integer
```

## Properties<a name="aws-properties-medialive-channel-videodescription-properties"></a>

`CodecSettings`  <a name="cfn-medialive-channel-videodescription-codecsettings"></a>
Video codec settings\.  
*Required*: No  
*Type*: [VideoCodecSettings](aws-properties-medialive-channel-videocodecsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Height`  <a name="cfn-medialive-channel-videodescription-height"></a>
Output video height, in pixels\. Must be an even number\. For most codecs, you can leave this field and width blank in order to use the height and width \(resolution\) from the source\. Note, however, that leaving blank is not recommended\. For the Frame Capture codec, height and width are required\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-videodescription-name"></a>
The name of this VideoDescription\. Outputs will use this name to uniquely identify this Description\. Description names should be unique within this Live Event\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RespondToAfd`  <a name="cfn-medialive-channel-videodescription-respondtoafd"></a>
Indicates how MediaLive will respond to the AFD values that might be in the input video\. If you do not know what AFD signaling is, or if your downstream system has not given you guidance, choose PASSTHROUGH\. RESPOND: MediaLive clips the input video using a formula that uses the AFD values \(configured in afdSignaling \), the input display aspect ratio, and the output display aspect ratio\. MediaLive also includes the AFD values in the output, unless the codec for this encode is FRAME\_CAPTURE\. PASSTHROUGH: MediaLive ignores the AFD values and does not clip the video\. But MediaLive does include the values in the output\. NONE: MediaLive does not clip the input video and does not include the AFD values in the output  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingBehavior`  <a name="cfn-medialive-channel-videodescription-scalingbehavior"></a>
STRETCH\_TO\_OUTPUT configures the output position to stretch the video to the specified output resolution \(height and width\)\. This option will override any position value\. DEFAULT may insert black boxes \(pillar boxes or letter boxes\) around the video to provide the specified output resolution\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sharpness`  <a name="cfn-medialive-channel-videodescription-sharpness"></a>
Changes the strength of the anti\-alias filter used for scaling\. 0 is the softest setting, 100 is the sharpest\. A setting of 50 is recommended for most content\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-medialive-channel-videodescription-width"></a>
Output video width, in pixels\. Must be an even number\. For most codecs, you can leave this field and height blank in order to use the height and width \(resolution\) from the source\. Note, however, that leaving blank is not recommended\. For the Frame Capture codec, height and width are required\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)