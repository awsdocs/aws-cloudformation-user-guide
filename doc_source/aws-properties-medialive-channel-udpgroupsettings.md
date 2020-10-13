# AWS::MediaLive::Channel UdpGroupSettings<a name="aws-properties-medialive-channel-udpgroupsettings"></a>

Identifies this output group as a UDP output group, and configures all the parts of the output group except for its outputs\. This element belongs to OutputGroupSettings\.

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
Specifies behavior of last resort when input video is lost, and no more backup inputs are available\. When dropTs is selected the entire transport stream will stop being emitted\. When dropProgram is selected the program can be dropped from the transport stream \(and replaced with null packets to meet the TS bitrate requirement\)\. Or, when emitProgram is chosen the transport stream will continue to be produced normally with repeat frames, black frames, or slate frames substituted for the absent input video\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Frame`  <a name="cfn-medialive-channel-udpgroupsettings-timedmetadataid3frame"></a>
Indicates ID3 frame that has the timecode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Period`  <a name="cfn-medialive-channel-udpgroupsettings-timedmetadataid3period"></a>
Timed Metadata interval in seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)