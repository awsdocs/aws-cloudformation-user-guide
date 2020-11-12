# AWS::MediaLive::Channel VideoDescription<a name="aws-properties-medialive-channel-videodescription"></a>

The configuration information for an individual output video encode\. This element belongs to EncoderSettings\. To associate this VideoDescription with its Output, you enter the same value in the name field of the VideoDescription and the VideoDescriptionNames field of the Output\.

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
Include this element once for each VideoDescription in the channel\.  
*Required*: No  
*Type*: [VideoCodecSettings](aws-properties-medialive-channel-videocodecsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Height`  <a name="cfn-medialive-channel-videodescription-height"></a>
Output video height, in pixels\. Must be an even number\. For most codecs, you can leave this field and width blank in order to use the height and width \(resolution\) from the source\. Note, however, that leaving blank is not recommended\. For the Frame Capture codec, height and width are required\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-videodescription-name"></a>
A name for this VideoDescription\. Must be unique in the channel\. MediaLive uses this name to associate the VideoDescription with the output group it belongs to: you enter the same value in this field and in the VideoDescriptionNames field of the output in the appropriate output group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RespondToAfd`  <a name="cfn-medialive-channel-videodescription-respondtoafd"></a>
Indicates how to respond to the AFD values in the input stream\. RESPOND causes input video to be clipped, depending on the AFD value, input display aspect ratio, and output display aspect ratio, and \(except for FRAME\_CAPTURE codec\) includes the values in the output\. PASSTHROUGH \(does not apply to FRAME\_CAPTURE codec\) ignores the AFD values and includes the values in the output, so input video is not clipped\. NONE ignores the AFD values and does not include the values through to the output, so input video is not clipped\.  
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