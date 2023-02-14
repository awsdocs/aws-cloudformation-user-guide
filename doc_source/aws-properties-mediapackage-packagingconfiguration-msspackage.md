# AWS::MediaPackage::PackagingConfiguration MssPackage<a name="aws-properties-mediapackage-packagingconfiguration-msspackage"></a>

Parameters for a packaging configuration that uses Microsoft Smooth Streaming \(MSS\) packaging\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-msspackage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-msspackage-syntax.json"></a>

```
{
  "[Encryption](#cfn-mediapackage-packagingconfiguration-msspackage-encryption)" : MssEncryption,
  "[MssManifests](#cfn-mediapackage-packagingconfiguration-msspackage-mssmanifests)" : [ MssManifest, ... ],
  "[SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-msspackage-segmentdurationseconds)" : Integer
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-msspackage-syntax.yaml"></a>

```
  [Encryption](#cfn-mediapackage-packagingconfiguration-msspackage-encryption): 
    MssEncryption
  [MssManifests](#cfn-mediapackage-packagingconfiguration-msspackage-mssmanifests): 
    - MssManifest
  [SegmentDurationSeconds](#cfn-mediapackage-packagingconfiguration-msspackage-segmentdurationseconds): Integer
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-msspackage-properties"></a>

`Encryption`  <a name="cfn-mediapackage-packagingconfiguration-msspackage-encryption"></a>
Parameters for encrypting content\.  
*Required*: No  
*Type*: [MssEncryption](aws-properties-mediapackage-packagingconfiguration-mssencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MssManifests`  <a name="cfn-mediapackage-packagingconfiguration-msspackage-mssmanifests"></a>
A list of Microsoft Smooth manifest configurations that are available from this endpoint\.  
*Required*: Yes  
*Type*: List of [MssManifest](aws-properties-mediapackage-packagingconfiguration-mssmanifest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackage-packagingconfiguration-msspackage-segmentdurationseconds"></a>
Duration \(in seconds\) of each fragment\. Actual fragments are rounded to the nearest multiple of the source fragment duration\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)