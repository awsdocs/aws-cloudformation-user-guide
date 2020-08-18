# AWS::MediaLive::Channel CaptionSelectorSettings<a name="aws-properties-medialive-channel-captionselectorsettings"></a>

Captions Selector Settings

The parent of this entity is CaptionSelector\.

## Syntax<a name="aws-properties-medialive-channel-captionselectorsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captionselectorsettings-syntax.json"></a>

```
{
  "[AribSourceSettings](#cfn-medialive-channel-captionselectorsettings-aribsourcesettings)" : AribSourceSettings,
  "[DvbSubSourceSettings](#cfn-medialive-channel-captionselectorsettings-dvbsubsourcesettings)" : DvbSubSourceSettings,
  "[EmbeddedSourceSettings](#cfn-medialive-channel-captionselectorsettings-embeddedsourcesettings)" : EmbeddedSourceSettings,
  "[Scte20SourceSettings](#cfn-medialive-channel-captionselectorsettings-scte20sourcesettings)" : Scte20SourceSettings,
  "[Scte27SourceSettings](#cfn-medialive-channel-captionselectorsettings-scte27sourcesettings)" : Scte27SourceSettings,
  "[TeletextSourceSettings](#cfn-medialive-channel-captionselectorsettings-teletextsourcesettings)" : TeletextSourceSettings
}
```

### YAML<a name="aws-properties-medialive-channel-captionselectorsettings-syntax.yaml"></a>

```
  [AribSourceSettings](#cfn-medialive-channel-captionselectorsettings-aribsourcesettings): 
    AribSourceSettings
  [DvbSubSourceSettings](#cfn-medialive-channel-captionselectorsettings-dvbsubsourcesettings): 
    DvbSubSourceSettings
  [EmbeddedSourceSettings](#cfn-medialive-channel-captionselectorsettings-embeddedsourcesettings): 
    EmbeddedSourceSettings
  [Scte20SourceSettings](#cfn-medialive-channel-captionselectorsettings-scte20sourcesettings): 
    Scte20SourceSettings
  [Scte27SourceSettings](#cfn-medialive-channel-captionselectorsettings-scte27sourcesettings): 
    Scte27SourceSettings
  [TeletextSourceSettings](#cfn-medialive-channel-captionselectorsettings-teletextsourcesettings): 
    TeletextSourceSettings
```

## Properties<a name="aws-properties-medialive-channel-captionselectorsettings-properties"></a>

`AribSourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-aribsourcesettings"></a>
Information about the ARIB captions to extract from the input\.  
*Required*: No  
*Type*: [AribSourceSettings](aws-properties-medialive-channel-aribsourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbSubSourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-dvbsubsourcesettings"></a>
Information about the DVB Sub captions to extract from the input\.  
*Required*: No  
*Type*: [DvbSubSourceSettings](aws-properties-medialive-channel-dvbsubsourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmbeddedSourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-embeddedsourcesettings"></a>
Information about the embedded captions to extract from the input\.  
*Required*: No  
*Type*: [EmbeddedSourceSettings](aws-properties-medialive-channel-embeddedsourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte20SourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-scte20sourcesettings"></a>
Information about the SCTE\-20 captions to extract from the input\.  
*Required*: No  
*Type*: [Scte20SourceSettings](aws-properties-medialive-channel-scte20sourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte27SourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-scte27sourcesettings"></a>
Information about the SCTE\-27 captions to extract from the input\.  
*Required*: No  
*Type*: [Scte27SourceSettings](aws-properties-medialive-channel-scte27sourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TeletextSourceSettings`  <a name="cfn-medialive-channel-captionselectorsettings-teletextsourcesettings"></a>
Information about the Teletext captions to extract from the input\.  
*Required*: No  
*Type*: [TeletextSourceSettings](aws-properties-medialive-channel-teletextsourcesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)