# AWS::MediaLive::Channel EbuTtDDestinationSettings<a name="aws-properties-medialive-channel-ebuttddestinationsettings"></a>

Configures the output captions encode for the EBU\-TT format\. This element belongs to CaptionDestinationSettings \.

## Syntax<a name="aws-properties-medialive-channel-ebuttddestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-ebuttddestinationsettings-syntax.json"></a>

```
{
  "[FillLineGap](#cfn-medialive-channel-ebuttddestinationsettings-filllinegap)" : String,
  "[FontFamily](#cfn-medialive-channel-ebuttddestinationsettings-fontfamily)" : String,
  "[StyleControl](#cfn-medialive-channel-ebuttddestinationsettings-stylecontrol)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-ebuttddestinationsettings-syntax.yaml"></a>

```
  [FillLineGap](#cfn-medialive-channel-ebuttddestinationsettings-filllinegap): String
  [FontFamily](#cfn-medialive-channel-ebuttddestinationsettings-fontfamily): String
  [StyleControl](#cfn-medialive-channel-ebuttddestinationsettings-stylecontrol): String
```

## Properties<a name="aws-properties-medialive-channel-ebuttddestinationsettings-properties"></a>

`FillLineGap`  <a name="cfn-medialive-channel-ebuttddestinationsettings-filllinegap"></a>
Fills the gap between the lines \(in multi\-line captions\) with the captions background color \(as specified in the input captions\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontFamily`  <a name="cfn-medialive-channel-ebuttddestinationsettings-fontfamily"></a>
Specify font families for the captions, as a comma\-separated list of font names, in order of preference\. The name can be a font family \(e\.g\. "Arial"\), or a generic font family \(e\.g\. "serif"\), or "default" \(let the downstream player choose the font\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleControl`  <a name="cfn-medialive-channel-ebuttddestinationsettings-stylecontrol"></a>
When set to passthrough, passes through style and position information from a TTML\-like input source \(TTML, SMPTE\-TT, CFF\-TT\) to the CFF\-TT output or EBU\-TT\-D output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)