# AWS::MediaLive::Channel InputSettings<a name="aws-properties-medialive-channel-inputsettings"></a>

Live Event input parameters\. There can be multiple inputs in a single Live Event\.

## Syntax<a name="aws-properties-medialive-channel-inputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputsettings-syntax.json"></a>

```
{
  "[AudioSelectors](#cfn-medialive-channel-inputsettings-audioselectors)" : [ AudioSelector, ... ],
  "[CaptionSelectors](#cfn-medialive-channel-inputsettings-captionselectors)" : [ CaptionSelector, ... ],
  "[DeblockFilter](#cfn-medialive-channel-inputsettings-deblockfilter)" : String,
  "[DenoiseFilter](#cfn-medialive-channel-inputsettings-denoisefilter)" : String,
  "[FilterStrength](#cfn-medialive-channel-inputsettings-filterstrength)" : Integer,
  "[InputFilter](#cfn-medialive-channel-inputsettings-inputfilter)" : String,
  "[NetworkInputSettings](#cfn-medialive-channel-inputsettings-networkinputsettings)" : NetworkInputSettings,
  "[Smpte2038DataPreference](#cfn-medialive-channel-inputsettings-smpte2038datapreference)" : String,
  "[SourceEndBehavior](#cfn-medialive-channel-inputsettings-sourceendbehavior)" : String,
  "[VideoSelector](#cfn-medialive-channel-inputsettings-videoselector)" : VideoSelector
}
```

### YAML<a name="aws-properties-medialive-channel-inputsettings-syntax.yaml"></a>

```
  [AudioSelectors](#cfn-medialive-channel-inputsettings-audioselectors): 
    - AudioSelector
  [CaptionSelectors](#cfn-medialive-channel-inputsettings-captionselectors): 
    - CaptionSelector
  [DeblockFilter](#cfn-medialive-channel-inputsettings-deblockfilter): String
  [DenoiseFilter](#cfn-medialive-channel-inputsettings-denoisefilter): String
  [FilterStrength](#cfn-medialive-channel-inputsettings-filterstrength): Integer
  [InputFilter](#cfn-medialive-channel-inputsettings-inputfilter): String
  [NetworkInputSettings](#cfn-medialive-channel-inputsettings-networkinputsettings): 
    NetworkInputSettings
  [Smpte2038DataPreference](#cfn-medialive-channel-inputsettings-smpte2038datapreference): String
  [SourceEndBehavior](#cfn-medialive-channel-inputsettings-sourceendbehavior): String
  [VideoSelector](#cfn-medialive-channel-inputsettings-videoselector): 
    VideoSelector
```

## Properties<a name="aws-properties-medialive-channel-inputsettings-properties"></a>

`AudioSelectors`  <a name="cfn-medialive-channel-inputsettings-audioselectors"></a>
Used to select the audio stream to decode for inputs that have multiple available\.  
*Required*: No  
*Type*: List of [AudioSelector](aws-properties-medialive-channel-audioselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionSelectors`  <a name="cfn-medialive-channel-inputsettings-captionselectors"></a>
Used to select the caption input to use for inputs that have multiple available\.  
*Required*: No  
*Type*: List of [CaptionSelector](aws-properties-medialive-channel-captionselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeblockFilter`  <a name="cfn-medialive-channel-inputsettings-deblockfilter"></a>
Enable or disable the deblock filter when filtering\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DenoiseFilter`  <a name="cfn-medialive-channel-inputsettings-denoisefilter"></a>
Enable or disable the denoise filter when filtering\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterStrength`  <a name="cfn-medialive-channel-inputsettings-filterstrength"></a>
Adjusts the magnitude of filtering from 1 \(minimal\) to 5 \(strongest\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputFilter`  <a name="cfn-medialive-channel-inputsettings-inputfilter"></a>
Turns on the filter for this input\. MPEG\-2 inputs have the deblocking filter enabled by default\. 1\) auto \- filtering will be applied depending on input type/quality 2\) disabled \- no filtering will be applied to the input 3\) forced \- filtering will be applied regardless of input type  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInputSettings`  <a name="cfn-medialive-channel-inputsettings-networkinputsettings"></a>
Input settings\.  
*Required*: No  
*Type*: [NetworkInputSettings](aws-properties-medialive-channel-networkinputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Smpte2038DataPreference`  <a name="cfn-medialive-channel-inputsettings-smpte2038datapreference"></a>
Specifies whether to extract applicable ancillary data from a SMPTE\-2038 source in this input\. Applicable data types are captions, timecode, AFD, and SCTE\-104 messages\. \- PREFER: Extract from SMPTE\-2038 if present in this input, otherwise extract from another source \(if any\)\. \- IGNORE: Never extract any ancillary data from SMPTE\-2038\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEndBehavior`  <a name="cfn-medialive-channel-inputsettings-sourceendbehavior"></a>
Loop input if it is a file\. This allows a file input to be streamed indefinitely\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoSelector`  <a name="cfn-medialive-channel-inputsettings-videoselector"></a>
Informs which video elementary stream to decode for input types that have multiple available\.  
*Required*: No  
*Type*: [VideoSelector](aws-properties-medialive-channel-videoselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)