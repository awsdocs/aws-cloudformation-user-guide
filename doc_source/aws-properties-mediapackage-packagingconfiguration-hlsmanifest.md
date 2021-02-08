# AWS::MediaPackage::PackagingConfiguration HlsManifest<a name="aws-properties-mediapackage-packagingconfiguration-hlsmanifest"></a>

Parameters for an HLS manifest\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-hlsmanifest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-hlsmanifest-syntax.json"></a>

```
{
  "[AdMarkers](#cfn-mediapackage-packagingconfiguration-hlsmanifest-admarkers)" : String,
  "[IncludeIframeOnlyStream](#cfn-mediapackage-packagingconfiguration-hlsmanifest-includeiframeonlystream)" : Boolean,
  "[ManifestName](#cfn-mediapackage-packagingconfiguration-hlsmanifest-manifestname)" : String,
  "[ProgramDateTimeIntervalSeconds](#cfn-mediapackage-packagingconfiguration-hlsmanifest-programdatetimeintervalseconds)" : Integer,
  "[RepeatExtXKey](#cfn-mediapackage-packagingconfiguration-hlsmanifest-repeatextxkey)" : Boolean,
  "[StreamSelection](#cfn-mediapackage-packagingconfiguration-hlsmanifest-streamselection)" : StreamSelection
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-hlsmanifest-syntax.yaml"></a>

```
  [AdMarkers](#cfn-mediapackage-packagingconfiguration-hlsmanifest-admarkers): String
  [IncludeIframeOnlyStream](#cfn-mediapackage-packagingconfiguration-hlsmanifest-includeiframeonlystream): Boolean
  [ManifestName](#cfn-mediapackage-packagingconfiguration-hlsmanifest-manifestname): String
  [ProgramDateTimeIntervalSeconds](#cfn-mediapackage-packagingconfiguration-hlsmanifest-programdatetimeintervalseconds): Integer
  [RepeatExtXKey](#cfn-mediapackage-packagingconfiguration-hlsmanifest-repeatextxkey): Boolean
  [StreamSelection](#cfn-mediapackage-packagingconfiguration-hlsmanifest-streamselection): 
    StreamSelection
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-hlsmanifest-properties"></a>

`AdMarkers`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-admarkers"></a>
This setting controls ad markers in the packaged content\. **NONE** omits SCTE\-35 ad markers from the output\. **PASSTHROUGH** copies SCTE\-35 ad markers from the source content to the output\. **SCTE35\_ENHANCED** generates ad markers and blackout tags in the output, based on SCTE\-35 messages in the source content\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStream`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-includeiframeonlystream"></a>
Applies to stream sets with a single video track only\. When enabled, the output includes an additional I\-frame only stream, along with the other tracks\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestName`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-manifestname"></a>
A short string that's appended to the end of the endpoint URL to create a unique path to this packaging configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimeIntervalSeconds`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-programdatetimeintervalseconds"></a>
Inserts `EXT-X-PROGRAM-DATE-TIME` tags in the output manifest at the interval that you specify\. Additionally, ID3Timed metadata messages are generated every 5 seconds starting when the content was ingested\.  
Irrespective of this parameter, if any ID3Timed metadata is in the HLS input, it is passed through to the HLS output\.  
Omit this attribute or enter `0` to indicate that the `EXT-X-PROGRAM-DATE-TIME` tags are not included in the manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepeatExtXKey`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-repeatextxkey"></a>
Repeat the `EXT-X-KEY` directive for every media segment\. This might result in an increase in client requests to the DRM server\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamSelection`  <a name="cfn-mediapackage-packagingconfiguration-hlsmanifest-streamselection"></a>
Video bitrate limitations for outputs from this packaging configuration\.  
*Required*: No  
*Type*: [StreamSelection](aws-properties-mediapackage-packagingconfiguration-streamselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)