# AWS::MediaPackage::PackagingConfiguration DashManifest<a name="aws-properties-mediapackage-packagingconfiguration-dashmanifest"></a>

Parameters for a DASH manifest\.

## Syntax<a name="aws-properties-mediapackage-packagingconfiguration-dashmanifest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packagingconfiguration-dashmanifest-syntax.json"></a>

```
{
  "[ManifestLayout](#cfn-mediapackage-packagingconfiguration-dashmanifest-manifestlayout)" : String,
  "[ManifestName](#cfn-mediapackage-packagingconfiguration-dashmanifest-manifestname)" : String,
  "[MinBufferTimeSeconds](#cfn-mediapackage-packagingconfiguration-dashmanifest-minbuffertimeseconds)" : Integer,
  "[Profile](#cfn-mediapackage-packagingconfiguration-dashmanifest-profile)" : String,
  "[StreamSelection](#cfn-mediapackage-packagingconfiguration-dashmanifest-streamselection)" : StreamSelection
}
```

### YAML<a name="aws-properties-mediapackage-packagingconfiguration-dashmanifest-syntax.yaml"></a>

```
  [ManifestLayout](#cfn-mediapackage-packagingconfiguration-dashmanifest-manifestlayout): String
  [ManifestName](#cfn-mediapackage-packagingconfiguration-dashmanifest-manifestname): String
  [MinBufferTimeSeconds](#cfn-mediapackage-packagingconfiguration-dashmanifest-minbuffertimeseconds): Integer
  [Profile](#cfn-mediapackage-packagingconfiguration-dashmanifest-profile): String
  [StreamSelection](#cfn-mediapackage-packagingconfiguration-dashmanifest-streamselection): 
    StreamSelection
```

## Properties<a name="aws-properties-mediapackage-packagingconfiguration-dashmanifest-properties"></a>

`ManifestLayout`  <a name="cfn-mediapackage-packagingconfiguration-dashmanifest-manifestlayout"></a>
Determines the position of some tags in the Media Presentation Description \(MPD\)\. When set to **FULL**, elements like `SegmentTemplate` and `ContentProtection` are included in each `Representation`\. When set to **COMPACT**, duplicate elements are combined and presented at the AdaptationSet level\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestName`  <a name="cfn-mediapackage-packagingconfiguration-dashmanifest-manifestname"></a>
A short string that's appended to the end of the endpoint URL to create a unique path to this packaging configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinBufferTimeSeconds`  <a name="cfn-mediapackage-packagingconfiguration-dashmanifest-minbuffertimeseconds"></a>
Minimum amount of content \(measured in seconds\) that a player must keep available in the buffer\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Profile`  <a name="cfn-mediapackage-packagingconfiguration-dashmanifest-profile"></a>
The DASH profile type\. When set to **HBBTV\_1\_5**, the content is compliant with HbbTV 1\.5\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamSelection`  <a name="cfn-mediapackage-packagingconfiguration-dashmanifest-streamselection"></a>
Limitations for outputs from the endpoint, based on the video bitrate\.   
*Required*: No  
*Type*: [StreamSelection](aws-properties-mediapackage-packagingconfiguration-streamselection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)