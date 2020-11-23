# AWS::MediaPackage::PackagingConfiguration CmafPackage<a name="aws-properties-mediapackage-packagingconfiguration-cmafpackage"></a>

Parameters for a packaging configuration that uses Common Media Application Format \(CMAF\) packaging\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-cmafpackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-cmafpackage-syntax.json"></a>

```
{
  "[Encryption](#cfn-mediapackage-packagingconfiguration-cmafpackage-encryption)" : CmafEncryption,
  "[HlsManifests](#cfn-mediapackage-packagingconfiguration-cmafpackage-hlsmanifests)" : [ HlsManifest, ... ],
  "[SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-cmafpackage-segmentdurationseconds)" : Integer
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-cmafpackage-syntax.yaml"></a>

```
  [Encryption](#cfn-mediapackage-packagingconfiguration-cmafpackage-encryption): 
    CmafEncryption
  [HlsManifests](#cfn-mediapackage-packagingconfiguration-cmafpackage-hlsmanifests): 
    - HlsManifest
  [SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-cmafpackage-segmentdurationseconds): Integer
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-cmafpackage-properties"></a>

`Encryption`  <a name="cfn-mediapackage-packagingconfiguration-cmafpackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [CmafEncryption](aws-properties-mediapackage-packagingconfiguration-cmafencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsManifests`  <a name="cfn-mediapackage-packagingconfiguration-cmafpackage-hlsmanifests"></a>
A list of HLS manifest configurations that are available from this endpoint\.  
*Required*: Yes  
*Type*: List of [HlsManifest](aws-properties-mediapackage-packagingconfiguration-hlsmanifest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-packagingconfiguration-cmafpackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each segment\. Actual segments are rounded to the nearest multiple of the source fragment duration\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)