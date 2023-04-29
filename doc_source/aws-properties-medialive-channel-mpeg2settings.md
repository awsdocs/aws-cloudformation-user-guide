# AWS::MediaLive::Channel Mpeg2Settings<a name="aws-properties-medialive-channel-mpeg2settings"></a>

The settings for the MPEG\-2 codec in the output\.

The parent of this entity is VideoCodecSetting\.

## Syntax<a name="aws-properties-medialive-channel-mpeg2settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mpeg2settings-syntax.json"></a>

```
{
  "[AdaptiveQuantization](#cfn-medialive-channel-mpeg2settings-adaptivequantization)" : String,
  "[AfdSignaling](#cfn-medialive-channel-mpeg2settings-afdsignaling)" : String,
  "[ColorMetadata](#cfn-medialive-channel-mpeg2settings-colormetadata)" : String,
  "[ColorSpace](#cfn-medialive-channel-mpeg2settings-colorspace)" : String,
  "[DisplayAspectRatio](#cfn-medialive-channel-mpeg2settings-displayaspectratio)" : String,
  "[FilterSettings](#cfn-medialive-channel-mpeg2settings-filtersettings)" : Mpeg2FilterSettings,
  "[FixedAfd](#cfn-medialive-channel-mpeg2settings-fixedafd)" : String,
  "[FramerateDenominator](#cfn-medialive-channel-mpeg2settings-frameratedenominator)" : Integer,
  "[FramerateNumerator](#cfn-medialive-channel-mpeg2settings-frameratenumerator)" : Integer,
  "[GopClosedCadence](#cfn-medialive-channel-mpeg2settings-gopclosedcadence)" : Integer,
  "[GopNumBFrames](#cfn-medialive-channel-mpeg2settings-gopnumbframes)" : Integer,
  "[GopSize](#cfn-medialive-channel-mpeg2settings-gopsize)" : Double,
  "[GopSizeUnits](#cfn-medialive-channel-mpeg2settings-gopsizeunits)" : String,
  "[ScanType](#cfn-medialive-channel-mpeg2settings-scantype)" : String,
  "[SubgopLength](#cfn-medialive-channel-mpeg2settings-subgoplength)" : String,
  "[TimecodeBurninSettings](#cfn-medialive-channel-mpeg2settings-timecodeburninsettings)" : TimecodeBurninSettings,
  "[TimecodeInsertion](#cfn-medialive-channel-mpeg2settings-timecodeinsertion)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-mpeg2settings-syntax.yaml"></a>

```
  [AdaptiveQuantization](#cfn-medialive-channel-mpeg2settings-adaptivequantization): String
  [AfdSignaling](#cfn-medialive-channel-mpeg2settings-afdsignaling): String
  [ColorMetadata](#cfn-medialive-channel-mpeg2settings-colormetadata): String
  [ColorSpace](#cfn-medialive-channel-mpeg2settings-colorspace): String
  [DisplayAspectRatio](#cfn-medialive-channel-mpeg2settings-displayaspectratio): String
  [FilterSettings](#cfn-medialive-channel-mpeg2settings-filtersettings): 
    Mpeg2FilterSettings
  [FixedAfd](#cfn-medialive-channel-mpeg2settings-fixedafd): String
  [FramerateDenominator](#cfn-medialive-channel-mpeg2settings-frameratedenominator): Integer
  [FramerateNumerator](#cfn-medialive-channel-mpeg2settings-frameratenumerator): Integer
  [GopClosedCadence](#cfn-medialive-channel-mpeg2settings-gopclosedcadence): Integer
  [GopNumBFrames](#cfn-medialive-channel-mpeg2settings-gopnumbframes): Integer
  [GopSize](#cfn-medialive-channel-mpeg2settings-gopsize): Double
  [GopSizeUnits](#cfn-medialive-channel-mpeg2settings-gopsizeunits): String
  [ScanType](#cfn-medialive-channel-mpeg2settings-scantype): String
  [SubgopLength](#cfn-medialive-channel-mpeg2settings-subgoplength): String
  [TimecodeBurninSettings](#cfn-medialive-channel-mpeg2settings-timecodeburninsettings): 
    TimecodeBurninSettings
  [TimecodeInsertion](#cfn-medialive-channel-mpeg2settings-timecodeinsertion): String
```

## Properties<a name="aws-properties-medialive-channel-mpeg2settings-properties"></a>

`AdaptiveQuantization`  <a name="cfn-medialive-channel-mpeg2settings-adaptivequantization"></a>
Choose Off to disable adaptive quantization\. Or choose another value to enable the quantizer and set its strength\. The strengths are: Auto, Off, Low, Medium, High\. When you enable this field, MediaLive allows intra\-frame quantizers to vary, which might improve visual quality\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AfdSignaling`  <a name="cfn-medialive-channel-mpeg2settings-afdsignaling"></a>
Indicates the AFD values that MediaLive will write into the video encode\. If you do not know what AFD signaling is, or if your downstream system has not given you guidance, choose AUTO\. AUTO: MediaLive will try to preserve the input AFD value \(in cases where multiple AFD values are valid\)\. FIXED: MediaLive will use the value you specify in fixedAFD\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorMetadata`  <a name="cfn-medialive-channel-mpeg2settings-colormetadata"></a>
Specifies whether to include the color space metadata\. The metadata describes the color space that applies to the video \(the colorSpace field\)\. We recommend that you insert the metadata\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorSpace`  <a name="cfn-medialive-channel-mpeg2settings-colorspace"></a>
Choose the type of color space conversion to apply to the output\. For detailed information on setting up both the input and the output to obtain the desired color space in the output, see the section on \\"MediaLive Features \- Video \- color space\\" in the MediaLive User Guide\. PASSTHROUGH: Keep the color space of the input content \- do not convert it\. AUTO:Convert all content that is SD to rec 601, and convert all content that is HD to rec 709\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayAspectRatio`  <a name="cfn-medialive-channel-mpeg2settings-displayaspectratio"></a>
Sets the pixel aspect ratio for the encode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterSettings`  <a name="cfn-medialive-channel-mpeg2settings-filtersettings"></a>
Optionally specify a noise reduction filter, which can improve quality of compressed content\. If you do not choose a filter, no filter will be applied\. TEMPORAL: This filter is useful for both source content that is noisy \(when it has excessive digital artifacts\) and source content that is clean\. When the content is noisy, the filter cleans up the source content before the encoding phase, with these two effects: First, it improves the output video quality because the content has been cleaned up\. Secondly, it decreases the bandwidth because MediaLive does not waste bits on encoding noise\. When the content is reasonably clean, the filter tends to decrease the bitrate\.  
*Required*: No  
*Type*: [Mpeg2FilterSettings](aws-properties-medialive-channel-mpeg2filtersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FixedAfd`  <a name="cfn-medialive-channel-mpeg2settings-fixedafd"></a>
Complete this field only when afdSignaling is set to FIXED\. Enter the AFD value \(4 bits\) to write on all frames of the video encode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FramerateDenominator`  <a name="cfn-medialive-channel-mpeg2settings-frameratedenominator"></a>
description": "The framerate denominator\. For example, 1001\. The framerate is the numerator divided by the denominator\. For example, 24000 / 1001 = 23\.976 FPS\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FramerateNumerator`  <a name="cfn-medialive-channel-mpeg2settings-frameratenumerator"></a>
The framerate numerator\. For example, 24000\. The framerate is the numerator divided by the denominator\. For example, 24000 / 1001 = 23\.976 FPS\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopClosedCadence`  <a name="cfn-medialive-channel-mpeg2settings-gopclosedcadence"></a>
MPEG2: default is open GOP\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopNumBFrames`  <a name="cfn-medialive-channel-mpeg2settings-gopnumbframes"></a>
Relates to the GOP structure\. The number of B\-frames between reference frames\. If you do not know what a B\-frame is, use the default\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopSize`  <a name="cfn-medialive-channel-mpeg2settings-gopsize"></a>
Relates to the GOP structure\. The GOP size \(keyframe interval\) in the units specified in gopSizeUnits\. If you do not know what GOP is, use the default\. If gopSizeUnits is frames, then the gopSize must be an integer and must be greater than or equal to 1\. If gopSizeUnits is seconds, the gopSize must be greater than 0, but does not need to be an integer\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopSizeUnits`  <a name="cfn-medialive-channel-mpeg2settings-gopsizeunits"></a>
Relates to the GOP structure\. Specifies whether the gopSize is specified in frames or seconds\. If you do not plan to change the default gopSize, leave the default\. If you specify SECONDS, MediaLive will internally convert the gop size to a frame count\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScanType`  <a name="cfn-medialive-channel-mpeg2settings-scantype"></a>
Set the scan type of the output to PROGRESSIVE or INTERLACED \(top field first\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubgopLength`  <a name="cfn-medialive-channel-mpeg2settings-subgoplength"></a>
Relates to the GOP structure\. If you do not know what GOP is, use the default\. FIXED: Set the number of B\-frames in each sub\-GOP to the value in gopNumBFrames\. DYNAMIC: Let MediaLive optimize the number of B\-frames in each sub\-GOP, to improve visual quality\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimecodeBurninSettings`  <a name="cfn-medialive-channel-mpeg2settings-timecodeburninsettings"></a>
Property description not available\.  
*Required*: No  
*Type*: [TimecodeBurninSettings](aws-properties-medialive-channel-timecodeburninsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimecodeInsertion`  <a name="cfn-medialive-channel-mpeg2settings-timecodeinsertion"></a>
Determines how MediaLive inserts timecodes in the output video\. For detailed information about setting up the input and the output for a timecode, see the section on \\"MediaLive Features \- Timecode configuration\\" in the MediaLive User Guide\. DISABLED: do not include timecodes\. GOP\_TIMECODE: Include timecode metadata in the GOP header\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)