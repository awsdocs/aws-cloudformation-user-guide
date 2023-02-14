# AWS::MediaLive::Channel HlsOutputSettings<a name="aws-properties-medialive-channel-hlsoutputsettings"></a>

The settings for an HLS output\.

The parent of this entity is OutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlsoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsoutputsettings-syntax.json"></a>

```
{
  "[H265PackagingType](#cfn-medialive-channel-hlsoutputsettings-h265packagingtype)" : String,
  "[HlsSettings](#cfn-medialive-channel-hlsoutputsettings-hlssettings)" : HlsSettings,
  "[NameModifier](#cfn-medialive-channel-hlsoutputsettings-namemodifier)" : String,
  "[SegmentModifier](#cfn-medialive-channel-hlsoutputsettings-segmentmodifier)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-hlsoutputsettings-syntax.yaml"></a>

```
  [H265PackagingType](#cfn-medialive-channel-hlsoutputsettings-h265packagingtype): String
  [HlsSettings](#cfn-medialive-channel-hlsoutputsettings-hlssettings): 
    HlsSettings
  [NameModifier](#cfn-medialive-channel-hlsoutputsettings-namemodifier): String
  [SegmentModifier](#cfn-medialive-channel-hlsoutputsettings-segmentmodifier): String
```

## Properties<a name="aws-properties-medialive-channel-hlsoutputsettings-properties"></a>

`H265PackagingType`  <a name="cfn-medialive-channel-hlsoutputsettings-h265packagingtype"></a>
Only applicable when this output is referencing an H\.265 video description\. Specifies whether MP4 segments should be packaged as HEV1 or HVC1\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsSettings`  <a name="cfn-medialive-channel-hlsoutputsettings-hlssettings"></a>
The settings regarding the underlying stream\. These settings are different for audio\-only outputs\.  
*Required*: No  
*Type*: [HlsSettings](aws-properties-medialive-channel-hlssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NameModifier`  <a name="cfn-medialive-channel-hlsoutputsettings-namemodifier"></a>
A string that is concatenated to the end of the destination file name\. Accepts \\"Format Identifiers\\":\#formatIdentifierParameters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentModifier`  <a name="cfn-medialive-channel-hlsoutputsettings-segmentmodifier"></a>
A string that is concatenated to the end of segment file names\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)