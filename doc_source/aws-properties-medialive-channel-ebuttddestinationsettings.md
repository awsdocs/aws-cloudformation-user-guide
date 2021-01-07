# AWS::MediaLive::Channel EbuTtDDestinationSettings<a name="aws-properties-medialive-channel-ebuttddestinationsettings"></a>

Ebu Tt DDestination Settings

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
Specifies how to handle the gap between the lines \(in multi\-line captions\)\. \- enabled: Fill with the captions background color \(as specified in the input captions\)\. \- disabled: Leave the gap unfilled\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontFamily`  <a name="cfn-medialive-channel-ebuttddestinationsettings-fontfamily"></a>
Specifies the font family to include in the font data attached to the EBU\-TT captions\. Valid only if styleControl is set to include\. If you leave this field empty, the font family is set to "monospaced"\. \(If styleControl is set to exclude, the font family is always set to "monospaced"\.\) You specify only the font family\. All other style information \(color, bold, position and so on\) is copied from the input captions\. The size is always set to 100% to allow the downstream player to choose the size\. \- Enter a list of font families, as a comma\-separated list of font names, in order of preference\. The name can be a font family \(such as “Arial”\), or a generic font family \(such as “serif”\), or “default” \(to let the downstream player choose the font\)\. \- Leave blank to set the family to “monospace”\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleControl`  <a name="cfn-medialive-channel-ebuttddestinationsettings-stylecontrol"></a>
Specifies the style information \(font color, font position, and so on\) to include in the font data that is attached to the EBU\-TT captions\. \- include: Take the style information \(font color, font position, and so on\) from the source captions and include that information in the font data attached to the EBU\-TT captions\. This option is valid only if the source captions are Embedded or Teletext\. \- exclude: In the font data attached to the EBU\-TT captions, set the font family to "monospaced"\. Do not include any other style information\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)