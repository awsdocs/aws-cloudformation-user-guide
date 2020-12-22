# AWS::MediaLive::Channel AudioChannelMapping<a name="aws-properties-medialive-channel-audiochannelmapping"></a>

The settings for remixing audio\.

The parent of this entity is RemixSettings\.

## Syntax<a name="aws-properties-medialive-channel-audiochannelmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiochannelmapping-syntax.json"></a>

```
{
  "[InputChannelLevels](#cfn-medialive-channel-audiochannelmapping-inputchannellevels)" : [ InputChannelLevel, ... ],
  "[OutputChannel](#cfn-medialive-channel-audiochannelmapping-outputchannel)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-audiochannelmapping-syntax.yaml"></a>

```
  [InputChannelLevels](#cfn-medialive-channel-audiochannelmapping-inputchannellevels): 
    - InputChannelLevel
  [OutputChannel](#cfn-medialive-channel-audiochannelmapping-outputchannel): Integer
```

## Properties<a name="aws-properties-medialive-channel-audiochannelmapping-properties"></a>

`InputChannelLevels`  <a name="cfn-medialive-channel-audiochannelmapping-inputchannellevels"></a>
The indices and gain values for each input channel that should be remixed into this output channel\.  
*Required*: No  
*Type*: List of [InputChannelLevel](aws-properties-medialive-channel-inputchannellevel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputChannel`  <a name="cfn-medialive-channel-audiochannelmapping-outputchannel"></a>
The index of the output channel that is being produced\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)