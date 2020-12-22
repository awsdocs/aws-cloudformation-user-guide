# AWS::MediaLive::Channel BurnInDestinationSettings<a name="aws-properties-medialive-channel-burnindestinationsettings"></a>

The settings for burn\-in captions in the output\.

The parent of this entity is CaptionDestinationSettings\.

## Syntax<a name="aws-properties-medialive-channel-burnindestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-burnindestinationsettings-syntax.json"></a>

```
{
  "[Alignment](#cfn-medialive-channel-burnindestinationsettings-alignment)" : String,
  "[BackgroundColor](#cfn-medialive-channel-burnindestinationsettings-backgroundcolor)" : String,
  "[BackgroundOpacity](#cfn-medialive-channel-burnindestinationsettings-backgroundopacity)" : Integer,
  "[Font](#cfn-medialive-channel-burnindestinationsettings-font)" : InputLocation,
  "[FontColor](#cfn-medialive-channel-burnindestinationsettings-fontcolor)" : String,
  "[FontOpacity](#cfn-medialive-channel-burnindestinationsettings-fontopacity)" : Integer,
  "[FontResolution](#cfn-medialive-channel-burnindestinationsettings-fontresolution)" : Integer,
  "[FontSize](#cfn-medialive-channel-burnindestinationsettings-fontsize)" : String,
  "[OutlineColor](#cfn-medialive-channel-burnindestinationsettings-outlinecolor)" : String,
  "[OutlineSize](#cfn-medialive-channel-burnindestinationsettings-outlinesize)" : Integer,
  "[ShadowColor](#cfn-medialive-channel-burnindestinationsettings-shadowcolor)" : String,
  "[ShadowOpacity](#cfn-medialive-channel-burnindestinationsettings-shadowopacity)" : Integer,
  "[ShadowXOffset](#cfn-medialive-channel-burnindestinationsettings-shadowxoffset)" : Integer,
  "[ShadowYOffset](#cfn-medialive-channel-burnindestinationsettings-shadowyoffset)" : Integer,
  "[TeletextGridControl](#cfn-medialive-channel-burnindestinationsettings-teletextgridcontrol)" : String,
  "[XPosition](#cfn-medialive-channel-burnindestinationsettings-xposition)" : Integer,
  "[YPosition](#cfn-medialive-channel-burnindestinationsettings-yposition)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-burnindestinationsettings-syntax.yaml"></a>

```
  [Alignment](#cfn-medialive-channel-burnindestinationsettings-alignment): String
  [BackgroundColor](#cfn-medialive-channel-burnindestinationsettings-backgroundcolor): String
  [BackgroundOpacity](#cfn-medialive-channel-burnindestinationsettings-backgroundopacity): Integer
  [Font](#cfn-medialive-channel-burnindestinationsettings-font): 
    InputLocation
  [FontColor](#cfn-medialive-channel-burnindestinationsettings-fontcolor): String
  [FontOpacity](#cfn-medialive-channel-burnindestinationsettings-fontopacity): Integer
  [FontResolution](#cfn-medialive-channel-burnindestinationsettings-fontresolution): Integer
  [FontSize](#cfn-medialive-channel-burnindestinationsettings-fontsize): String
  [OutlineColor](#cfn-medialive-channel-burnindestinationsettings-outlinecolor): String
  [OutlineSize](#cfn-medialive-channel-burnindestinationsettings-outlinesize): Integer
  [ShadowColor](#cfn-medialive-channel-burnindestinationsettings-shadowcolor): String
  [ShadowOpacity](#cfn-medialive-channel-burnindestinationsettings-shadowopacity): Integer
  [ShadowXOffset](#cfn-medialive-channel-burnindestinationsettings-shadowxoffset): Integer
  [ShadowYOffset](#cfn-medialive-channel-burnindestinationsettings-shadowyoffset): Integer
  [TeletextGridControl](#cfn-medialive-channel-burnindestinationsettings-teletextgridcontrol): String
  [XPosition](#cfn-medialive-channel-burnindestinationsettings-xposition): Integer
  [YPosition](#cfn-medialive-channel-burnindestinationsettings-yposition): Integer
```

## Properties<a name="aws-properties-medialive-channel-burnindestinationsettings-properties"></a>

`Alignment`  <a name="cfn-medialive-channel-burnindestinationsettings-alignment"></a>
If no explicit xPosition or yPosition is provided, setting alignment to centered places the captions at the bottom center of the output\. Similarly, setting a left alignment aligns captions to the bottom left of the output\. If x and y positions are specified in conjunction with the alignment parameter, the font is justified \(either left or centered\) relative to those coordinates\. Selecting "smart" justification left\-justifies live subtitles and center\-justifies pre\-recorded subtitles\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackgroundColor`  <a name="cfn-medialive-channel-burnindestinationsettings-backgroundcolor"></a>
Specifies the color of the rectangle behind the captions\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackgroundOpacity`  <a name="cfn-medialive-channel-burnindestinationsettings-backgroundopacity"></a>
Specifies the opacity of the background rectangle\. 255 is opaque; 0 is transparent\. Keeping this parameter blank is equivalent to setting it to 0 \(transparent\)\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Font`  <a name="cfn-medialive-channel-burnindestinationsettings-font"></a>
The external font file that is used for captions burn\-in\. The file extension must be \.ttf or \.tte\. Although you can select output fonts for many different types of input captions, embedded, STL, and Teletext sources use a strict grid system\. Using external fonts with these captions sources could cause an unexpected display of proportional fonts\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontColor`  <a name="cfn-medialive-channel-burnindestinationsettings-fontcolor"></a>
Specifies the color of the burned\-in captions\. This option is not valid for source captions that are STL, 608/embedded, or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontOpacity`  <a name="cfn-medialive-channel-burnindestinationsettings-fontopacity"></a>
Specifies the opacity of the burned\-in captions\. 255 is opaque; 0 is transparent\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontResolution`  <a name="cfn-medialive-channel-burnindestinationsettings-fontresolution"></a>
The font resolution in DPI \(dots per inch\)\. The default is 96 dpi\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontSize`  <a name="cfn-medialive-channel-burnindestinationsettings-fontsize"></a>
When set to auto, fontSize scales depending on the size of the output\. Providing a positive integer specifies the exact font size in points\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlineColor`  <a name="cfn-medialive-channel-burnindestinationsettings-outlinecolor"></a>
Specifies the font outline color\. This option is not valid for source captions that are either 608/embedded or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlineSize`  <a name="cfn-medialive-channel-burnindestinationsettings-outlinesize"></a>
Specifies font outline size in pixels\. This option is not valid for source captions that are either 608/embedded or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowColor`  <a name="cfn-medialive-channel-burnindestinationsettings-shadowcolor"></a>
Specifies the color of the shadow cast by the captions\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowOpacity`  <a name="cfn-medialive-channel-burnindestinationsettings-shadowopacity"></a>
Specifies the opacity of the shadow\. 255 is opaque; 0 is transparent\. Keeping this parameter blank is equivalent to setting it to 0 \(transparent\)\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowXOffset`  <a name="cfn-medialive-channel-burnindestinationsettings-shadowxoffset"></a>
Specifies the horizontal offset of the shadow that is relative to the captions in pixels\. A value of \-2 would result in a shadow offset 2 pixels to the left\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowYOffset`  <a name="cfn-medialive-channel-burnindestinationsettings-shadowyoffset"></a>
Specifies the vertical offset of the shadow that is relative to the captions in pixels\. A value of \-2 would result in a shadow offset 2 pixels above the text\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeletextGridControl`  <a name="cfn-medialive-channel-burnindestinationsettings-teletextgridcontrol"></a>
Controls whether a fixed grid size is used to generate the output subtitles bitmap\. This applies only to Teletext inputs and DVB\-Sub/Burn\-in outputs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XPosition`  <a name="cfn-medialive-channel-burnindestinationsettings-xposition"></a>
Specifies the horizontal position of the captions relative to the left side of the output in pixels\. A value of 10 would result in the captions starting 10 pixels from the left of the output\. If no explicit xPosition is provided, the horizontal captions position is determined by the alignment parameter\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YPosition`  <a name="cfn-medialive-channel-burnindestinationsettings-yposition"></a>
Specifies the vertical position of the captions relative to the top of the output in pixels\. A value of 10 would result in the captions starting 10 pixels from the top of the output\. If no explicit yPosition is provided, the captions are positioned towards the bottom of the output\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)