# AWS::MediaLive::Channel UdpGroupSettings<a name="aws-properties-medialive-channel-udpgroupsettings"></a>

The configuration of a UDP output group\.

The parent of this entity is OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-udpgroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-udpgroupsettings-syntax.json"></a>

```
{
  "[InputLossAction](#cfn-medialive-channel-udpgroupsettings-inputlossaction)" : String,
  "[TimedMetadataId3Frame](#cfn-medialive-channel-udpgroupsettings-timedmetadataid3frame)" : String,
  "[TimedMetadataId3Period](#cfn-medialive-channel-udpgroupsettings-timedmetadataid3period)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-udpgroupsettings-syntax.yaml"></a>

```
  [InputLossAction](#cfn-medialive-channel-udpgroupsettings-inputlossaction): String
  [TimedMetadataId3Frame](#cfn-medialive-channel-udpgroupsettings-timedmetadataid3frame): String
  [TimedMetadataId3Period](#cfn-medialive-channel-udpgroupsettings-timedmetadataid3period): Integer
```

## Properties<a name="aws-properties-medialive-channel-udpgroupsettings-properties"></a>

`InputLossAction`  <a name="cfn-medialive-channel-udpgroupsettings-inputlossaction"></a>
Specifies the behavior of the last resort when the input video is lost, and no more backup inputs are available\. When dropTs is selected, the entire transport stream stops emitting\. When dropProgram is selected, the program can be dropped from the transport stream \(and replaced with null packets to meet the TS bitrate requirement\)\. Or when emitProgram is selected, the transport stream continues to be produced normally with repeat frames, black frames, or slate frames substituted for the absent input video\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Frame`  <a name="cfn-medialive-channel-udpgroupsettings-timedmetadataid3frame"></a>
Indicates the ID3 frame that has the timecode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Period`  <a name="cfn-medialive-channel-udpgroupsettings-timedmetadataid3period"></a>
The timed metadata interval in seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)