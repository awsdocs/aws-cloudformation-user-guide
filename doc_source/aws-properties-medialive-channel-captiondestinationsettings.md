# AWS::MediaLive::Channel CaptionDestinationSettings<a name="aws-properties-medialive-channel-captiondestinationsettings"></a>

This element configures the format for one output captions encode\. In this element, include only one type of the 'destination' child elements\. This element belongs to CaptionDescription\.

## Syntax<a name="aws-properties-medialive-channel-captiondestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captiondestinationsettings-syntax.json"></a>

```
{
  "[AribDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-aribdestinationsettings)" : AribDestinationSettings,
  "[BurnInDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-burnindestinationsettings)" : BurnInDestinationSettings,
  "[DvbSubDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-dvbsubdestinationsettings)" : DvbSubDestinationSettings,
  "[EbuTtDDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-ebuttddestinationsettings)" : EbuTtDDestinationSettings,
  "[EmbeddedDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-embeddeddestinationsettings)" : EmbeddedDestinationSettings,
  "[EmbeddedPlusScte20DestinationSettings](#cfn-medialive-channel-captiondestinationsettings-embeddedplusscte20destinationsettings)" : EmbeddedPlusScte20DestinationSettings,
  "[RtmpCaptionInfoDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-rtmpcaptioninfodestinationsettings)" : RtmpCaptionInfoDestinationSettings,
  "[Scte20PlusEmbeddedDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-scte20plusembeddeddestinationsettings)" : Scte20PlusEmbeddedDestinationSettings,
  "[Scte27DestinationSettings](#cfn-medialive-channel-captiondestinationsettings-scte27destinationsettings)" : Scte27DestinationSettings,
  "[SmpteTtDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-smptettdestinationsettings)" : SmpteTtDestinationSettings,
  "[TeletextDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-teletextdestinationsettings)" : TeletextDestinationSettings,
  "[TtmlDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-ttmldestinationsettings)" : TtmlDestinationSettings,
  "[WebvttDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-webvttdestinationsettings)" : WebvttDestinationSettings
}
```

### YAML<a name="aws-properties-medialive-channel-captiondestinationsettings-syntax.yaml"></a>

```
  [AribDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-aribdestinationsettings): 
    AribDestinationSettings
  [BurnInDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-burnindestinationsettings): 
    BurnInDestinationSettings
  [DvbSubDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-dvbsubdestinationsettings): 
    DvbSubDestinationSettings
  [EbuTtDDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-ebuttddestinationsettings): 
    EbuTtDDestinationSettings
  [EmbeddedDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-embeddeddestinationsettings): 
    EmbeddedDestinationSettings
  [EmbeddedPlusScte20DestinationSettings](#cfn-medialive-channel-captiondestinationsettings-embeddedplusscte20destinationsettings): 
    EmbeddedPlusScte20DestinationSettings
  [RtmpCaptionInfoDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-rtmpcaptioninfodestinationsettings): 
    RtmpCaptionInfoDestinationSettings
  [Scte20PlusEmbeddedDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-scte20plusembeddeddestinationsettings): 
    Scte20PlusEmbeddedDestinationSettings
  [Scte27DestinationSettings](#cfn-medialive-channel-captiondestinationsettings-scte27destinationsettings): 
    Scte27DestinationSettings
  [SmpteTtDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-smptettdestinationsettings): 
    SmpteTtDestinationSettings
  [TeletextDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-teletextdestinationsettings): 
    TeletextDestinationSettings
  [TtmlDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-ttmldestinationsettings): 
    TtmlDestinationSettings
  [WebvttDestinationSettings](#cfn-medialive-channel-captiondestinationsettings-webvttdestinationsettings): 
    WebvttDestinationSettings
```

## Properties<a name="aws-properties-medialive-channel-captiondestinationsettings-properties"></a>

`AribDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-aribdestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the ARIB format\.  
*Required*: No  
*Type*: [AribDestinationSettings](aws-properties-medialive-channel-aribdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BurnInDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-burnindestinationsettings"></a>
Include this element if you want to set up the output captions encode to use burned\-in captions\.  
*Required*: No  
*Type*: [BurnInDestinationSettings](aws-properties-medialive-channel-burnindestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbSubDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-dvbsubdestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the DVB\-Sub format\.  
*Required*: No  
*Type*: [DvbSubDestinationSettings](aws-properties-medialive-channel-dvbsubdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbuTtDDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-ebuttddestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the EBU\-TT format\.  
*Required*: No  
*Type*: [EbuTtDDestinationSettings](aws-properties-medialive-channel-ebuttddestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmbeddedDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-embeddeddestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the embedded format\.  
*Required*: No  
*Type*: [EmbeddedDestinationSettings](aws-properties-medialive-channel-embeddeddestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmbeddedPlusScte20DestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-embeddedplusscte20destinationsettings"></a>
Include this element if you want to set up the output captions encode to use the embedded format and the SCTE\-20 format \(with embedded appearing first in the encode\)\.  
*Required*: No  
*Type*: [EmbeddedPlusScte20DestinationSettings](aws-properties-medialive-channel-embeddedplusscte20destinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RtmpCaptionInfoDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-rtmpcaptioninfodestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the RTMP CaptionInfo format\.  
*Required*: No  
*Type*: [RtmpCaptionInfoDestinationSettings](aws-properties-medialive-channel-rtmpcaptioninfodestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte20PlusEmbeddedDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-scte20plusembeddeddestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the SCTE\-20 format and the embedded format \(with SCTE\-20 appearing first in the encode\)\.  
*Required*: No  
*Type*: [Scte20PlusEmbeddedDestinationSettings](aws-properties-medialive-channel-scte20plusembeddeddestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte27DestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-scte27destinationsettings"></a>
Include this element if you want to set up the output captions encode to use the SCTE\-27 format\.  
*Required*: No  
*Type*: [Scte27DestinationSettings](aws-properties-medialive-channel-scte27destinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmpteTtDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-smptettdestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the SMPTE\-TT format\.  
*Required*: No  
*Type*: [SmpteTtDestinationSettings](aws-properties-medialive-channel-smptettdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeletextDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-teletextdestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the Teletext format\.  
*Required*: No  
*Type*: [TeletextDestinationSettings](aws-properties-medialive-channel-teletextdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TtmlDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-ttmldestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the TTML format\.  
*Required*: No  
*Type*: [TtmlDestinationSettings](aws-properties-medialive-channel-ttmldestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebvttDestinationSettings`  <a name="cfn-medialive-channel-captiondestinationsettings-webvttdestinationsettings"></a>
Include this element if you want to set up the output captions encode to use the Web\-VTT format\.  
*Required*: No  
*Type*: [WebvttDestinationSettings](aws-properties-medialive-channel-webvttdestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)