# AWS::MediaLive::Channel DvbSubDestinationSettings<a name="aws-properties-medialive-channel-dvbsubdestinationsettings"></a>

The settings for DVB Sub captions in the output\.

The parent of this entity is CaptionDestinationSettings\.

## Syntax<a name="aws-properties-medialive-channel-dvbsubdestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbsubdestinationsettings-syntax.json"></a>

```
{
  "[Alignment](#cfn-medialive-channel-dvbsubdestinationsettings-alignment)" : String,
  "[BackgroundColor](#cfn-medialive-channel-dvbsubdestinationsettings-backgroundcolor)" : String,
  "[BackgroundOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-backgroundopacity)" : Integer,
  "[Font](#cfn-medialive-channel-dvbsubdestinationsettings-font)" : InputLocation,
  "[FontColor](#cfn-medialive-channel-dvbsubdestinationsettings-fontcolor)" : String,
  "[FontOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-fontopacity)" : Integer,
  "[FontResolution](#cfn-medialive-channel-dvbsubdestinationsettings-fontresolution)" : Integer,
  "[FontSize](#cfn-medialive-channel-dvbsubdestinationsettings-fontsize)" : String,
  "[OutlineColor](#cfn-medialive-channel-dvbsubdestinationsettings-outlinecolor)" : String,
  "[OutlineSize](#cfn-medialive-channel-dvbsubdestinationsettings-outlinesize)" : Integer,
  "[ShadowColor](#cfn-medialive-channel-dvbsubdestinationsettings-shadowcolor)" : String,
  "[ShadowOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-shadowopacity)" : Integer,
  "[ShadowXOffset](#cfn-medialive-channel-dvbsubdestinationsettings-shadowxoffset)" : Integer,
  "[ShadowYOffset](#cfn-medialive-channel-dvbsubdestinationsettings-shadowyoffset)" : Integer,
  "[TeletextGridControl](#cfn-medialive-channel-dvbsubdestinationsettings-teletextgridcontrol)" : String,
  "[XPosition](#cfn-medialive-channel-dvbsubdestinationsettings-xposition)" : Integer,
  "[YPosition](#cfn-medialive-channel-dvbsubdestinationsettings-yposition)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-dvbsubdestinationsettings-syntax.yaml"></a>

```
  [Alignment](#cfn-medialive-channel-dvbsubdestinationsettings-alignment): String
  [BackgroundColor](#cfn-medialive-channel-dvbsubdestinationsettings-backgroundcolor): String
  [BackgroundOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-backgroundopacity): Integer
  [Font](#cfn-medialive-channel-dvbsubdestinationsettings-font): 
    InputLocation
  [FontColor](#cfn-medialive-channel-dvbsubdestinationsettings-fontcolor): String
  [FontOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-fontopacity): Integer
  [FontResolution](#cfn-medialive-channel-dvbsubdestinationsettings-fontresolution): Integer
  [FontSize](#cfn-medialive-channel-dvbsubdestinationsettings-fontsize): String
  [OutlineColor](#cfn-medialive-channel-dvbsubdestinationsettings-outlinecolor): String
  [OutlineSize](#cfn-medialive-channel-dvbsubdestinationsettings-outlinesize): Integer
  [ShadowColor](#cfn-medialive-channel-dvbsubdestinationsettings-shadowcolor): String
  [ShadowOpacity](#cfn-medialive-channel-dvbsubdestinationsettings-shadowopacity): Integer
  [ShadowXOffset](#cfn-medialive-channel-dvbsubdestinationsettings-shadowxoffset): Integer
  [ShadowYOffset](#cfn-medialive-channel-dvbsubdestinationsettings-shadowyoffset): Integer
  [TeletextGridControl](#cfn-medialive-channel-dvbsubdestinationsettings-teletextgridcontrol): String
  [XPosition](#cfn-medialive-channel-dvbsubdestinationsettings-xposition): Integer
  [YPosition](#cfn-medialive-channel-dvbsubdestinationsettings-yposition): Integer
```

## Properties<a name="aws-properties-medialive-channel-dvbsubdestinationsettings-properties"></a>

`Alignment`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-alignment"></a>
If no explicit xPosition or yPosition is provided, setting the alignment to centered places the captions at the bottom center of the output\. Similarly, setting a left alignment aligns captions to the bottom left of the output\. If x and y positions are specified in conjunction with the alignment parameter, the font is justified \(either left or centered\) relative to those coordinates\. Selecting "smart" justification left\-justifies live subtitles and center\-justifies pre\-recorded subtitles\. This option is not valid for source captions that are STL or 608/embedded\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackgroundColor`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-backgroundcolor"></a>
Specifies the color of the rectangle behind the captions\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BackgroundOpacity`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-backgroundopacity"></a>
Specifies the opacity of the background rectangle\. 255 is opaque; 0 is transparent\. Keeping this parameter blank is equivalent to setting it to 0 \(transparent\)\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Font`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-font"></a>
The external font file that is used for captions burn\-in\. The file extension must be \.ttf or \.tte\. Although you can select output fonts for many different types of input captions, embedded, STL, and Teletext sources use a strict grid system\. Using external fonts with these captions sources could cause an unexpected display of proportional fonts\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontColor`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-fontcolor"></a>
Specifies the color of the burned\-in captions\. This option is not valid for source captions that are STL, 608/embedded, or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontOpacity`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-fontopacity"></a>
Specifies the opacity of the burned\-in captions\. 255 is opaque; 0 is transparent\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontResolution`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-fontresolution"></a>
The font resolution in DPI \(dots per inch\)\. The default is 96 dpi\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontSize`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-fontsize"></a>
When set to auto, fontSize scales depending on the size of the output\. Providing a positive integer specifies the exact font size in points\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlineColor`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-outlinecolor"></a>
Specifies the font outline color\. This option is not valid for source captions that are either 608/embedded or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutlineSize`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-outlinesize"></a>
Specifies the font outline size in pixels\. This option is not valid for source captions that are either 608/embedded or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowColor`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-shadowcolor"></a>
Specifies the color of the shadow that is cast by the captions\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowOpacity`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-shadowopacity"></a>
Specifies the opacity of the shadow\. 255 is opaque; 0 is transparent\. Keeping this parameter blank is equivalent to setting it to 0 \(transparent\)\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowXOffset`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-shadowxoffset"></a>
Specifies the horizontal offset of the shadow relative to the captions in pixels\. A value of \-2 would result in a shadow offset 2 pixels to the left\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShadowYOffset`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-shadowyoffset"></a>
Specifies the vertical offset of the shadow relative to the captions in pixels\. A value of \-2 would result in a shadow offset 2 pixels above the text\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeletextGridControl`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-teletextgridcontrol"></a>
Controls whether a fixed grid size is used to generate the output subtitles bitmap\. This applies to only Teletext inputs and DVB\-Sub/Burn\-in outputs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XPosition`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-xposition"></a>
Specifies the horizontal position of the captions relative to the left side of the output in pixels\. A value of 10 would result in the captions starting 10 pixels from the left of the output\. If no explicit xPosition is provided, the horizontal captions position is determined by the alignment parameter\. This option is not valid for source captions that are STL, 608/embedded, or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YPosition`  <a name="cfn-medialive-channel-dvbsubdestinationsettings-yposition"></a>
Specifies the vertical position of the captions relative to the top of the output in pixels\. A value of 10 would result in the captions starting 10 pixels from the top of the output\. If no explicit yPosition is provided, the captions are positioned towards the bottom of the output\. This option is not valid for source captions that are STL, 608/embedded, or Teletext\. These source settings are already pre\-defined by the captions stream\. All burn\-in and DVB\-Sub font settings must match\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)