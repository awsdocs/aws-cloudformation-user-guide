# AWS::MediaLive::Channel StandardHlsSettings<a name="aws-properties-medialive-channel-standardhlssettings"></a>

The configuration of an HLS output that is a standard output \(not an audio\-only output\)\.

The parent of this entity is HlsSettings\.

## Syntax<a name="aws-properties-medialive-channel-standardhlssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-standardhlssettings-syntax.json"></a>

```
{
  "[AudioRenditionSets](#cfn-medialive-channel-standardhlssettings-audiorenditionsets)" : String,
  "[M3u8Settings](#cfn-medialive-channel-standardhlssettings-m3u8settings)" : M3u8Settings
}
```

### YAML<a name="aws-properties-medialive-channel-standardhlssettings-syntax.yaml"></a>

```
  [AudioRenditionSets](#cfn-medialive-channel-standardhlssettings-audiorenditionsets): String
  [M3u8Settings](#cfn-medialive-channel-standardhlssettings-m3u8settings): 
    M3u8Settings
```

## Properties<a name="aws-properties-medialive-channel-standardhlssettings-properties"></a>

`AudioRenditionSets`  <a name="cfn-medialive-channel-standardhlssettings-audiorenditionsets"></a>
Lists all the audio groups that are used with the video output stream\. This inputs all the audio GROUP\-IDs that are associated with the video, separated by a comma \(,\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`M3u8Settings`  <a name="cfn-medialive-channel-standardhlssettings-m3u8settings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [M3u8Settings](aws-properties-medialive-channel-m3u8settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)