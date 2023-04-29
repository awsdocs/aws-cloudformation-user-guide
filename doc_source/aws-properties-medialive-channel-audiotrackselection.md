# AWS::MediaLive::Channel AudioTrackSelection<a name="aws-properties-medialive-channel-audiotrackselection"></a>

Information about the audio track to extract\.

The parent of this entity is AudioSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-audiotrackselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiotrackselection-syntax.json"></a>

```
{
  "[DolbyEDecode](#cfn-medialive-channel-audiotrackselection-dolbyedecode)" : AudioDolbyEDecode,
  "[Tracks](#cfn-medialive-channel-audiotrackselection-tracks)" : [ AudioTrack, ... ]
}
```

### YAML<a name="aws-properties-medialive-channel-audiotrackselection-syntax.yaml"></a>

```
  [DolbyEDecode](#cfn-medialive-channel-audiotrackselection-dolbyedecode): 
    AudioDolbyEDecode
  [Tracks](#cfn-medialive-channel-audiotrackselection-tracks): 
    - AudioTrack
```

## Properties<a name="aws-properties-medialive-channel-audiotrackselection-properties"></a>

`DolbyEDecode`  <a name="cfn-medialive-channel-audiotrackselection-dolbyedecode"></a>
Property description not available\.  
*Required*: No  
*Type*: [AudioDolbyEDecode](aws-properties-medialive-channel-audiodolbyedecode.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tracks`  <a name="cfn-medialive-channel-audiotrackselection-tracks"></a>
Selects one or more unique audio tracks from within a source\.  
*Required*: No  
*Type*: List of [AudioTrack](aws-properties-medialive-channel-audiotrack.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)