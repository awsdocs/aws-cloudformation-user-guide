# AWS::MediaLive::Channel Fmp4HlsSettings<a name="aws-properties-medialive-channel-fmp4hlssettings"></a>

Fmp4 Hls Settings

## Syntax<a name="aws-properties-medialive-channel-fmp4hlssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-fmp4hlssettings-syntax.json"></a>

```
{
  "[AudioRenditionSets](#cfn-medialive-channel-fmp4hlssettings-audiorenditionsets)" : String,
  "[NielsenId3Behavior](#cfn-medialive-channel-fmp4hlssettings-nielsenid3behavior)" : String,
  "[TimedMetadataBehavior](#cfn-medialive-channel-fmp4hlssettings-timedmetadatabehavior)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-fmp4hlssettings-syntax.yaml"></a>

```
  [AudioRenditionSets](#cfn-medialive-channel-fmp4hlssettings-audiorenditionsets): String
  [NielsenId3Behavior](#cfn-medialive-channel-fmp4hlssettings-nielsenid3behavior): String
  [TimedMetadataBehavior](#cfn-medialive-channel-fmp4hlssettings-timedmetadatabehavior): String
```

## Properties<a name="aws-properties-medialive-channel-fmp4hlssettings-properties"></a>

`AudioRenditionSets`  <a name="cfn-medialive-channel-fmp4hlssettings-audiorenditionsets"></a>
List all the audio groups that are used with the video output stream\. Input all the audio GROUP\-IDs that are associated to the video, separate by ','\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenId3Behavior`  <a name="cfn-medialive-channel-fmp4hlssettings-nielsenid3behavior"></a>
If set to passthrough, Nielsen inaudible tones for media tracking will be detected in the input audio and an equivalent ID3 tag will be inserted in the output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataBehavior`  <a name="cfn-medialive-channel-fmp4hlssettings-timedmetadatabehavior"></a>
When set to passthrough, timed metadata is passed through from input to output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)