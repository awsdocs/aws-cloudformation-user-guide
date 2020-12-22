# AWS::MediaLive::Channel RemixSettings<a name="aws-properties-medialive-channel-remixsettings"></a>

The settings for remixing audio in the output\.

The parent of this entity is AudioDescription\.

## Syntax<a name="aws-properties-medialive-channel-remixsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-remixsettings-syntax.json"></a>

```
{
  "[ChannelMappings](#cfn-medialive-channel-remixsettings-channelmappings)" : [ AudioChannelMapping, ... ],
  "[ChannelsIn](#cfn-medialive-channel-remixsettings-channelsin)" : Integer,
  "[ChannelsOut](#cfn-medialive-channel-remixsettings-channelsout)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-remixsettings-syntax.yaml"></a>

```
  [ChannelMappings](#cfn-medialive-channel-remixsettings-channelmappings): 
    - AudioChannelMapping
  [ChannelsIn](#cfn-medialive-channel-remixsettings-channelsin): Integer
  [ChannelsOut](#cfn-medialive-channel-remixsettings-channelsout): Integer
```

## Properties<a name="aws-properties-medialive-channel-remixsettings-properties"></a>

`ChannelMappings`  <a name="cfn-medialive-channel-remixsettings-channelmappings"></a>
A mapping of input channels to output channels, with appropriate gain adjustments\.  
*Required*: No  
*Type*: List of [AudioChannelMapping](aws-properties-medialive-channel-audiochannelmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelsIn`  <a name="cfn-medialive-channel-remixsettings-channelsin"></a>
The number of input channels to be used\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelsOut`  <a name="cfn-medialive-channel-remixsettings-channelsout"></a>
The number of output channels to be produced\. Valid values: 1, 2, 4, 6, 8\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)