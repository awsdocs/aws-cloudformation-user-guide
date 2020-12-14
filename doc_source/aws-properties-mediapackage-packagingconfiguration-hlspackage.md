# AWS::MediaPackage::PackagingConfiguration HlsPackage<a name="aws-properties-mediapackage-packagingconfiguration-hlspackage"></a>

Parameters for a packaging configuration that uses HTTP Live Streaming \(HLS\) packaging\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-hlspackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-hlspackage-syntax.json"></a>

```
{
  "[Encryption](#cfn-mediapackage-packagingconfiguration-hlspackage-encryption)" : HlsEncryption,
  "[HlsManifests](#cfn-mediapackage-packagingconfiguration-hlspackage-hlsmanifests)" : [ HlsManifest, ... ],
  "[SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-hlspackage-segmentdurationseconds)" : Integer,
  "[UseAudioRenditionGroup](#cfn-mediapackage-packagingconfiguration-hlspackage-useaudiorenditiongroup)" : Boolean
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-hlspackage-syntax.yaml"></a>

```
  [Encryption](#cfn-mediapackage-packagingconfiguration-hlspackage-encryption): 
    HlsEncryption
  [HlsManifests](#cfn-mediapackage-packagingconfiguration-hlspackage-hlsmanifests): 
    - HlsManifest
  [SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-hlspackage-segmentdurationseconds): Integer
  [UseAudioRenditionGroup](#cfn-mediapackage-packagingconfiguration-hlspackage-useaudiorenditiongroup): Boolean
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-hlspackage-properties"></a>

`Encryption`  <a name="cfn-mediapackage-packagingconfiguration-hlspackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [HlsEncryption](aws-properties-mediapackage-packagingconfiguration-hlsencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsManifests`  <a name="cfn-mediapackage-packagingconfiguration-hlspackage-hlsmanifests"></a>
A list of HLS manifest configurations that are available from this endpoint\.  
*Required*: Yes  
*Type*: List of [HlsManifest](aws-properties-mediapackage-packagingconfiguration-hlsmanifest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-packagingconfiguration-hlspackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each fragment\. Actual fragments are rounded to the nearest multiple of the source fragment duration\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseAudioRenditionGroup`  <a name="cfn-mediapackage-packagingconfiguration-hlspackage-useaudiorenditiongroup"></a>
When true, AWS Elemental MediaPackage bundles all audio tracks in a rendition group\. All other tracks in the stream can be used with any audio rendition from the group\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)