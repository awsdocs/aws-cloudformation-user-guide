# AWS::MediaLive::Channel M2tsSettings<a name="aws-properties-medialive-channel-m2tssettings"></a>

The configuration of the M2TS in the UDP output\.

The parent of this entity is UdpContainerSettings\.

## Syntax<a name="aws-properties-medialive-channel-m2tssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-m2tssettings-syntax.json"></a>

```
{
  "[AbsentInputAudioBehavior](#cfn-medialive-channel-m2tssettings-absentinputaudiobehavior)" : String,
  "[Arib](#cfn-medialive-channel-m2tssettings-arib)" : String,
  "[AribCaptionsPid](#cfn-medialive-channel-m2tssettings-aribcaptionspid)" : String,
  "[AribCaptionsPidControl](#cfn-medialive-channel-m2tssettings-aribcaptionspidcontrol)" : String,
  "[AudioBufferModel](#cfn-medialive-channel-m2tssettings-audiobuffermodel)" : String,
  "[AudioFramesPerPes](#cfn-medialive-channel-m2tssettings-audioframesperpes)" : Integer,
  "[AudioPids](#cfn-medialive-channel-m2tssettings-audiopids)" : String,
  "[AudioStreamType](#cfn-medialive-channel-m2tssettings-audiostreamtype)" : String,
  "[Bitrate](#cfn-medialive-channel-m2tssettings-bitrate)" : Integer,
  "[BufferModel](#cfn-medialive-channel-m2tssettings-buffermodel)" : String,
  "[CcDescriptor](#cfn-medialive-channel-m2tssettings-ccdescriptor)" : String,
  "[DvbNitSettings](#cfn-medialive-channel-m2tssettings-dvbnitsettings)" : DvbNitSettings,
  "[DvbSdtSettings](#cfn-medialive-channel-m2tssettings-dvbsdtsettings)" : DvbSdtSettings,
  "[DvbSubPids](#cfn-medialive-channel-m2tssettings-dvbsubpids)" : String,
  "[DvbTdtSettings](#cfn-medialive-channel-m2tssettings-dvbtdtsettings)" : DvbTdtSettings,
  "[DvbTeletextPid](#cfn-medialive-channel-m2tssettings-dvbteletextpid)" : String,
  "[Ebif](#cfn-medialive-channel-m2tssettings-ebif)" : String,
  "[EbpAudioInterval](#cfn-medialive-channel-m2tssettings-ebpaudiointerval)" : String,
  "[EbpLookaheadMs](#cfn-medialive-channel-m2tssettings-ebplookaheadms)" : Integer,
  "[EbpPlacement](#cfn-medialive-channel-m2tssettings-ebpplacement)" : String,
  "[EcmPid](#cfn-medialive-channel-m2tssettings-ecmpid)" : String,
  "[EsRateInPes](#cfn-medialive-channel-m2tssettings-esrateinpes)" : String,
  "[EtvPlatformPid](#cfn-medialive-channel-m2tssettings-etvplatformpid)" : String,
  "[EtvSignalPid](#cfn-medialive-channel-m2tssettings-etvsignalpid)" : String,
  "[FragmentTime](#cfn-medialive-channel-m2tssettings-fragmenttime)" : Double,
  "[Klv](#cfn-medialive-channel-m2tssettings-klv)" : String,
  "[KlvDataPids](#cfn-medialive-channel-m2tssettings-klvdatapids)" : String,
  "[NielsenId3Behavior](#cfn-medialive-channel-m2tssettings-nielsenid3behavior)" : String,
  "[NullPacketBitrate](#cfn-medialive-channel-m2tssettings-nullpacketbitrate)" : Double,
  "[PatInterval](#cfn-medialive-channel-m2tssettings-patinterval)" : Integer,
  "[PcrControl](#cfn-medialive-channel-m2tssettings-pcrcontrol)" : String,
  "[PcrPeriod](#cfn-medialive-channel-m2tssettings-pcrperiod)" : Integer,
  "[PcrPid](#cfn-medialive-channel-m2tssettings-pcrpid)" : String,
  "[PmtInterval](#cfn-medialive-channel-m2tssettings-pmtinterval)" : Integer,
  "[PmtPid](#cfn-medialive-channel-m2tssettings-pmtpid)" : String,
  "[ProgramNum](#cfn-medialive-channel-m2tssettings-programnum)" : Integer,
  "[RateMode](#cfn-medialive-channel-m2tssettings-ratemode)" : String,
  "[Scte27Pids](#cfn-medialive-channel-m2tssettings-scte27pids)" : String,
  "[Scte35Control](#cfn-medialive-channel-m2tssettings-scte35control)" : String,
  "[Scte35Pid](#cfn-medialive-channel-m2tssettings-scte35pid)" : String,
  "[SegmentationMarkers](#cfn-medialive-channel-m2tssettings-segmentationmarkers)" : String,
  "[SegmentationStyle](#cfn-medialive-channel-m2tssettings-segmentationstyle)" : String,
  "[SegmentationTime](#cfn-medialive-channel-m2tssettings-segmentationtime)" : Double,
  "[TimedMetadataBehavior](#cfn-medialive-channel-m2tssettings-timedmetadatabehavior)" : String,
  "[TimedMetadataPid](#cfn-medialive-channel-m2tssettings-timedmetadatapid)" : String,
  "[TransportStreamId](#cfn-medialive-channel-m2tssettings-transportstreamid)" : Integer,
  "[VideoPid](#cfn-medialive-channel-m2tssettings-videopid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-m2tssettings-syntax.yaml"></a>

```
  [AbsentInputAudioBehavior](#cfn-medialive-channel-m2tssettings-absentinputaudiobehavior): String
  [Arib](#cfn-medialive-channel-m2tssettings-arib): String
  [AribCaptionsPid](#cfn-medialive-channel-m2tssettings-aribcaptionspid): String
  [AribCaptionsPidControl](#cfn-medialive-channel-m2tssettings-aribcaptionspidcontrol): String
  [AudioBufferModel](#cfn-medialive-channel-m2tssettings-audiobuffermodel): String
  [AudioFramesPerPes](#cfn-medialive-channel-m2tssettings-audioframesperpes): Integer
  [AudioPids](#cfn-medialive-channel-m2tssettings-audiopids): String
  [AudioStreamType](#cfn-medialive-channel-m2tssettings-audiostreamtype): String
  [Bitrate](#cfn-medialive-channel-m2tssettings-bitrate): Integer
  [BufferModel](#cfn-medialive-channel-m2tssettings-buffermodel): String
  [CcDescriptor](#cfn-medialive-channel-m2tssettings-ccdescriptor): String
  [DvbNitSettings](#cfn-medialive-channel-m2tssettings-dvbnitsettings): 
    DvbNitSettings
  [DvbSdtSettings](#cfn-medialive-channel-m2tssettings-dvbsdtsettings): 
    DvbSdtSettings
  [DvbSubPids](#cfn-medialive-channel-m2tssettings-dvbsubpids): String
  [DvbTdtSettings](#cfn-medialive-channel-m2tssettings-dvbtdtsettings): 
    DvbTdtSettings
  [DvbTeletextPid](#cfn-medialive-channel-m2tssettings-dvbteletextpid): String
  [Ebif](#cfn-medialive-channel-m2tssettings-ebif): String
  [EbpAudioInterval](#cfn-medialive-channel-m2tssettings-ebpaudiointerval): String
  [EbpLookaheadMs](#cfn-medialive-channel-m2tssettings-ebplookaheadms): Integer
  [EbpPlacement](#cfn-medialive-channel-m2tssettings-ebpplacement): String
  [EcmPid](#cfn-medialive-channel-m2tssettings-ecmpid): String
  [EsRateInPes](#cfn-medialive-channel-m2tssettings-esrateinpes): String
  [EtvPlatformPid](#cfn-medialive-channel-m2tssettings-etvplatformpid): String
  [EtvSignalPid](#cfn-medialive-channel-m2tssettings-etvsignalpid): String
  [FragmentTime](#cfn-medialive-channel-m2tssettings-fragmenttime): Double
  [Klv](#cfn-medialive-channel-m2tssettings-klv): String
  [KlvDataPids](#cfn-medialive-channel-m2tssettings-klvdatapids): String
  [NielsenId3Behavior](#cfn-medialive-channel-m2tssettings-nielsenid3behavior): String
  [NullPacketBitrate](#cfn-medialive-channel-m2tssettings-nullpacketbitrate): Double
  [PatInterval](#cfn-medialive-channel-m2tssettings-patinterval): Integer
  [PcrControl](#cfn-medialive-channel-m2tssettings-pcrcontrol): String
  [PcrPeriod](#cfn-medialive-channel-m2tssettings-pcrperiod): Integer
  [PcrPid](#cfn-medialive-channel-m2tssettings-pcrpid): String
  [PmtInterval](#cfn-medialive-channel-m2tssettings-pmtinterval): Integer
  [PmtPid](#cfn-medialive-channel-m2tssettings-pmtpid): String
  [ProgramNum](#cfn-medialive-channel-m2tssettings-programnum): Integer
  [RateMode](#cfn-medialive-channel-m2tssettings-ratemode): String
  [Scte27Pids](#cfn-medialive-channel-m2tssettings-scte27pids): String
  [Scte35Control](#cfn-medialive-channel-m2tssettings-scte35control): String
  [Scte35Pid](#cfn-medialive-channel-m2tssettings-scte35pid): String
  [SegmentationMarkers](#cfn-medialive-channel-m2tssettings-segmentationmarkers): String
  [SegmentationStyle](#cfn-medialive-channel-m2tssettings-segmentationstyle): String
  [SegmentationTime](#cfn-medialive-channel-m2tssettings-segmentationtime): Double
  [TimedMetadataBehavior](#cfn-medialive-channel-m2tssettings-timedmetadatabehavior): String
  [TimedMetadataPid](#cfn-medialive-channel-m2tssettings-timedmetadatapid): String
  [TransportStreamId](#cfn-medialive-channel-m2tssettings-transportstreamid): Integer
  [VideoPid](#cfn-medialive-channel-m2tssettings-videopid): String
```

## Properties<a name="aws-properties-medialive-channel-m2tssettings-properties"></a>

`AbsentInputAudioBehavior`  <a name="cfn-medialive-channel-m2tssettings-absentinputaudiobehavior"></a>
When set to drop, the output audio streams are removed from the program if the selected input audio stream is removed from the input\. This allows the output audio configuration to dynamically change based on the input configuration\. If this is set to encodeSilence, all output audio streams will output encoded silence when not connected to an active input stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Arib`  <a name="cfn-medialive-channel-m2tssettings-arib"></a>
When set to enabled, uses ARIB\-compliant field muxing and removes video descriptor\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AribCaptionsPid`  <a name="cfn-medialive-channel-m2tssettings-aribcaptionspid"></a>
The PID for ARIB Captions in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AribCaptionsPidControl`  <a name="cfn-medialive-channel-m2tssettings-aribcaptionspidcontrol"></a>
If set to auto, The PID number used for ARIB Captions will be auto\-selected from unused PIDs\. If set to useConfigured, ARIB captions will be on the configured PID number\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioBufferModel`  <a name="cfn-medialive-channel-m2tssettings-audiobuffermodel"></a>
When set to dvb, uses the DVB buffer model for Dolby Digital audio\. When set to atsc, the ATSC model is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioFramesPerPes`  <a name="cfn-medialive-channel-m2tssettings-audioframesperpes"></a>
The number of audio frames to insert for each PES packet\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioPids`  <a name="cfn-medialive-channel-m2tssettings-audiopids"></a>
The PID of the elementary audio streams in the transport stream\. Multiple values are accepted, and can be entered in ranges or by comma separation\. You can enter the value as a decimal or hexadecimal value\. Each PID specified must be in the range of 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioStreamType`  <a name="cfn-medialive-channel-m2tssettings-audiostreamtype"></a>
When set to atsc, uses stream type = 0x81 for AC3 and stream type = 0x87 for EAC3\. When set to dvb, uses stream type = 0x06\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bitrate`  <a name="cfn-medialive-channel-m2tssettings-bitrate"></a>
The output bitrate of the transport stream in bits per second\. Setting to 0 lets the muxer automatically determine the appropriate bitrate\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BufferModel`  <a name="cfn-medialive-channel-m2tssettings-buffermodel"></a>
If set to multiplex, uses the multiplex buffer model for accurate interleaving\. Setting to bufferModel to none can lead to lower latency, but low\-memory devices might not be able to play back the stream without interruptions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CcDescriptor`  <a name="cfn-medialive-channel-m2tssettings-ccdescriptor"></a>
When set to enabled, generates captionServiceDescriptor in PMT\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbNitSettings`  <a name="cfn-medialive-channel-m2tssettings-dvbnitsettings"></a>
Inserts a DVB Network Information Table \(NIT\) at the specified table repetition interval\.  
*Required*: No  
*Type*: [DvbNitSettings](aws-properties-medialive-channel-dvbnitsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbSdtSettings`  <a name="cfn-medialive-channel-m2tssettings-dvbsdtsettings"></a>
Inserts a DVB Service Description Table \(SDT\) at the specified table repetition interval\.  
*Required*: No  
*Type*: [DvbSdtSettings](aws-properties-medialive-channel-dvbsdtsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbSubPids`  <a name="cfn-medialive-channel-m2tssettings-dvbsubpids"></a>
The PID for the input source DVB Subtitle data to this output\. Multiple values are accepted, and can be entered in ranges and/or by comma separation\. You can enter the value as a decimal or hexadecimal value\. Each PID specified must be in the range of 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbTdtSettings`  <a name="cfn-medialive-channel-m2tssettings-dvbtdtsettings"></a>
Inserts DVB Time and Date Table \(TDT\) at the specified table repetition interval\.  
*Required*: No  
*Type*: [DvbTdtSettings](aws-properties-medialive-channel-dvbtdtsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DvbTeletextPid`  <a name="cfn-medialive-channel-m2tssettings-dvbteletextpid"></a>
The PID for the input source DVB Teletext data to this output\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebif`  <a name="cfn-medialive-channel-m2tssettings-ebif"></a>
If set to passthrough, passes any EBIF data from the input source to this output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbpAudioInterval`  <a name="cfn-medialive-channel-m2tssettings-ebpaudiointerval"></a>
When videoAndFixedIntervals is selected, audio EBP markers are added to partitions 3 and 4\. The interval between these additional markers is fixed, and is slightly shorter than the video EBP marker interval\. This is only available when EBP Cablelabs segmentation markers are selected\. Partitions 1 and 2 always follow the video interval\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbpLookaheadMs`  <a name="cfn-medialive-channel-m2tssettings-ebplookaheadms"></a>
When set, enforces that Encoder Boundary Points do not come within the specified time interval of each other by looking ahead at input video\. If another EBP is going to come in within the specified time interval, the current EBP is not emitted, and the segment is "stretched" to the next marker\. The lookahead value does not add latency to the system\. The channel must be configured elsewhere to create sufficient latency to make the lookahead accurate\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbpPlacement`  <a name="cfn-medialive-channel-m2tssettings-ebpplacement"></a>
Controls placement of EBP on audio PIDs\. If set to videoAndAudioPids, EBP markers are placed on the video PID and all audio PIDs\. If set to videoPid, EBP markers are placed on only the video PID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcmPid`  <a name="cfn-medialive-channel-m2tssettings-ecmpid"></a>
This field is unused and deprecated\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EsRateInPes`  <a name="cfn-medialive-channel-m2tssettings-esrateinpes"></a>
Includes or excludes the ES Rate field in the PES header\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EtvPlatformPid`  <a name="cfn-medialive-channel-m2tssettings-etvplatformpid"></a>
The PID for the input source ETV Platform data to this output\. You can enter it as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EtvSignalPid`  <a name="cfn-medialive-channel-m2tssettings-etvsignalpid"></a>
The PID for input source ETV Signal data to this output\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FragmentTime`  <a name="cfn-medialive-channel-m2tssettings-fragmenttime"></a>
The length in seconds of each fragment\. This is used only with EBP markers\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Klv`  <a name="cfn-medialive-channel-m2tssettings-klv"></a>
If set to passthrough, passes any KLV data from the input source to this output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KlvDataPids`  <a name="cfn-medialive-channel-m2tssettings-klvdatapids"></a>
The PID for the input source KLV data to this output\. Multiple values are accepted, and can be entered in ranges or by comma separation\. You can enter the value as a decimal or hexadecimal value\. Each PID specified must be in the range of 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenId3Behavior`  <a name="cfn-medialive-channel-m2tssettings-nielsenid3behavior"></a>
If set to passthrough, Nielsen inaudible tones for media tracking will be detected in the input audio and an equivalent ID3 tag will be inserted in the output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullPacketBitrate`  <a name="cfn-medialive-channel-m2tssettings-nullpacketbitrate"></a>
The value, in bits per second, of extra null packets to insert into the transport stream\. This can be used if a downstream encryption system requires periodic null packets\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatInterval`  <a name="cfn-medialive-channel-m2tssettings-patinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\. Valid values are 0, 10\.\.1000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrControl`  <a name="cfn-medialive-channel-m2tssettings-pcrcontrol"></a>
When set to pcrEveryPesPacket, a Program Clock Reference value is inserted for every Packetized Elementary Stream \(PES\) header\. This parameter is effective only when the PCR PID is the same as the video or audio elementary stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrPeriod`  <a name="cfn-medialive-channel-m2tssettings-pcrperiod"></a>
The maximum time, in milliseconds, between Program Clock References \(PCRs\) inserted into the transport stream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PcrPid`  <a name="cfn-medialive-channel-m2tssettings-pcrpid"></a>
The PID of the Program Clock Reference \(PCR\) in the transport stream\. When no value is given, MediaLive assigns the same value as the video PID\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PmtInterval`  <a name="cfn-medialive-channel-m2tssettings-pmtinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\. Valid values are 0, 10\.\.1000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PmtPid`  <a name="cfn-medialive-channel-m2tssettings-pmtpid"></a>
The PID for the Program Map Table \(PMT\) in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramNum`  <a name="cfn-medialive-channel-m2tssettings-programnum"></a>
The value of the program number field in the Program Map Table \(PMT\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateMode`  <a name="cfn-medialive-channel-m2tssettings-ratemode"></a>
When VBR, does not insert null packets into the transport stream to fill the specified bitrate\. The bitrate setting acts as the maximum bitrate when VBR is set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte27Pids`  <a name="cfn-medialive-channel-m2tssettings-scte27pids"></a>
The PID for the input source SCTE\-27 data to this output\. Multiple values are accepted, and can be entered in ranges or by comma separation\. You can enter the value as a decimal or hexadecimal value\. Each PID specified must be in the range of 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35Control`  <a name="cfn-medialive-channel-m2tssettings-scte35control"></a>
Optionally passes SCTE\-35 signals from the input source to this output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35Pid`  <a name="cfn-medialive-channel-m2tssettings-scte35pid"></a>
The PID of the SCTE\-35 stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationMarkers`  <a name="cfn-medialive-channel-m2tssettings-segmentationmarkers"></a>
Inserts segmentation markers at each segmentationTime period\. raiSegstart sets the Random Access Indicator bit in the adaptation field\. raiAdapt sets the RAI bit and adds the current timecode in the private data bytes\. psiSegstart inserts PAT and PMT tables at the start of segments\. ebp adds Encoder Boundary Point information to the adaptation field as per OpenCable specification OC\-SP\-EBP\-I01\-130118\. ebpLegacy adds Encoder Boundary Point information to the adaptation field using a legacy proprietary format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationStyle`  <a name="cfn-medialive-channel-m2tssettings-segmentationstyle"></a>
The segmentation style parameter controls how segmentation markers are inserted into the transport stream\. With avails, it is possible that segments might be truncated, which can influence where future segmentation markers are inserted\. When a segmentation style of resetCadence is selected and a segment is truncated due to an avail, we will reset the segmentation cadence\. This means the subsequent segment will have a duration of $segmentationTime seconds\. When a segmentation style of maintainCadence is selected and a segment is truncated due to an avail, we will not reset the segmentation cadence\. This means the subsequent segment will likely be truncated as well\. However, all segments after that will have a duration of $segmentationTime seconds\. Note that EBP lookahead is a slight exception to this rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationTime`  <a name="cfn-medialive-channel-m2tssettings-segmentationtime"></a>
The length, in seconds, of each segment\. This is required unless markers is set to None\_\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataBehavior`  <a name="cfn-medialive-channel-m2tssettings-timedmetadatabehavior"></a>
When set to passthrough, timed metadata is passed through from input to output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataPid`  <a name="cfn-medialive-channel-m2tssettings-timedmetadatapid"></a>
The PID of the timed metadata stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransportStreamId`  <a name="cfn-medialive-channel-m2tssettings-transportstreamid"></a>
The value of the transport stream ID field in the Program Map Table \(PMT\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoPid`  <a name="cfn-medialive-channel-m2tssettings-videopid"></a>
The PID of the elementary video stream in the transport stream\. You can enter the value as a decimal or hexadecimal value\. Valid values are 32 \(or 0x20\)\.\.8182 \(or 0x1ff6\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)