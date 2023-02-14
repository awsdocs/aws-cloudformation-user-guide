# AWS::MediaLive::Channel AudioWatermarkSettings<a name="aws-properties-medialive-channel-audiowatermarksettings"></a>

Audio Watermark Settings

The parent of this entity is AudioDescription\.

## Syntax<a name="aws-properties-medialive-channel-audiowatermarksettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiowatermarksettings-syntax.json"></a>

```
{
  "[NielsenWatermarksSettings](#cfn-medialive-channel-audiowatermarksettings-nielsenwatermarkssettings)" : NielsenWatermarksSettings
}
```

### YAML<a name="aws-properties-medialive-channel-audiowatermarksettings-syntax.yaml"></a>

```
  [NielsenWatermarksSettings](#cfn-medialive-channel-audiowatermarksettings-nielsenwatermarkssettings): 
    NielsenWatermarksSettings
```

## Properties<a name="aws-properties-medialive-channel-audiowatermarksettings-properties"></a>

`NielsenWatermarksSettings`  <a name="cfn-medialive-channel-audiowatermarksettings-nielsenwatermarkssettings"></a>
Settings to configure Nielsen Watermarks in the audio encode  
*Required*: No  
*Type*: [NielsenWatermarksSettings](aws-properties-medialive-channel-nielsenwatermarkssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)