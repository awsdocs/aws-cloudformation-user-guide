# AWS::MediaLive::Channel Mpeg2FilterSettings<a name="aws-properties-medialive-channel-mpeg2filtersettings"></a>

Settings to configure video filters that apply to the MPEG\-2 codec\.

The parent of this entity is Mpeg2FilterSettings\.

## Syntax<a name="aws-properties-medialive-channel-mpeg2filtersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mpeg2filtersettings-syntax.json"></a>

```
{
  "[TemporalFilterSettings](#cfn-medialive-channel-mpeg2filtersettings-temporalfiltersettings)" : TemporalFilterSettings
}
```

### YAML<a name="aws-properties-medialive-channel-mpeg2filtersettings-syntax.yaml"></a>

```
  [TemporalFilterSettings](#cfn-medialive-channel-mpeg2filtersettings-temporalfiltersettings): 
    TemporalFilterSettings
```

## Properties<a name="aws-properties-medialive-channel-mpeg2filtersettings-properties"></a>

`TemporalFilterSettings`  <a name="cfn-medialive-channel-mpeg2filtersettings-temporalfiltersettings"></a>
Settings for applying the temporal filter to the video\.   
*Required*: No  
*Type*: [TemporalFilterSettings](aws-properties-medialive-channel-temporalfiltersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)