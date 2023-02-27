# AWS::MediaPackage::PackagingConfiguration DashPackage<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage"></a>

Parameters for a packaging configuration that uses Dynamic Adaptive Streaming over HTTP \(DASH\) packaging\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-syntax.json"></a>

```
{
  "[DashManifests](#cfn-mediapackage-packagingconfiguration-dashpackage-dashmanifests)" : [ DashManifest, ... ],
  "[Encryption](#cfn-mediapackage-packagingconfiguration-dashpackage-encryption)" : DashEncryption,
  "[IncludeEncoderConfigurationInSegments](#cfn-mediapackage-packagingconfiguration-dashpackage-includeencoderconfigurationinsegments)" : Boolean,
  "[IncludeIframeOnlyStream](#cfn-mediapackage-packagingconfiguration-dashpackage-includeiframeonlystream)" : Boolean,
  "[PeriodTriggers](#cfn-mediapackage-packagingconfiguration-dashpackage-periodtriggers)" : [ String, ... ],
  "[SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-dashpackage-segmentdurationseconds)" : Integer,
  "[SegmentTemplateFormat](#cfn-mediapackage-packagingconfiguration-dashpackage-segmenttemplateformat)" : String
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-syntax.yaml"></a>

```
  [DashManifests](#cfn-mediapackage-packagingconfiguration-dashpackage-dashmanifests): 
    - DashManifest
  [Encryption](#cfn-mediapackage-packagingconfiguration-dashpackage-encryption): 
    DashEncryption
  [IncludeEncoderConfigurationInSegments](#cfn-mediapackage-packagingconfiguration-dashpackage-includeencoderconfigurationinsegments): Boolean
  [IncludeIframeOnlyStream](#cfn-mediapackage-packagingconfiguration-dashpackage-includeiframeonlystream): Boolean
  [PeriodTriggers](#cfn-mediapackage-packagingconfiguration-dashpackage-periodtriggers): 
    - String
  [SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-dashpackage-segmentdurationseconds): Integer
  [SegmentTemplateFormat](#cfn-mediapackage-packagingconfiguration-dashpackage-segmenttemplateformat): String
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-properties"></a>

`DashManifests`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-dashmanifests"></a>
A list of DASH manifest configurations that are available from this endpoint\.  
*Required*: Yes  
*Type*: List of [DashManifest](aws-properties-mediapackage-packagingconfiguration-dashmanifest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encryption`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [DashEncryption](aws-properties-mediapackage-packagingconfiguration-dashencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeEncoderConfigurationInSegments`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-includeencoderconfigurationinsegments"></a>
When includeEncoderConfigurationInSegments is set to true, AWS Elemental MediaPackage places your encoder's Sequence Parameter Set \(SPS\), Picture Parameter Set \(PPS\), and Video Parameter Set \(VPS\) metadata in every video segment instead of in the init fragment\. This lets you use different SPS/PPS/VPS settings for your assets during content playback\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStream`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-includeiframeonlystream"></a>
This applies only to stream sets with a single video track\. When true, the stream set includes an additional I\-frame trick\-play only stream, along with the other tracks\. If false, this extra stream is not included\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodTriggers`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-periodtriggers"></a>
Controls whether AWS Elemental MediaPackage produces single\-period or multi\-period DASH manifests\. For more information about periods, see [Multi\-period DASH in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/multi-period.html)\.  
Valid values:  
+ **ADS** \- AWS Elemental MediaPackage will produce multi\-period DASH manifests\. Periods are created based on the SCTE\-35 ad markers present in the input manifest\.
+ *No value* \- AWS Elemental MediaPackage will produce single\-period DASH manifests\. This is the default setting\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each fragment\. Actual fragments are rounded to the nearest multiple of the source segment duration\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentTemplateFormat`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-segmenttemplateformat"></a>
Determines the type of SegmentTemplate included in the Media Presentation Description \(MPD\)\. When set to **NUMBER\_WITH\_TIMELINE**, a full timeline is presented in each SegmentTemplate, with $Number$ media URLs\. When set to **TIME\_WITH\_TIMELINE**, a full timeline is presented in each SegmentTemplate, with $Time$ media URLs\. When set to **NUMBER\_WITH\_DURATION**, only a duration is included in each SegmentTemplate, with $Number$ media URLs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)