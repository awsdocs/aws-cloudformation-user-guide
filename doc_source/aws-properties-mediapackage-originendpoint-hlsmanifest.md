# AWS::MediaPackage::OriginEndpoint HlsManifest<a name="aws-properties-mediapackage-originendpoint-hlsmanifest"></a>

An HTTP Live Streaming \(HLS\) manifest configuration on a CMAF endpoint\.

## Syntax<a name="aws-properties-mediapackage-originendpoint-hlsmanifest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-hlsmanifest-syntax.json"></a>

```
{
  "[AdMarkers](#cfn-mediapackage-originendpoint-hlsmanifest-admarkers)" : String,
  "[AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-hlsmanifest-adsondeliveryrestrictions)" : String,
  "[AdTriggers](#cfn-mediapackage-originendpoint-hlsmanifest-adtriggers)" : [ String, ... ],
  "[Id](#cfn-mediapackage-originendpoint-hlsmanifest-id)" : String,
  "[IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-hlsmanifest-includeiframeonlystream)" : Boolean,
  "[ManifestName](#cfn-mediapackage-originendpoint-hlsmanifest-manifestname)" : String,
  "[PlaylistType](#cfn-mediapackage-originendpoint-hlsmanifest-playlisttype)" : String,
  "[PlaylistWindowSeconds](#cfn-mediapackage-originendpoint-hlsmanifest-playlistwindowseconds)" : Integer,
  "[ProgramDateTimeIntervalSeconds](#cfn-mediapackage-originendpoint-hlsmanifest-programdatetimeintervalseconds)" : Integer,
  "[Url](#cfn-mediapackage-originendpoint-hlsmanifest-url)" : String
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-hlsmanifest-syntax.yaml"></a>

```
  [AdMarkers](#cfn-mediapackage-originendpoint-hlsmanifest-admarkers): String
  [AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-hlsmanifest-adsondeliveryrestrictions): String
  [AdTriggers](#cfn-mediapackage-originendpoint-hlsmanifest-adtriggers): 
    - String
  [Id](#cfn-mediapackage-originendpoint-hlsmanifest-id): String
  [IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-hlsmanifest-includeiframeonlystream): Boolean
  [ManifestName](#cfn-mediapackage-originendpoint-hlsmanifest-manifestname): String
  [PlaylistType](#cfn-mediapackage-originendpoint-hlsmanifest-playlisttype): String
  [PlaylistWindowSeconds](#cfn-mediapackage-originendpoint-hlsmanifest-playlistwindowseconds): Integer
  [ProgramDateTimeIntervalSeconds](#cfn-mediapackage-originendpoint-hlsmanifest-programdatetimeintervalseconds): Integer
  [Url](#cfn-mediapackage-originendpoint-hlsmanifest-url): String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-hlsmanifest-properties"></a>

`AdMarkers`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-admarkers"></a>
Controls how ad markers are included in the packaged endpoint\. Valid values are `none`, `passthrough`, or `scte35_enhanced`\.  
+  **NONE** \- omits all SCTE\-35 ad markers from the output\.
+  **PASSTHROUGH** \- creates a copy in the output of the SCTE\-35 ad markers \(comments\) taken directly from the input manifest\.
+  **SCTE35\_ENHANCED** \- generates ad markers and blackout tags in the output based on the SCTE\-35 messages from the input manifest\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdsOnDeliveryRestrictions`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-adsondeliveryrestrictions"></a>
The flags on SCTE\-35 segmentation descriptors that have to be present for MediaPackage to insert ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdTriggers`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-adtriggers"></a>
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

`Id`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-id"></a>
The manifest ID is required and must be unique within the OriginEndpoint\. The ID can't be changed after the endpoint is created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStream`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-includeiframeonlystream"></a>
Applies to stream sets with a single video track only\. When true, the stream set includes an additional I\-frame only stream, along with the other tracks\. If false, this extra stream is not included\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestName`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-manifestname"></a>
A short string that's appended to the end of the endpoint URL to create a unique path to this endpoint\. The manifestName on the HLSManifest object overrides the manifestName that you provided on the originEndpoint object\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaylistType`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-playlisttype"></a>
When specified as either `event` or `vod`, a corresponding `EXT-X-PLAYLIST-TYPE` entry is included in the media playlist\. Indicates if the playlist is live\-to\-VOD content\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaylistWindowSeconds`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-playlistwindowseconds"></a>
Time window \(in seconds\) contained in each parent manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimeIntervalSeconds`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-programdatetimeintervalseconds"></a>
Inserts `EXT-X-PROGRAM-DATE-TIME `tags in the output manifest at the interval that you specify\. Additionally, ID3Timed metadata messages are generated every 5 seconds starting when the content was ingested\.  
Irrespective of this parameter, if any ID3Timed metadata is in the HLS input, it is passed through to the HLS output\.  
Omit this attribute or enter `0` to indicate that the `EXT-X-PROGRAM-DATE-TIME` tags are not included in the manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackage-originendpoint-hlsmanifest-url"></a>
The URL that's used to request this manifest from this endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)