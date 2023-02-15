# AWS::MediaLive::Channel MsSmoothGroupSettings<a name="aws-properties-medialive-channel-mssmoothgroupsettings"></a>

The settings for a Microsoft Smooth output group\.

The parent of this entity is OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-mssmoothgroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mssmoothgroupsettings-syntax.json"></a>

```
{
  "[AcquisitionPointId](#cfn-medialive-channel-mssmoothgroupsettings-acquisitionpointid)" : String,
  "[AudioOnlyTimecodeControl](#cfn-medialive-channel-mssmoothgroupsettings-audioonlytimecodecontrol)" : String,
  "[CertificateMode](#cfn-medialive-channel-mssmoothgroupsettings-certificatemode)" : String,
  "[ConnectionRetryInterval](#cfn-medialive-channel-mssmoothgroupsettings-connectionretryinterval)" : Integer,
  "[Destination](#cfn-medialive-channel-mssmoothgroupsettings-destination)" : OutputLocationRef,
  "[EventId](#cfn-medialive-channel-mssmoothgroupsettings-eventid)" : String,
  "[EventIdMode](#cfn-medialive-channel-mssmoothgroupsettings-eventidmode)" : String,
  "[EventStopBehavior](#cfn-medialive-channel-mssmoothgroupsettings-eventstopbehavior)" : String,
  "[FilecacheDuration](#cfn-medialive-channel-mssmoothgroupsettings-filecacheduration)" : Integer,
  "[FragmentLength](#cfn-medialive-channel-mssmoothgroupsettings-fragmentlength)" : Integer,
  "[InputLossAction](#cfn-medialive-channel-mssmoothgroupsettings-inputlossaction)" : String,
  "[NumRetries](#cfn-medialive-channel-mssmoothgroupsettings-numretries)" : Integer,
  "[RestartDelay](#cfn-medialive-channel-mssmoothgroupsettings-restartdelay)" : Integer,
  "[SegmentationMode](#cfn-medialive-channel-mssmoothgroupsettings-segmentationmode)" : String,
  "[SendDelayMs](#cfn-medialive-channel-mssmoothgroupsettings-senddelayms)" : Integer,
  "[SparseTrackType](#cfn-medialive-channel-mssmoothgroupsettings-sparsetracktype)" : String,
  "[StreamManifestBehavior](#cfn-medialive-channel-mssmoothgroupsettings-streammanifestbehavior)" : String,
  "[TimestampOffset](#cfn-medialive-channel-mssmoothgroupsettings-timestampoffset)" : String,
  "[TimestampOffsetMode](#cfn-medialive-channel-mssmoothgroupsettings-timestampoffsetmode)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-mssmoothgroupsettings-syntax.yaml"></a>

```
  [AcquisitionPointId](#cfn-medialive-channel-mssmoothgroupsettings-acquisitionpointid): String
  [AudioOnlyTimecodeControl](#cfn-medialive-channel-mssmoothgroupsettings-audioonlytimecodecontrol): String
  [CertificateMode](#cfn-medialive-channel-mssmoothgroupsettings-certificatemode): String
  [ConnectionRetryInterval](#cfn-medialive-channel-mssmoothgroupsettings-connectionretryinterval): Integer
  [Destination](#cfn-medialive-channel-mssmoothgroupsettings-destination): 
    OutputLocationRef
  [EventId](#cfn-medialive-channel-mssmoothgroupsettings-eventid): String
  [EventIdMode](#cfn-medialive-channel-mssmoothgroupsettings-eventidmode): String
  [EventStopBehavior](#cfn-medialive-channel-mssmoothgroupsettings-eventstopbehavior): String
  [FilecacheDuration](#cfn-medialive-channel-mssmoothgroupsettings-filecacheduration): Integer
  [FragmentLength](#cfn-medialive-channel-mssmoothgroupsettings-fragmentlength): Integer
  [InputLossAction](#cfn-medialive-channel-mssmoothgroupsettings-inputlossaction): String
  [NumRetries](#cfn-medialive-channel-mssmoothgroupsettings-numretries): Integer
  [RestartDelay](#cfn-medialive-channel-mssmoothgroupsettings-restartdelay): Integer
  [SegmentationMode](#cfn-medialive-channel-mssmoothgroupsettings-segmentationmode): String
  [SendDelayMs](#cfn-medialive-channel-mssmoothgroupsettings-senddelayms): Integer
  [SparseTrackType](#cfn-medialive-channel-mssmoothgroupsettings-sparsetracktype): String
  [StreamManifestBehavior](#cfn-medialive-channel-mssmoothgroupsettings-streammanifestbehavior): String
  [TimestampOffset](#cfn-medialive-channel-mssmoothgroupsettings-timestampoffset): String
  [TimestampOffsetMode](#cfn-medialive-channel-mssmoothgroupsettings-timestampoffsetmode): String
```

## Properties<a name="aws-properties-medialive-channel-mssmoothgroupsettings-properties"></a>

`AcquisitionPointId`  <a name="cfn-medialive-channel-mssmoothgroupsettings-acquisitionpointid"></a>
The value of the Acquisition Point Identity element that is used in each message placed in the sparse track\. Enabled only if sparseTrackType is not "none\."  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioOnlyTimecodeControl`  <a name="cfn-medialive-channel-mssmoothgroupsettings-audioonlytimecodecontrol"></a>
If set to passthrough for an audio\-only Microsoft Smooth output, the fragment absolute time is set to the current timecode\. This option does not write timecodes to the audio elementary stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertificateMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-certificatemode"></a>
If set to verifyAuthenticity, verifies the HTTPS certificate chain to a trusted certificate authority \(CA\)\. This causes HTTPS outputs to self\-signed certificates to fail\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-mssmoothgroupsettings-connectionretryinterval"></a>
The number of seconds to wait before retrying the connection to the IIS server if the connection is lost\. Content is cached during this time, and the cache is delivered to the IIS server after the connection is re\-established\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-mssmoothgroupsettings-destination"></a>
The Smooth Streaming publish point on an IIS server\. MediaLive acts as a "Push" encoder to IIS\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventId`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventid"></a>
The Microsoft Smooth channel ID that is sent to the IIS server\. Specify the ID only if eventIdMode is set to useConfigured\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventIdMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventidmode"></a>
Specifies whether to send a channel ID to the IIS server\. If no channel ID is sent and the same channel is used without changing the publishing point, clients might see cached video from the previous run\. Options: \- "useConfigured" \- use the value provided in eventId \- "useTimestamp" \- generate and send a channel ID based on the current timestamp \- "noEventId" \- do not send a channel ID to the IIS server\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventStopBehavior`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventstopbehavior"></a>
When set to sendEos, sends an EOS signal to an IIS server when stopping the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-mssmoothgroupsettings-filecacheduration"></a>
The size, in seconds, of the file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FragmentLength`  <a name="cfn-medialive-channel-mssmoothgroupsettings-fragmentlength"></a>
The length, in seconds, of mp4 fragments to generate\. The fragment length must be compatible with GOP size and frame rate\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossAction`  <a name="cfn-medialive-channel-mssmoothgroupsettings-inputlossaction"></a>
A parameter that controls output group behavior on an input loss\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-mssmoothgroupsettings-numretries"></a>
The number of retry attempts\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-mssmoothgroupsettings-restartdelay"></a>
The number of seconds before initiating a restart due to output failure, due to exhausting the numRetries on one segment, or exceeding filecacheDuration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-segmentationmode"></a>
useInputSegmentation has been deprecated\. The configured segment size is always used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SendDelayMs`  <a name="cfn-medialive-channel-mssmoothgroupsettings-senddelayms"></a>
The number of milliseconds to delay the output from the second pipeline\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SparseTrackType`  <a name="cfn-medialive-channel-mssmoothgroupsettings-sparsetracktype"></a>
If set to scte35, uses incoming SCTE\-35 messages to generate a sparse track in this group of Microsoft Smooth outputs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamManifestBehavior`  <a name="cfn-medialive-channel-mssmoothgroupsettings-streammanifestbehavior"></a>
When set to send, sends a stream manifest so that the publishing point doesn't start until all streams start\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampOffset`  <a name="cfn-medialive-channel-mssmoothgroupsettings-timestampoffset"></a>
The timestamp offset for the channel\. Used only if timestampOffsetMode is set to useConfiguredOffset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampOffsetMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-timestampoffsetmode"></a>
The type of timestamp date offset to use\. \- useEventStartDate: Use the date the channel was started as the offset \- useConfiguredOffset: Use an explicitly configured date as the offset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)