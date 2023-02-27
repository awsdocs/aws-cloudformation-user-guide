# AWS::MediaLive::Channel MsSmoothOutputSettings<a name="aws-properties-medialive-channel-mssmoothoutputsettings"></a>

Configuration of a Microsoft Smooth output\.

The parent of this entity is OutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-mssmoothoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mssmoothoutputsettings-syntax.json"></a>

```
{
  "[H265PackagingType](#cfn-medialive-channel-mssmoothoutputsettings-h265packagingtype)" : String,
  "[NameModifier](#cfn-medialive-channel-mssmoothoutputsettings-namemodifier)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-mssmoothoutputsettings-syntax.yaml"></a>

```
  [H265PackagingType](#cfn-medialive-channel-mssmoothoutputsettings-h265packagingtype): String
  [NameModifier](#cfn-medialive-channel-mssmoothoutputsettings-namemodifier): String
```

## Properties<a name="aws-properties-medialive-channel-mssmoothoutputsettings-properties"></a>

`H265PackagingType`  <a name="cfn-medialive-channel-mssmoothoutputsettings-h265packagingtype"></a>
Only applicable when this output is referencing an H\.265 video description\. Specifies whether MP4 segments should be packaged as HEV1 or HVC1\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NameModifier`  <a name="cfn-medialive-channel-mssmoothoutputsettings-namemodifier"></a>
A string that is concatenated to the end of the destination file name\. This is required for multiple outputs of the same type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)