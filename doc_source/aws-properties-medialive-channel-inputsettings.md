# AWS::MediaLive::Channel InputSettings<a name="aws-properties-medialive-channel-inputsettings"></a>

This element identifies the video, audio and captions to extract from the input, and customizes some of the handling of the input\. This element belongs to InputAttachment\.

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
  [SourceEndBehavior](#cfn-medialive-channel-inputsettings-sourceendbehavior): String
  [VideoSelector](#cfn-medialive-channel-inputsettings-videoselector): 
    VideoSelector
```

## Properties<a name="aws-properties-medialive-channel-inputsettings-properties"></a>

`AudioSelectors`  <a name="cfn-medialive-channel-inputsettings-audioselectors"></a>
The optional list of audio selectors for this input\. Each audio selector identifes one audio asset to extract from the input\.  
*Required*: No  
*Type*: List of [AudioSelector](aws-properties-medialive-channel-audioselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionSelectors`  <a name="cfn-medialive-channel-inputsettings-captionselectors"></a>
The optional list of caption selectors for this input\. Each caption selector identifes one captions asset to extract from the input\.  
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
Turns on the filter for this input\. MPEG\-2 inputs have the deblocking filter enabled by default\. 1\) auto \- filtering will be applied depending on input type/quality 2\) disabled \- no filtering will be applied to the input 3\) forced \- filtering will be applied regardless of input type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInputSettings`  <a name="cfn-medialive-channel-inputsettings-networkinputsettings"></a>
Include this element only if the InputAttachment specifies an inputId that identifies an HLS input\.  
*Required*: No  
*Type*: [NetworkInputSettings](aws-properties-medialive-channel-networkinputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEndBehavior`  <a name="cfn-medialive-channel-inputsettings-sourceendbehavior"></a>
Loop input if it is a file\. This allows a file input to be streamed indefinitely\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoSelector`  <a name="cfn-medialive-channel-inputsettings-videoselector"></a>
The video selector identifies the video asset to extract from the input\. This element is optional if the input contains only one video asset; MediaLive will automatically extract that single asset\. This element is required if the input contains more than one video asset, and/or if you want to configure the color space in the video\.  
*Required*: No  
*Type*: [VideoSelector](aws-properties-medialive-channel-videoselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)