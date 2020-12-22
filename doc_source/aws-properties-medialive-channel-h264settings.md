# AWS::MediaLive::Channel H264Settings<a name="aws-properties-medialive-channel-h264settings"></a>

The settings for the H\.264 codec in the output\.

The parent of this entity is VideoCodecSettings\.

## Syntax<a name="aws-properties-medialive-channel-h264settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-h264settings-syntax.json"></a>

```
{
  "[AdaptiveQuantization](#cfn-medialive-channel-h264settings-adaptivequantization)" : String,
  "[AfdSignaling](#cfn-medialive-channel-h264settings-afdsignaling)" : String,
  "[Bitrate](#cfn-medialive-channel-h264settings-bitrate)" : Integer,
  "[BufFillPct](#cfn-medialive-channel-h264settings-buffillpct)" : Integer,
  "[BufSize](#cfn-medialive-channel-h264settings-bufsize)" : Integer,
  "[ColorMetadata](#cfn-medialive-channel-h264settings-colormetadata)" : String,
  "[ColorSpaceSettings](#cfn-medialive-channel-h264settings-colorspacesettings)" : H264ColorSpaceSettings,
  "[EntropyEncoding](#cfn-medialive-channel-h264settings-entropyencoding)" : String,
  "[FilterSettings](#cfn-medialive-channel-h264settings-filtersettings)" : H264FilterSettings,
  "[FixedAfd](#cfn-medialive-channel-h264settings-fixedafd)" : String,
  "[FlickerAq](#cfn-medialive-channel-h264settings-flickeraq)" : String,
  "[ForceFieldPictures](#cfn-medialive-channel-h264settings-forcefieldpictures)" : String,
  "[FramerateControl](#cfn-medialive-channel-h264settings-frameratecontrol)" : String,
  "[FramerateDenominator](#cfn-medialive-channel-h264settings-frameratedenominator)" : Integer,
  "[FramerateNumerator](#cfn-medialive-channel-h264settings-frameratenumerator)" : Integer,
  "[GopBReference](#cfn-medialive-channel-h264settings-gopbreference)" : String,
  "[GopClosedCadence](#cfn-medialive-channel-h264settings-gopclosedcadence)" : Integer,
  "[GopNumBFrames](#cfn-medialive-channel-h264settings-gopnumbframes)" : Integer,
  "[GopSize](#cfn-medialive-channel-h264settings-gopsize)" : Double,
  "[GopSizeUnits](#cfn-medialive-channel-h264settings-gopsizeunits)" : String,
  "[Level](#cfn-medialive-channel-h264settings-level)" : String,
  "[LookAheadRateControl](#cfn-medialive-channel-h264settings-lookaheadratecontrol)" : String,
  "[MaxBitrate](#cfn-medialive-channel-h264settings-maxbitrate)" : Integer,
  "[MinIInterval](#cfn-medialive-channel-h264settings-miniinterval)" : Integer,
  "[NumRefFrames](#cfn-medialive-channel-h264settings-numrefframes)" : Integer,
  "[ParControl](#cfn-medialive-channel-h264settings-parcontrol)" : String,
  "[ParDenominator](#cfn-medialive-channel-h264settings-pardenominator)" : Integer,
  "[ParNumerator](#cfn-medialive-channel-h264settings-parnumerator)" : Integer,
  "[Profile](#cfn-medialive-channel-h264settings-profile)" : String,
  "[QualityLevel](#cfn-medialive-channel-h264settings-qualitylevel)" : String,
  "[QvbrQualityLevel](#cfn-medialive-channel-h264settings-qvbrqualitylevel)" : Integer,
  "[RateControlMode](#cfn-medialive-channel-h264settings-ratecontrolmode)" : String,
  "[ScanType](#cfn-medialive-channel-h264settings-scantype)" : String,
  "[SceneChangeDetect](#cfn-medialive-channel-h264settings-scenechangedetect)" : String,
  "[Slices](#cfn-medialive-channel-h264settings-slices)" : Integer,
  "[Softness](#cfn-medialive-channel-h264settings-softness)" : Integer,
  "[SpatialAq](#cfn-medialive-channel-h264settings-spatialaq)" : String,
  "[SubgopLength](#cfn-medialive-channel-h264settings-subgoplength)" : String,
  "[Syntax](#cfn-medialive-channel-h264settings-syntax)" : String,
  "[TemporalAq](#cfn-medialive-channel-h264settings-temporalaq)" : String,
  "[TimecodeInsertion](#cfn-medialive-channel-h264settings-timecodeinsertion)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-h264settings-syntax.yaml"></a>

```
  [AdaptiveQuantization](#cfn-medialive-channel-h264settings-adaptivequantization): String
  [AfdSignaling](#cfn-medialive-channel-h264settings-afdsignaling): String
  [Bitrate](#cfn-medialive-channel-h264settings-bitrate): Integer
  [BufFillPct](#cfn-medialive-channel-h264settings-buffillpct): Integer
  [BufSize](#cfn-medialive-channel-h264settings-bufsize): Integer
  [ColorMetadata](#cfn-medialive-channel-h264settings-colormetadata): String
  [ColorSpaceSettings](#cfn-medialive-channel-h264settings-colorspacesettings): 
    H264ColorSpaceSettings
  [EntropyEncoding](#cfn-medialive-channel-h264settings-entropyencoding): String
  [FilterSettings](#cfn-medialive-channel-h264settings-filtersettings): 
    H264FilterSettings
  [FixedAfd](#cfn-medialive-channel-h264settings-fixedafd): String
  [FlickerAq](#cfn-medialive-channel-h264settings-flickeraq): String
  [ForceFieldPictures](#cfn-medialive-channel-h264settings-forcefieldpictures): String
  [FramerateControl](#cfn-medialive-channel-h264settings-frameratecontrol): String
  [FramerateDenominator](#cfn-medialive-channel-h264settings-frameratedenominator): Integer
  [FramerateNumerator](#cfn-medialive-channel-h264settings-frameratenumerator): Integer
  [GopBReference](#cfn-medialive-channel-h264settings-gopbreference): String
  [GopClosedCadence](#cfn-medialive-channel-h264settings-gopclosedcadence): Integer
  [GopNumBFrames](#cfn-medialive-channel-h264settings-gopnumbframes): Integer
  [GopSize](#cfn-medialive-channel-h264settings-gopsize): Double
  [GopSizeUnits](#cfn-medialive-channel-h264settings-gopsizeunits): String
  [Level](#cfn-medialive-channel-h264settings-level): String
  [LookAheadRateControl](#cfn-medialive-channel-h264settings-lookaheadratecontrol): String
  [MaxBitrate](#cfn-medialive-channel-h264settings-maxbitrate): Integer
  [MinIInterval](#cfn-medialive-channel-h264settings-miniinterval): Integer
  [NumRefFrames](#cfn-medialive-channel-h264settings-numrefframes): Integer
  [ParControl](#cfn-medialive-channel-h264settings-parcontrol): String
  [ParDenominator](#cfn-medialive-channel-h264settings-pardenominator): Integer
  [ParNumerator](#cfn-medialive-channel-h264settings-parnumerator): Integer
  [Profile](#cfn-medialive-channel-h264settings-profile): String
  [QualityLevel](#cfn-medialive-channel-h264settings-qualitylevel): String
  [QvbrQualityLevel](#cfn-medialive-channel-h264settings-qvbrqualitylevel): Integer
  [RateControlMode](#cfn-medialive-channel-h264settings-ratecontrolmode): String
  [ScanType](#cfn-medialive-channel-h264settings-scantype): String
  [SceneChangeDetect](#cfn-medialive-channel-h264settings-scenechangedetect): String
  [Slices](#cfn-medialive-channel-h264settings-slices): Integer
  [Softness](#cfn-medialive-channel-h264settings-softness): Integer
  [SpatialAq](#cfn-medialive-channel-h264settings-spatialaq): String
  [SubgopLength](#cfn-medialive-channel-h264settings-subgoplength): String
  [Syntax](#cfn-medialive-channel-h264settings-syntax): String
  [TemporalAq](#cfn-medialive-channel-h264settings-temporalaq): String
  [TimecodeInsertion](#cfn-medialive-channel-h264settings-timecodeinsertion): String
```

## Properties<a name="aws-properties-medialive-channel-h264settings-properties"></a>

`AdaptiveQuantization`  <a name="cfn-medialive-channel-h264settings-adaptivequantization"></a>
The adaptive quantization\. This allows intra\-frame quantizers to vary to improve visual quality\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AfdSignaling`  <a name="cfn-medialive-channel-h264settings-afdsignaling"></a>
Indicates that AFD values will be written into the output stream\. If afdSignaling is auto, the system tries to preserve the input AFD value \(in cases where multiple AFD values are valid\)\. If set to fixed, the AFD value is the value configured in the fixedAfd parameter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bitrate`  <a name="cfn-medialive-channel-h264settings-bitrate"></a>
The average bitrate in bits/second\. This is required when the rate control mode is VBR or CBR\. It isn't used for QVBR\. In a Microsoft Smooth output group, each output must have a unique value when its bitrate is rounded down to the nearest multiple of 1000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BufFillPct`  <a name="cfn-medialive-channel-h264settings-buffillpct"></a>
The percentage of the buffer that should initially be filled \(HRD buffer model\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BufSize`  <a name="cfn-medialive-channel-h264settings-bufsize"></a>
The size of the buffer \(HRD buffer model\) in bits/second\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorMetadata`  <a name="cfn-medialive-channel-h264settings-colormetadata"></a>
Includes color space metadata in the output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorSpaceSettings`  <a name="cfn-medialive-channel-h264settings-colorspacesettings"></a>
Color Space settings  
*Required*: No  
*Type*: [H264ColorSpaceSettings](aws-properties-medialive-channel-h264colorspacesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntropyEncoding`  <a name="cfn-medialive-channel-h264settings-entropyencoding"></a>
The entropy encoding mode\. Use cabac \(must be in Main or High profile\) or cavlc\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterSettings`  <a name="cfn-medialive-channel-h264settings-filtersettings"></a>
Optional filters that you can apply to an encode\.  
*Required*: No  
*Type*: [H264FilterSettings](aws-properties-medialive-channel-h264filtersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FixedAfd`  <a name="cfn-medialive-channel-h264settings-fixedafd"></a>
A four\-bit AFD value to write on all frames of video in the output stream\. Valid only when afdSignaling is set to Fixed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlickerAq`  <a name="cfn-medialive-channel-h264settings-flickeraq"></a>
If set to enabled, adjusts the quantization within each frame to reduce flicker or pop on I\-frames\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForceFieldPictures`  <a name="cfn-medialive-channel-h264settings-forcefieldpictures"></a>
This setting applies only when scan type is "interlaced\." It controls whether coding is performed on a field basis or on a frame basis\. \(When the video is progressive, the coding is always performed on a frame basis\.\) enabled: Force MediaLive to code on a field basis, so that odd and even sets of fields are coded separately\. disabled: Code the two sets of fields separately \(on a field basis\) or together \(on a frame basis using PAFF\), depending on what is most appropriate for the content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FramerateControl`  <a name="cfn-medialive-channel-h264settings-frameratecontrol"></a>
Indicates how the output video frame rate is specified\. If you select "specified," the output video frame rate is determined by framerateNumerator and framerateDenominator\. If you select "initializeFromSource," the output video frame rate is set equal to the input video frame rate of the first input\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FramerateDenominator`  <a name="cfn-medialive-channel-h264settings-frameratedenominator"></a>
The frame rate denominator\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FramerateNumerator`  <a name="cfn-medialive-channel-h264settings-frameratenumerator"></a>
The frame rate numerator\. The frame rate is a fraction, for example, 24000/1001 = 23\.976 fps\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopBReference`  <a name="cfn-medialive-channel-h264settings-gopbreference"></a>
If enabled, uses reference B frames for GOP structures that have B frames > 1\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopClosedCadence`  <a name="cfn-medialive-channel-h264settings-gopclosedcadence"></a>
The frequency of closed GOPs\. In streaming applications, we recommend that you set this to 1 so that a decoder joining mid\-stream will receive an IDR frame as quickly as possible\. Setting this value to 0 will break output segmenting\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopNumBFrames`  <a name="cfn-medialive-channel-h264settings-gopnumbframes"></a>
The number of B\-frames between reference frames\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopSize`  <a name="cfn-medialive-channel-h264settings-gopsize"></a>
The GOP size \(keyframe interval\) in units of either frames or seconds per gopSizeUnits\. The value must be greater than zero\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GopSizeUnits`  <a name="cfn-medialive-channel-h264settings-gopsizeunits"></a>
Indicates if the gopSize is specified in frames or seconds\. If seconds, the system converts the gopSize into a frame count at runtime\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Level`  <a name="cfn-medialive-channel-h264settings-level"></a>
The H\.264 level\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LookAheadRateControl`  <a name="cfn-medialive-channel-h264settings-lookaheadratecontrol"></a>
The amount of lookahead\. A value of low can decrease latency and memory usage, while high can produce better quality for certain content\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxBitrate`  <a name="cfn-medialive-channel-h264settings-maxbitrate"></a>
For QVBR: See the tooltip for Quality level\. For VBR: Set the maximum bitrate in order to accommodate expected spikes in the complexity of the video\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinIInterval`  <a name="cfn-medialive-channel-h264settings-miniinterval"></a>
Meaningful only if sceneChangeDetect is set to enabled\. This setting enforces separation between repeated \(cadence\) I\-frames and I\-frames inserted by Scene Change Detection\. If a scene change I\-frame is within I\-interval frames of a cadence I\-frame, the GOP is shrunk or stretched to the scene change I\-frame\. GOP stretch requires enabling lookahead as well as setting the I\-interval\. The normal cadence resumes for the next GOP\. Note that the maximum GOP stretch = GOP size \+ Min\-I\-interval \- 1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRefFrames`  <a name="cfn-medialive-channel-h264settings-numrefframes"></a>
The number of reference frames to use\. The encoder might use more than requested if you use B\-frames or interlaced encoding\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParControl`  <a name="cfn-medialive-channel-h264settings-parcontrol"></a>
Indicates how the output pixel aspect ratio is specified\. If "specified" is selected, the output video pixel aspect ratio is determined by parNumerator and parDenominator\. If "initializeFromSource" is selected, the output pixels aspect ratio will be set equal to the input video pixel aspect ratio of the first input\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParDenominator`  <a name="cfn-medialive-channel-h264settings-pardenominator"></a>
The Pixel Aspect Ratio denominator\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParNumerator`  <a name="cfn-medialive-channel-h264settings-parnumerator"></a>
The Pixel Aspect Ratio numerator\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Profile`  <a name="cfn-medialive-channel-h264settings-profile"></a>
An H\.264 profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QualityLevel`  <a name="cfn-medialive-channel-h264settings-qualitylevel"></a>
Leave as STANDARD\_QUALITY or choose a different value \(which might result in additional costs to run the channel\)\. \- ENHANCED\_QUALITY: Produces a slightly better video quality without an increase in the bitrate\. Has an effect only when the Rate control mode is QVBR or CBR\. If this channel is in a MediaLive multiplex, the value must be ENHANCED\_QUALITY\. \- STANDARD\_QUALITY: Valid for any Rate control mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QvbrQualityLevel`  <a name="cfn-medialive-channel-h264settings-qvbrqualitylevel"></a>
Controls the target quality for the video encode\. This applies only when the rate control mode is QVBR\. Set values for the QVBR quality level field and Max bitrate field that suit your most important viewing devices\. Recommended values are: \- Primary screen: Quality level: 8 to 10\. Max bitrate: 4M \- PC or tablet: Quality level: 7\. Max bitrate: 1\.5M to 3M \- Smartphone: Quality level: 6\. Max bitrate: 1M to 1\.5M\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateControlMode`  <a name="cfn-medialive-channel-h264settings-ratecontrolmode"></a>
The rate control mode\. QVBR: The quality will match the specified quality level except when it is constrained by the maximum bitrate\. We recommend this if you or your viewers pay for bandwidth\. VBR: The quality and bitrate vary, depending on the video complexity\. We recommend this instead of QVBR if you want to maintain a specific average bitrate over the duration of the channel\. CBR: The quality varies, depending on the video complexity\. We recommend this only if you distribute your assets to devices that can't handle variable bitrates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScanType`  <a name="cfn-medialive-channel-h264settings-scantype"></a>
Sets the scan type of the output to progressive or top\-field\-first interlaced\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SceneChangeDetect`  <a name="cfn-medialive-channel-h264settings-scenechangedetect"></a>
The scene change detection\. On: inserts I\-frames when the scene change is detected\. Off: does not force an I\-frame when the scene change is detected\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slices`  <a name="cfn-medialive-channel-h264settings-slices"></a>
The number of slices per picture\. The number must be less than or equal to the number of macroblock rows for progressive pictures, and less than or equal to half the number of macroblock rows for interlaced pictures\. This field is optional\. If you don't specify a value, MediaLive chooses the number of slices based on the encode resolution\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Softness`  <a name="cfn-medialive-channel-h264settings-softness"></a>
Softness\. Selects a quantizer matrix\. Larger values reduce high\-frequency content in the encoded image\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpatialAq`  <a name="cfn-medialive-channel-h264settings-spatialaq"></a>
If set to enabled, adjusts quantization within each frame based on the spatial variation of content complexity\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubgopLength`  <a name="cfn-medialive-channel-h264settings-subgoplength"></a>
If set to fixed, uses gopNumBFrames B\-frames per sub\-GOP\. If set to dynamic, optimizes the number of B\-frames used for each sub\-GOP to improve visual quality\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Syntax`  <a name="cfn-medialive-channel-h264settings-syntax"></a>
Produces a bitstream that is compliant with SMPTE RP\-2027\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemporalAq`  <a name="cfn-medialive-channel-h264settings-temporalaq"></a>
If set to enabled, adjusts quantization within each frame based on the temporal variation of content complexity\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimecodeInsertion`  <a name="cfn-medialive-channel-h264settings-timecodeinsertion"></a>
Determines how timecodes should be inserted into the video elementary stream\. disabled: don't include timecodes\. picTimingSei: pass through picture timing SEI messages from the source specified in Timecode Config\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)