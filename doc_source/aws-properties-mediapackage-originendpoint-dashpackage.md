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
  "[ManifestLayout](#cfn-mediapackage-originendpoint-dashpackage-manifestlayout)" : String,
  "[ManifestWindowSeconds](#cfn-mediapackage-originendpoint-dashpackage-manifestwindowseconds)" : Integer,
  "[MinBufferTimeSeconds](#cfn-mediapackage-originendpoint-dashpackage-minbuffertimeseconds)" : Integer,
  "[MinUpdatePeriodSeconds](#cfn-mediapackage-originendpoint-dashpackage-minupdateperiodseconds)" : Integer,
  "[PeriodTriggers](#cfn-mediapackage-originendpoint-dashpackage-periodtriggers)" : [ String, ... ],
  "[Profile](#cfn-mediapackage-originendpoint-dashpackage-profile)" : String,
  "[SegmentDurationSeconds](#cfn-mediapackage-originendpoint-dashpackage-segmentdurationseconds)" : Integer,
  "[SegmentTemplateFormat](#cfn-mediapackage-originendpoint-dashpackage-segmenttemplateformat)" : String,
  "[StreamSelection](#cfn-mediapackage-originendpoint-dashpackage-streamselection)" : StreamSelection,
  "[SuggestedPresentationDelaySeconds](#cfn-mediapackage-originendpoint-dashpackage-suggestedpresentationdelayseconds)" : Integer
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-dashpackage-syntax.yaml"></a>

```
  [AdsOnDeliveryRestrictions](#cfn-mediapackage-originendpoint-dashpackage-adsondeliveryrestrictions): String
  [AdTriggers](#cfn-mediapackage-originendpoint-dashpackage-adtriggers): 
    - String
  [Encryption](#cfn-mediapackage-originendpoint-dashpackage-encryption): 
    DashEncryption
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
```

## Properties<a name="aws-properties-mediapackage-originendpoint-dashpackage-properties"></a>

`AdsOnDeliveryRestrictions`  <a name="cfn-mediapackage-originendpoint-dashpackage-adsondeliveryrestrictions"></a>
The flags on SCTE\-35 segmentation descriptors that have to be present for MediaPackage to insert ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdTriggers`  <a name="cfn-mediapackage-originendpoint-dashpackage-adtriggers"></a>
The SCTE\-35 message types that MediaPackage treats as ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage\.   
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

`Encryption`  <a name="cfn-mediapackage-originendpoint-dashpackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [DashEncryption](aws-properties-mediapackage-originendpoint-dashencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestLayout`  <a name="cfn-mediapackage-originendpoint-dashpackage-manifestlayout"></a>
Determines the position of some tags in the manifest\.   
Options:  
+  **FULL** \- elements like `SegmentTemplate` and `ContentProtection` are included in each `Representation`\.
+  **COMPACT** \- duplicate elements are combined and presented at the `AdaptationSet` level\.
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
A list of triggers that controls when AWS Elemental MediaPackage separates the MPEG\-DASH manifest into multiple periods\. Type **ADS** to indicate that AWS Elemental MediaPackage must create periods in the output manifest that correspond to SCTE\-35 ad markers in the input source\. Leave this value empty to indicate that the manifest is contained all in one period\. For more information about periods in the DASH manifest, see [Multi\-period DASH in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/multi-period.html)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Profile`  <a name="cfn-mediapackage-originendpoint-dashpackage-profile"></a>
DASH profile for the output, such as HbbTV\.  
Valid values:  
+  **NONE** \- the output doesn't use a DASH profile\.
+  **HBBTV\_1\_5** \- the output is HbbTV\-compliant\.
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
+  **NUMBER\_WITH\_TIMELINE** \- The `$Number$` variable is used in the `media` URL\. The value of this variable is the sequential number of the segment\. A full `SegmentTimeline` object is presented in each `SegmentTemplate`\.
+  **NUMBER\_WITH\_DURATION** \- The `$Number$` variable is used in the `media` URL and a `duration` attribute is added to the segment template\. The `SegmentTimeline` object is removed from the representation\.
+  **TIME\_WITH\_TIMELINE** \- The `$Time$` variable is used in the `media` URL\. The value of this variable is the timestamp of when the segment starts\. A full `SegmentTimeline` object is presented in each `SegmentTemplate`\.
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