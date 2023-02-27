# AWS::MediaPackage::OriginEndpoint DashPackage<a name="aws-properties-mediapackage-originendpoint-dashpackage"></a>

Parameters for DASH packaging\.

## Syntax<a name="aws-properties-mediapackage-originendpoint-dashpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-dashpackage-syntax.json"></a>

```
{
  "[AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-dashpackage-adsondeliveryrestrictions)" : String,
  "[AdTriggers](#cfn-mediapackage-originendpoint-dashpackage-adtriggers)" : [ String, ... ],
  "[Encryption](#cfn-mediapackage-originendpoint-dashpackage-encryption)" : DashEncryption,
  "[IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-dashpackage-includeiframeonlystream)" : Boolean,
  "[ManifestLayout](#cfn-mediapackage-originendpoint-dashpackage-manifestlayout)" : String,
  "[ManifestWindowSeconds](#cfn-mediapackage-originendpoint-dashpackage-manifestwindowseconds)" : Integer,
  "[MinBufferTimeSeconds](#cfn-mediapackage-originendpoint-dashpackage-minbuffertimeseconds)" : Integer,
  "[MinUpdatePeriodSeconds](#cfn-mediapackage-originendpoint-dashpackage-minupdateperiodseconds)" : Integer,
  "[PeriodTriggers](#cfn-mediapackage-originendpoint-dashpackage-periodtriggers)" : [ String, ... ],
  "[Profile](#cfn-mediapackage-originendpoint-dashpackage-profile)" : String,
  "[SegmentDurationSeconds](#cfn-mediapackage-originendpoint-dashpackage-segmentdurationseconds)" : Integer,
  "[SegmentTemplateFormat](#cfn-mediapackage-originendpoint-dashpackage-segmenttemplateformat)" : String,
  "[StreamSelection](#cfn-mediapackage-originendpoint-dashpackage-streamselection)" : StreamSelection,
  "[SuggestedPresentationDelaySeconds](#cfn-mediapackage-originendpoint-dashpackage-suggestedpresentationdelayseconds)" : Integer,
  "[UtcTiming](#cfn-mediapackage-originendpoint-dashpackage-utctiming)" : String,
  "[UtcTimingUri](#cfn-mediapackage-originendpoint-dashpackage-utctiminguri)" : String
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-dashpackage-syntax.yaml"></a>

```
  [AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-dashpackage-adsondeliveryrestrictions): String
  [AdTriggers](#cfn-mediapackage-originendpoint-dashpackage-adtriggers): 
    - String
  [Encryption](#cfn-mediapackage-originendpoint-dashpackage-encryption): 
    DashEncryption
  [IncludeIframeOnlyStream](#cfn-mediapackage-originendpoint-dashpackage-includeiframeonlystream): Boolean
  [ManifestLayout](#cfn-mediapackage-originendpoint-dashpackage-manifestlayout): String
  [ManifestWindowSeconds](#cfn-mediapackage-originendpoint-dashpackage-manifestwindowseconds): Integer
  [MinBufferTimeSeconds](#cfn-mediapackage-originendpoint-dashpackage-minbuffertimeseconds): Integer
  [MinUpdatePeriodSeconds](#cfn-mediapackage-originendpoint-dashpackage-minupdateperiodseconds): Integer
  [PeriodTriggers](#cfn-mediapackage-originendpoint-dashpackage-periodtriggers): 
    - String
  [Profile](#cfn-mediapackage-originendpoint-dashpackage-profile): String
  [SegmentDurationSeconds](#cfn-mediapackage-originendpoint-dashpackage-segmentdurationseconds): Integer
  [SegmentTemplateFormat](#cfn-mediapackage-originendpoint-dashpackage-segmenttemplateformat): String
  [StreamSelection](#cfn-mediapackage-originendpoint-dashpackage-streamselection): 
    StreamSelection
  [SuggestedPresentationDelaySeconds](#cfn-mediapackage-originendpoint-dashpackage-suggestedpresentationdelayseconds): Integer
  [UtcTiming](#cfn-mediapackage-originendpoint-dashpackage-utctiming): String
  [UtcTimingUri](#cfn-mediapackage-originendpoint-dashpackage-utctiminguri): String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-dashpackage-properties"></a>

`AdsOnDeliveryRestrictions`  <a name="cfn-mediapackage-originendpoint-dashpackage-adsondeliveryrestrictions"></a>
The flags on SCTE\-35 segmentation descriptors that have to be present for AWS Elemental MediaPackage to insert ad markers in the output manifest\. For information about SCTE\-35 in AWS Elemental MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdTriggers`  <a name="cfn-mediapackage-originendpoint-dashpackage-adtriggers"></a>
Specifies the SCTE\-35 message types that AWS Elemental MediaPackage treats as ad markers in the output manifest\.  
Valid values:  
+ **BREAK**
+ **DISTRIBUTOR\_ADVERTISEMENT**
+ **DISTRIBUTOR\_OVERLAY\_PLACEMENT\_OPPORTUNITY**\.
+ **DISTRIBUTOR\_PLACEMENT\_OPPORTUNITY**\.
+ **PROVIDER\_ADVERTISEMENT**\.
+ **PROVIDER\_OVERLAY\_PLACEMENT\_OPPORTUNITY**\.
+ **PROVIDER\_PLACEMENT\_OPPORTUNITY**\.
+ **SPLICE\_INSERT**\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encryption`  <a name="cfn-mediapackage-originendpoint-dashpackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [DashEncryption](aws-properties-mediapackage-originendpoint-dashencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStream`  <a name="cfn-mediapackage-originendpoint-dashpackage-includeiframeonlystream"></a>
This applies only to stream sets with a single video track\. When true, the stream set includes an additional I\-frame trick\-play only stream, along with the other tracks\. If false, this extra stream is not included\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestLayout`  <a name="cfn-mediapackage-originendpoint-dashpackage-manifestlayout"></a>
Determines the position of some tags in the manifest\.   
Valid values:  
+ **FULL** \- Elements like `SegmentTemplate` and `ContentProtection` are included in each `Representation`\.
+ **COMPACT** \- Duplicate elements are combined and presented at the `AdaptationSet` level\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestWindowSeconds`  <a name="cfn-mediapackage-originendpoint-dashpackage-manifestwindowseconds"></a>
Time window \(in seconds\) contained in each manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinBufferTimeSeconds`  <a name="cfn-mediapackage-originendpoint-dashpackage-minbuffertimeseconds"></a>
Minimum amount of content \(measured in seconds\) that a player must keep available in the buffer\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinUpdatePeriodSeconds`  <a name="cfn-mediapackage-originendpoint-dashpackage-minupdateperiodseconds"></a>
Minimum amount of time \(in seconds\) that the player should wait before requesting updates to the manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodTriggers`  <a name="cfn-mediapackage-originendpoint-dashpackage-periodtriggers"></a>
Controls whether AWS Elemental MediaPackage produces single\-period or multi\-period DASH manifests\. For more information about periods, see [Multi\-period DASH in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/multi-period.html)\.  
Valid values:  
+ **ADS** \- AWS Elemental MediaPackage will produce multi\-period DASH manifests\. Periods are created based on the SCTE\-35 ad markers present in the input manifest\.
+ *No value* \- AWS Elemental MediaPackage will produce single\-period DASH manifests\. This is the default setting\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Profile`  <a name="cfn-mediapackage-originendpoint-dashpackage-profile"></a>
The DASH profile for the output\.  
Valid values:  
+ **NONE** \- The output doesn't use a DASH profile\.
+ **HBBTV\_1\_5** \- The output is compliant with HbbTV v1\.5\.
+ **DVB\_DASH\_2014** \- The output is compliant with DVB\-DASH 2014\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-originendpoint-dashpackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each fragment\. Actual fragments are rounded to the nearest multiple of the source fragment duration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentTemplateFormat`  <a name="cfn-mediapackage-originendpoint-dashpackage-segmenttemplateformat"></a>
Determines the type of variable used in the `media` URL of the `SegmentTemplate` tag in the manifest\. Also specifies if segment timeline information is included in `SegmentTimeline` or `SegmentTemplate`\.  
Valid values:  
+ **NUMBER\_WITH\_TIMELINE** \- The `$Number$` variable is used in the `media` URL\. The value of this variable is the sequential number of the segment\. A full `SegmentTimeline` object is presented in each `SegmentTemplate`\.
+ **NUMBER\_WITH\_DURATION** \- The `$Number$` variable is used in the `media` URL and a `duration` attribute is added to the segment template\. The `SegmentTimeline` object is removed from the representation\.
+ **TIME\_WITH\_TIMELINE** \- The `$Time$` variable is used in the `media` URL\. The value of this variable is the timestamp of when the segment starts\. A full `SegmentTimeline` object is presented in each `SegmentTemplate`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamSelection`  <a name="cfn-mediapackage-originendpoint-dashpackage-streamselection"></a>
Limitations for outputs from the endpoint, based on the video bitrate\.  
*Required*: No  
*Type*: [StreamSelection](aws-properties-mediapackage-originendpoint-streamselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuggestedPresentationDelaySeconds`  <a name="cfn-mediapackage-originendpoint-dashpackage-suggestedpresentationdelayseconds"></a>
Amount of time \(in seconds\) that the player should be from the live point at the end of the manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UtcTiming`  <a name="cfn-mediapackage-originendpoint-dashpackage-utctiming"></a>
Determines the type of UTC timing included in the DASH Media Presentation Description \(MPD\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UtcTimingUri`  <a name="cfn-mediapackage-originendpoint-dashpackage-utctiminguri"></a>
Specifies the value attribute of the UTC timing field when utcTiming is set to HTTP\-ISO or HTTP\-HEAD\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)