# AWS::MediaTailor::Channel HlsPlaylistSettings<a name="aws-properties-mediatailor-channel-hlsplaylistsettings"></a>

HLS playlist configuration parameters\.

## Syntax<a name="aws-properties-mediatailor-channel-hlsplaylistsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-channel-hlsplaylistsettings-syntax.json"></a>

```
{
  "[ManifestWindowSeconds](#cfn-mediatailor-channel-hlsplaylistsettings-manifestwindowseconds)" : Double
}
```

### YAML<a name="aws-properties-mediatailor-channel-hlsplaylistsettings-syntax.yaml"></a>

```
  [ManifestWindowSeconds](#cfn-mediatailor-channel-hlsplaylistsettings-manifestwindowseconds): Double
```

## Properties<a name="aws-properties-mediatailor-channel-hlsplaylistsettings-properties"></a>

`ManifestWindowSeconds`  <a name="cfn-mediatailor-channel-hlsplaylistsettings-manifestwindowseconds"></a>
The total duration \(in seconds\) of each manifest\. Minimum value: `30` seconds\. Maximum value: `3600` seconds\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)