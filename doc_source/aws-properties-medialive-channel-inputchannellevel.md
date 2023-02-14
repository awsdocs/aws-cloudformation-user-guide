# AWS::MediaLive::Channel InputChannelLevel<a name="aws-properties-medialive-channel-inputchannellevel"></a>

The setting to remix the audio\.

The parent of this entity is AudioChannelMappings\.

## Syntax<a name="aws-properties-medialive-channel-inputchannellevel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputchannellevel-syntax.json"></a>

```
{
  "[Gain](#cfn-medialive-channel-inputchannellevel-gain)" : Integer,
  "[InputChannel](#cfn-medialive-channel-inputchannellevel-inputchannel)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-inputchannellevel-syntax.yaml"></a>

```
  [Gain](#cfn-medialive-channel-inputchannellevel-gain): Integer
  [InputChannel](#cfn-medialive-channel-inputchannellevel-inputchannel): Integer
```

## Properties<a name="aws-properties-medialive-channel-inputchannellevel-properties"></a>

`Gain`  <a name="cfn-medialive-channel-inputchannellevel-gain"></a>
The remixing value\. Units are in dB, and acceptable values are within the range from \-60 \(mute\) to 6 dB\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputChannel`  <a name="cfn-medialive-channel-inputchannellevel-inputchannel"></a>
The index of the input channel that is used as a source\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)