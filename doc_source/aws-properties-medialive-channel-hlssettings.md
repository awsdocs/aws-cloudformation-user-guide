# AWS::MediaLive::Channel HlsSettings<a name="aws-properties-medialive-channel-hlssettings"></a>

The settings for an HLS output\.

The parent of this entity is HlsOutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlssettings-syntax.json"></a>

```
{
  "[AudioOnlyHlsSettings](#cfn-medialive-channel-hlssettings-audioonlyhlssettings)" : AudioOnlyHlsSettings,
  "[Fmp4HlsSettings](#cfn-medialive-channel-hlssettings-fmp4hlssettings)" : Fmp4HlsSettings,
  "[StandardHlsSettings](#cfn-medialive-channel-hlssettings-standardhlssettings)" : StandardHlsSettings
}
```

### YAML<a name="aws-properties-medialive-channel-hlssettings-syntax.yaml"></a>

```
  [AudioOnlyHlsSettings](#cfn-medialive-channel-hlssettings-audioonlyhlssettings): 
    AudioOnlyHlsSettings
  [Fmp4HlsSettings](#cfn-medialive-channel-hlssettings-fmp4hlssettings): 
    Fmp4HlsSettings
  [StandardHlsSettings](#cfn-medialive-channel-hlssettings-standardhlssettings): 
    StandardHlsSettings
```

## Properties<a name="aws-properties-medialive-channel-hlssettings-properties"></a>

`AudioOnlyHlsSettings`  <a name="cfn-medialive-channel-hlssettings-audioonlyhlssettings"></a>
The settings for an audio\-only output\.  
*Required*: No  
*Type*: [AudioOnlyHlsSettings](aws-properties-medialive-channel-audioonlyhlssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fmp4HlsSettings`  <a name="cfn-medialive-channel-hlssettings-fmp4hlssettings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Fmp4HlsSettings](aws-properties-medialive-channel-fmp4hlssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StandardHlsSettings`  <a name="cfn-medialive-channel-hlssettings-standardhlssettings"></a>
The settings for a standard output \(an output that is not audio\-only\)\.  
*Required*: No  
*Type*: [StandardHlsSettings](aws-properties-medialive-channel-standardhlssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)