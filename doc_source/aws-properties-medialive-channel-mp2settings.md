# AWS::MediaLive::Channel Mp2Settings<a name="aws-properties-medialive-channel-mp2settings"></a>

The configuration for this MP2 audio\.

The parent of this entity is AudioCodecSettings\.

## Syntax<a name="aws-properties-medialive-channel-mp2settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mp2settings-syntax.json"></a>

```
{
  "[Bitrate](#cfn-medialive-channel-mp2settings-bitrate)" : Double,
  "[CodingMode](#cfn-medialive-channel-mp2settings-codingmode)" : String,
  "[SampleRate](#cfn-medialive-channel-mp2settings-samplerate)" : Double
}
```

### YAML<a name="aws-properties-medialive-channel-mp2settings-syntax.yaml"></a>

```
  [Bitrate](#cfn-medialive-channel-mp2settings-bitrate): Double
  [CodingMode](#cfn-medialive-channel-mp2settings-codingmode): String
  [SampleRate](#cfn-medialive-channel-mp2settings-samplerate): Double
```

## Properties<a name="aws-properties-medialive-channel-mp2settings-properties"></a>

`Bitrate`  <a name="cfn-medialive-channel-mp2settings-bitrate"></a>
The average bitrate in bits/second\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodingMode`  <a name="cfn-medialive-channel-mp2settings-codingmode"></a>
The MPEG2 Audio coding mode\. Valid values are codingMode10 \(for mono\) or codingMode20 \(for stereo\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleRate`  <a name="cfn-medialive-channel-mp2settings-samplerate"></a>
The sample rate in Hz\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)