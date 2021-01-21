# AWS::MediaLive::Channel AudioSilenceFailoverSettings<a name="aws-properties-medialive-channel-audiosilencefailoversettings"></a>

<a name="aws-properties-medialive-channel-audiosilencefailoversettings-description"></a>The `AudioSilenceFailoverSettings` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::MediaLive::Channel](aws-resource-medialive-channel.md)\.

## Syntax<a name="aws-properties-medialive-channel-audiosilencefailoversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiosilencefailoversettings-syntax.json"></a>

```
{
  "[AudioSelectorName](#cfn-medialive-channel-audiosilencefailoversettings-audioselectorname)" : String,
  "[AudioSilenceThresholdMsec](#cfn-medialive-channel-audiosilencefailoversettings-audiosilencethresholdmsec)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-audiosilencefailoversettings-syntax.yaml"></a>

```
  [AudioSelectorName](#cfn-medialive-channel-audiosilencefailoversettings-audioselectorname): String
  [AudioSilenceThresholdMsec](#cfn-medialive-channel-audiosilencefailoversettings-audiosilencethresholdmsec): Integer
```

## Properties<a name="aws-properties-medialive-channel-audiosilencefailoversettings-properties"></a>

`AudioSelectorName`  <a name="cfn-medialive-channel-audiosilencefailoversettings-audioselectorname"></a>
The name of the audio selector in the input that MediaLive should monitor to detect silence\. Select your most important rendition\. If you didn't create an audio selector in this input, leave blank\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioSilenceThresholdMsec`  <a name="cfn-medialive-channel-audiosilencefailoversettings-audiosilencethresholdmsec"></a>
The amount of time \(in milliseconds\) that the active input must be silent before automatic input failover occurs\. Silence is defined as audio loss or audio quieter than \-50 dBFS\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)