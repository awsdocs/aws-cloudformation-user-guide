# AWS::MediaPackage::PackagingConfiguration DashPackage<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage"></a>

Parameters for a packaging configuration that uses Dynamic Adaptive Streaming over HTTP \(DASH\) packaging\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-dashpackage-syntax.json"></a>

```
{
  "[DashManifests](#cfn-mediapackage-packagingconfiguration-dashpackage-dashmanifests)" : [ DashManifest, ... ],
  "[Encryption](#cfn-mediapackage-packagingconfiguration-dashpackage-encryption)" : DashEncryption,
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

`PeriodTriggers`  <a name="cfn-mediapackage-packagingconfiguration-dashpackage-periodtriggers"></a>
A list of triggers that controls when the outgoing Dynamic Adaptive Streaming over HTTP \(DASH\) Media Presentation Description \(MPD\) is partitioned into multiple periods\. If empty, the content isl not partitioned into more than one period\. If the list contains "ADS", new periods are created where the Asset contains SCTE\-35 ad markers\.   
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