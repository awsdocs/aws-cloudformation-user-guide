# AWS::MediaLive::Channel M3u8Settings<a name="aws-properties-medialive-channel-m3u8settings"></a>

The settings information for the M3U8 container\.

The parent of this entity is StandardHlsSettings\.

## Syntax<a name="aws-properties-medialive-channel-m3u8settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-m3u8settings-syntax.json"></a>

```
{
  "[AudioFramesPerPes](#cfn-medialive-channel-m3u8settings-audioframesperpes)" : Integer,
  "[AudioPids](#cfn-medialive-channel-m3u8settings-audiopids)" : String,
  "[EcmPid](#cfn-medialive-channel-m3u8settings-ecmpid)" : String,
  "[NielsenId3Behavior](#cfn-medialive-channel-m3u8settings-nielsenid3behavior)" : String,
  "[PatInterval](#cfn-medialive-channel-m3u8settings-patinterval)" : Integer,
  "[PcrControl](#cfn-medialive-channel-m3u8settings-pcrcontrol)" : String,
  "[PcrPeriod](#cfn-medialive-channel-m3u8settings-pcrperiod)" : Integer,
  "[PcrPid](#cfn-medialive-channel-m3u8settings-pcrpid)" : String,
  "[PmtInterval](#cfn-medialive-channel-m3u8settings-pmtinterval)" : Integer,
  "[PmtPid](#cfn-medialive-channel-m3u8settings-pmtpid)" : String,
  "[ProgramNum](#cfn-medialive-channel-m3u8settings-programnum)" : Integer,
  "[Scte35Behavior](#cfn-medialive-channel-m3u8settings-scte35behavior)" : String,
  "[Scte35Pid](#cfn-medialive-channel-m3u8settings-scte35pid)" : String,
  "[TimedMetadataBehavior](#cfn-medialive-channel-m3u8settings-timedmetadatabehavior)" : String,
  "[TimedMetadataPid](#cfn-medialive-channel-m3u8settings-timedmetadatapid)" : String,
  "[TransportStreamId](#cfn-medialive-channel-m3u8settings-transportstreamid)" : Integer,
  "[VideoPid](#cfn-medialive-channel-m3u8settings-videopid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-m3u8settings-syntax.yaml"></a>

```
  [AudioFramesPerPes](#cfn-medialive-channel-m3u8settings-audioframesperpes): Integer
  [AudioPids](#cfn-medialive-channel-m3u8settings-audiopids): String
  [EcmPid](#cfn-medialive-channel-m3u8settings-ecmpid): String
  [NielsenId3Behavior](#cfn-medialive-channel-m3u8settings-nielsenid3behavior): String
  [PatInterval](#cfn-medialive-channel-m3u8settings-patinterval): Integer
  [PcrControl](#cfn-medialive-channel-m3u8settings-pcrcontrol): String
  [PcrPeriod](#cfn-medialive-channel-m3u8settings-pcrperiod): Integer
  [PcrPid](#cfn-medialive-channel-m3u8settings-pcrpid): String
  [PmtInterval](#cfn-medialive-channel-m3u8settings-pmtinterval): Integer
  [PmtPid](#cfn-medialive-channel-m3u8settings-pmtpid): String
  [ProgramNum](#cfn-medialive-channel-m3u8settings-programnum): Integer
  [Scte35Behavior](#cfn-medialive-channel-m3u8settings-scte35behavior): String
  [Scte35Pid](#cfn-medialive-channel-m3u8settings-scte35pid): String
  [TimedMetadataBehavior](#cfn-medialive-channel-m3u8settings-timedmetadatabehavior): String
  [TimedMetadataPid](#cfn-medialive-channel-m3u8settings-timedmetadatapid): String
  [TransportStreamId](#cfn-medialive-channel-m3u8settings-transportstreamid): Integer
  [VideoPid](#cfn-medialive-channel-m3u8settings-videopid): String
```

## Properties<a name="aws-properties-medialive-channel-m3u8settings-properties"></a>

`AudioFramesPerPes`  <a name="cfn-medialive-channel-m3u8settings-audioframesperpes"></a>
The number of audio frames to insert for each PES packet\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioPids`  <a name="cfn-medialive-channel-m3u8settings-audiopids"></a>
The PID of the elementary audio streams in the transport stream\. Multiple values are accepted, and can be entered in ranges or by comma separation\. You can enter the value as a decimal or hexadecimal value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcmPid`  <a name="cfn-medialive-channel-m3u8settings-ecmpid"></a>
This parameter is unused and deprecated\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenId3Behavior`  <a name="cfn-medialive-channel-m3u8settings-nielsenid3behavior"></a>
If set to passthrough, Nielsen inaudible tones for media tracking will be detected in the input audio and an equivalent ID3 tag will be inserted in the output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatInterval`  <a name="cfn-medialive-channel-m3u8settings-patinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\. A value of \\"0\\" writes out the PMT once per segment file\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrControl`  <a name="cfn-medialive-channel-m3u8settings-pcrcontrol"></a>
When set to pcrEveryPesPacket, a Program Clock Reference value is inserted for every Packetized Elementary Stream \(PES\) header\. This parameter is effective only when the PCR PID is the same as the video or audio elementary stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrPeriod`  <a name="cfn-medialive-channel-m3u8settings-pcrperiod"></a>
The maximum time, in milliseconds, between Program Clock References \(PCRs\) inserted into the transport stream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrPid`  <a name="cfn-medialive-channel-m3u8settings-pcrpid"></a>
The PID of the Program Clock Reference \(PCR\) in the transport stream\. When no value is given, MediaLive assigns the same value as the video PID\. You can enter the value as a decimal or hexadecimal value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PmtInterval`  <a name="cfn-medialive-channel-m3u8settings-pmtinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\. A value of \\"0\\" writes out the PMT once per segment file\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PmtPid`  <a name="cfn-medialive-channel-m3u8settings-pmtpid"></a>
The PID for the Program Map Table \(PMT\) in the transport stream\. You can enter the value as a decimal or hexadecimal value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramNum`  <a name="cfn-medialive-channel-m3u8settings-programnum"></a>
The value of the program number field in the Program Map Table \(PMT\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35Behavior`  <a name="cfn-medialive-channel-m3u8settings-scte35behavior"></a>
If set to passthrough, passes any SCTE\-35 signals from the input source to this output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35Pid`  <a name="cfn-medialive-channel-m3u8settings-scte35pid"></a>
The PID of the SCTE\-35 stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataBehavior`  <a name="cfn-medialive-channel-m3u8settings-timedmetadatabehavior"></a>
When set to passthrough, timed metadata is passed through from input to output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataPid`  <a name="cfn-medialive-channel-m3u8settings-timedmetadatapid"></a>
The PID of the timed metadata stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransportStreamId`  <a name="cfn-medialive-channel-m3u8settings-transportstreamid"></a>
The value of the transport stream ID field in the Program Map Table \(PMT\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoPid`  <a name="cfn-medialive-channel-m3u8settings-videopid"></a>
The PID of the elementary video stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)