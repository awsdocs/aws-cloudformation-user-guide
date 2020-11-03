# AWS::MediaPackage::OriginEndpoint HlsPackage<a name="aws-properties-mediapackage-originendpoint-hlspackage"></a>

Parameters for Apple HLS packaging\.

## Syntax<a name="aws-properties-mediapackage-originendpoint-hlspackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-hlspackage-syntax.json"></a>

```
{
  "[AdMarkers](#cfn-mediapackage-originendpoint-hlspackage-admarkers)" : String,
  "[AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-hlspackage-adsondeliveryrestrictions)" : String,
  "[AdTriggers](#cfn-mediapackage-originendpoint-hlspackage-adtriggers)" : [ String, ... ],
  "[Encryption](#cfn-mediapackage-originendpoint-hlspackage-encryption)" : HlsEncryption,
  "[IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-hlspackage-includeiframeonlystream)" : Boolean,
  "[PlaylistType](#cfn-mediapackage-originendpoint-hlspackage-playlisttype)" : String,
  "[PlaylistWindowSeconds](#cfn-mediapackage-originendpoint-hlspackage-playlistwindowseconds)" : Integer,
  "[ProgramDateTimeIntervalSeconds](#cfn-mediapackage-originendpoint-hlspackage-programdatetimeintervalseconds)" : Integer,
  "[SegmentDurationSeconds](#cfn-mediapackage-originendpoint-hlspackage-segmentdurationseconds)" : Integer,
  "[StreamSelection](#cfn-mediapackage-originendpoint-hlspackage-streamselection)" : StreamSelection,
  "[UseAudioRenditionGroup](#cfn-mediapackage-originendpoint-hlspackage-useaudiorenditiongroup)" : Boolean
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-hlspackage-syntax.yaml"></a>

```
  [AdMarkers](#cfn-mediapackage-originendpoint-hlspackage-admarkers): String
  [AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-hlspackage-adsondeliveryrestrictions): String
  [AdTriggers](#cfn-mediapackage-originendpoint-hlspackage-adtriggers): 
    - String
  [Encryption](#cfn-mediapackage-originendpoint-hlspackage-encryption): 
    HlsEncryption
  [IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-hlspackage-includeiframeonlystream): Boolean
  [PlaylistType](#cfn-mediapackage-originendpoint-hlspackage-playlisttype): String
  [PlaylistWindowSeconds](#cfn-mediapackage-originendpoint-hlspackage-playlistwindowseconds): Integer
  [ProgramDateTimeIntervalSeconds](#cfn-mediapackage-originendpoint-hlspackage-programdatetimeintervalseconds): Integer
  [SegmentDurationSeconds](#cfn-mediapackage-originendpoint-hlspackage-segmentdurationseconds): Integer
  [StreamSelection](#cfn-mediapackage-originendpoint-hlspackage-streamselection): 
    StreamSelection
  [UseAudioRenditionGroup](#cfn-mediapackage-originendpoint-hlspackage-useaudiorenditiongroup): Boolean
```

## Properties<a name="aws-properties-mediapackage-originendpoint-hlspackage-properties"></a>

`AdMarkers`  <a name="cfn-mediapackage-originendpoint-hlspackage-admarkers"></a>
Controls how ad markers are included in the packaged endpoint\. Valid values are `none`, `passthrough`, or `scte35_enhanced`\.  
+  **NONE** \- omits all SCTE\-35 ad markers from the output\.
+  **PASSTHROUGH** \- creates a copy in the output of the SCTE\-35 ad markers \(comments\) taken directly from the input manifest\.
+  **SCTE35\_ENHANCED** \- generates ad markers and blackout tags in the output based on the SCTE\-35 messages from the input manifest\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdsOnDeliveryRestrictions`  <a name="cfn-mediapackage-originendpoint-hlspackage-adsondeliveryrestrictions"></a>
The flags on SCTE\-35 segmentation descriptors that have to be present for MediaPackage to insert ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdTriggers`  <a name="cfn-mediapackage-originendpoint-hlspackage-adtriggers"></a>
The SCTE\-35 message types that MediaPackage treats as ad markers in the output manifest\.   
 Valid values:   
+  **BREAK**
+  **DISTRIBUTOR\_ADVERTISEMENT**
+  **DISTRIBUTOR\_OVERLAY\_PLACEMENT\_OPPORTUNITY**
+  **DISTRIBUTOR\_PLACEMENT\_OPPORTUNITY**
+  **PROVIDER\_ADVERTISEMENT**
+  **PROVIDER\_OVERLAY\_PLACEMENT\_OPPORTUNITY**
+  **PROVIDER\_PLACEMENT\_OPPORTUNITY**
+  **SPLICE\_INSERT**
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encryption`  <a name="cfn-mediapackage-originendpoint-hlspackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [HlsEncryption](aws-properties-mediapackage-originendpoint-hlsencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStream`  <a name="cfn-mediapackage-originendpoint-hlspackage-includeiframeonlystream"></a>
Only applies to stream sets with a single video track\. When true, the stream set includes an additional I\-frame only stream, along with the other tracks\. If false, this extra stream is not included\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaylistType`  <a name="cfn-mediapackage-originendpoint-hlspackage-playlisttype"></a>
When specified as either `event` or `vod`, a corresponding `EXT-X-PLAYLIST-TYPE` entry is included in the media playlist\. Indicates if the playlist is live\-to\-VOD content\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaylistWindowSeconds`  <a name="cfn-mediapackage-originendpoint-hlspackage-playlistwindowseconds"></a>
Time window \(in seconds\) contained in each parent manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimeIntervalSeconds`  <a name="cfn-mediapackage-originendpoint-hlspackage-programdatetimeintervalseconds"></a>
Inserts `EXT-X-PROGRAM-DATE-TIME` tags in the output manifest at the interval that you specify\. Additionally, ID3Timed metadata messages are generated every 5 seconds starting when the content was ingested\.  
Irrespective of this parameter, if any ID3Timed metadata is in the HLS input, it is passed through to the HLS output\.  
Omit this attribute or enter `0` to indicate that the `EXT-X-PROGRAM-DATE-TIME` tags are not included in the manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-originendpoint-hlspackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each fragment\. Actual fragments are rounded to the nearest multiple of the source fragment duration\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamSelection`  <a name="cfn-mediapackage-originendpoint-hlspackage-streamselection"></a>
Limitations for outputs from the endpoint, based on the video bitrate\.  
*Required*: No  
*Type*: [StreamSelection](aws-properties-mediapackage-originendpoint-streamselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseAudioRenditionGroup`  <a name="cfn-mediapackage-originendpoint-hlspackage-useaudiorenditiongroup"></a>
When true, AWS Elemental MediaPackage bundles all audio tracks in a rendition group\. All other tracks in the stream can be used with any audio rendition from the group\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)