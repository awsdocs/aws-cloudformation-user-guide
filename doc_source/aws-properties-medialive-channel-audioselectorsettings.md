# AWS::MediaLive::Channel AudioSelectorSettings<a name="aws-properties-medialive-channel-audioselectorsettings"></a>

Information about the audio to extract from the input\.

The parent of this entity is AudioSelector\.

## Syntax<a name="aws-properties-medialive-channel-audioselectorsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audioselectorsettings-syntax.json"></a>

```
{
  "[AudioLanguageSelection](#cfn-medialive-channel-audioselectorsettings-audiolanguageselection)" : AudioLanguageSelection,
  "[AudioPidSelection](#cfn-medialive-channel-audioselectorsettings-audiopidselection)" : AudioPidSelection,
  "[AudioTrackSelection](#cfn-medialive-channel-audioselectorsettings-audiotrackselection)" : AudioTrackSelection
}
```

### YAML<a name="aws-properties-medialive-channel-audioselectorsettings-syntax.yaml"></a>

```
  [AudioLanguageSelection](#cfn-medialive-channel-audioselectorsettings-audiolanguageselection): 
    AudioLanguageSelection
  [AudioPidSelection](#cfn-medialive-channel-audioselectorsettings-audiopidselection): 
    AudioPidSelection
  [AudioTrackSelection](#cfn-medialive-channel-audioselectorsettings-audiotrackselection): 
    AudioTrackSelection
```

## Properties<a name="aws-properties-medialive-channel-audioselectorsettings-properties"></a>

`AudioLanguageSelection`  <a name="cfn-medialive-channel-audioselectorsettings-audiolanguageselection"></a>
The language code of the audio to select\.  
*Required*: No  
*Type*: [AudioLanguageSelection](aws-properties-medialive-channel-audiolanguageselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioPidSelection`  <a name="cfn-medialive-channel-audioselectorsettings-audiopidselection"></a>
The PID of the audio to select\.  
*Required*: No  
*Type*: [AudioPidSelection](aws-properties-medialive-channel-audiopidselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioTrackSelection`  <a name="cfn-medialive-channel-audioselectorsettings-audiotrackselection"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [AudioTrackSelection](aws-properties-medialive-channel-audiotrackselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)