# AWS::MediaLive::Channel MsSmoothGroupSettings<a name="aws-properties-medialive-channel-mssmoothgroupsettings"></a>

Ms Smooth Group Settings

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
The ID to include in each message in the sparse track\. Ignored if sparseTrackType is NONE\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioOnlyTimecodeControl`  <a name="cfn-medialive-channel-mssmoothgroupsettings-audioonlytimecodecontrol"></a>
If set to passthrough for an audio\-only MS Smooth output, the fragment absolute time will be set to the current timecode\. This option does not write timecodes to the audio elementary stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CertificateMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-certificatemode"></a>
If set to verifyAuthenticity, verify the https certificate chain to a trusted Certificate Authority \(CA\)\. This will cause https outputs to self\-signed certificates to fail\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-mssmoothgroupsettings-connectionretryinterval"></a>
Number of seconds to wait before retrying connection to the IIS server if the connection is lost\. Content will be cached during this time and the cache will be be delivered to the IIS server once the connection is re\-established\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-mssmoothgroupsettings-destination"></a>
Smooth Streaming publish point on an IIS server\. MediaLive acts as a "Push" encoder to IIS\.   
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventId`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventid"></a>
MS Smooth event ID to be sent to the IIS server\. Should only be specified if eventIdMode is set to useConfigured\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventIdMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventidmode"></a>
Specifies whether or not to send an event ID to the IIS server\. If no event ID is sent and the same MediaLive channel is used again without changing the publishing point, clients might see cached video from the previous run\. Options: \- "useConfigured" \- use the value provided in eventId \- "useTimestamp" \- generate and send an event ID based on the current timestamp \- "noEventId" \- do not send an event ID to the IIS server\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventStopBehavior`  <a name="cfn-medialive-channel-mssmoothgroupsettings-eventstopbehavior"></a>
When set to sendEos, send EOS signal to IIS server when stopping the channel\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-mssmoothgroupsettings-filecacheduration"></a>
Size in seconds of file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FragmentLength`  <a name="cfn-medialive-channel-mssmoothgroupsettings-fragmentlength"></a>
Length of mp4 fragments to generate \(in seconds\)\. Fragment length must be compatible with GOP size and framerate\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossAction`  <a name="cfn-medialive-channel-mssmoothgroupsettings-inputlossaction"></a>
Parameter that control output group behavior on input loss\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-mssmoothgroupsettings-numretries"></a>
Number of retry attempts\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-mssmoothgroupsettings-restartdelay"></a>
Number of seconds before initiating a restart due to output failure, due to exhausting the numRetries on one segment, or exceeding filecacheDuration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-segmentationmode"></a>
useInputSegmentation has been deprecated\. The configured segment size is always used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SendDelayMs`  <a name="cfn-medialive-channel-mssmoothgroupsettings-senddelayms"></a>
Number of milliseconds to delay the output from the second pipeline\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SparseTrackType`  <a name="cfn-medialive-channel-mssmoothgroupsettings-sparsetracktype"></a>
Identifies the type of data to place in the sparse track: \- SCTE35: Insert SCTE\-35 messages from the source content\. With each message, insert an IDR frame to start a new segment\. \- SCTE35\_WITHOUT\_SEGMENTATION: Insert SCTE\-35 messages from the source content\. With each message, insert an IDR frame but don't start a new segment\. \- NONE: Don't generate a sparse track for any outputs in this output group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamManifestBehavior`  <a name="cfn-medialive-channel-mssmoothgroupsettings-streammanifestbehavior"></a>
When set to send, send stream manifest so publishing point doesn't start until all streams start\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampOffset`  <a name="cfn-medialive-channel-mssmoothgroupsettings-timestampoffset"></a>
Timestamp offset for the channel\. Only used if timestampOffsetMode is set to useConfiguredOffset\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampOffsetMode`  <a name="cfn-medialive-channel-mssmoothgroupsettings-timestampoffsetmode"></a>
Type of timestamp date offset to use\. \- useEventStartDate: Use the date the channel was started as the offset \- useConfiguredOffset: Use an explicitly configured date as the offset\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)