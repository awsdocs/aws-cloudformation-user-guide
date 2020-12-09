# AWS::MediaPackage::PackagingConfiguration MssManifest<a name="aws-properties-mediapackage-packagingconfiguration-mssmanifest"></a>

Parameters for a Microsoft Smooth manifest\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-mssmanifest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-mssmanifest-syntax.json"></a>

```
{
  "[ManifestName](#cfn-mediapackage-packagingconfiguration-mssmanifest-manifestname)" : String,
  "[StreamSelection](#cfn-mediapackage-packagingconfiguration-mssmanifest-streamselection)" : StreamSelection
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-mssmanifest-syntax.yaml"></a>

```
  [ManifestName](#cfn-mediapackage-packagingconfiguration-mssmanifest-manifestname): String
  [StreamSelection](#cfn-mediapackage-packagingconfiguration-mssmanifest-streamselection): 
    StreamSelection
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-mssmanifest-properties"></a>

`ManifestName`  <a name="cfn-mediapackage-packagingconfiguration-mssmanifest-manifestname"></a>
A short string that's appended to the end of the endpoint URL to create a unique path to this packaging configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamSelection`  <a name="cfn-mediapackage-packagingconfiguration-mssmanifest-streamselection"></a>
Video bitrate limitations for outputs from this packaging configuration\.  
*Required*: No  
*Type*: [StreamSelection](aws-properties-mediapackage-packagingconfiguration-streamselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)