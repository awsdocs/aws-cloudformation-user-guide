# AWS::MediaLive::Channel VideoSelectorColorSpaceSettings<a name="aws-properties-medialive-channel-videoselectorcolorspacesettings"></a>

Settings to configure color space settings in the incoming video\.

The parent of this entity is VideoSelector\.

## Syntax<a name="aws-properties-medialive-channel-videoselectorcolorspacesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoselectorcolorspacesettings-syntax.json"></a>

```
{
  "[Hdr10Settings](#cfn-medialive-channel-videoselectorcolorspacesettings-hdr10settings)" : Hdr10Settings
}
```

### YAML<a name="aws-properties-medialive-channel-videoselectorcolorspacesettings-syntax.yaml"></a>

```
  [Hdr10Settings](#cfn-medialive-channel-videoselectorcolorspacesettings-hdr10settings): 
    Hdr10Settings
```

## Properties<a name="aws-properties-medialive-channel-videoselectorcolorspacesettings-properties"></a>

`Hdr10Settings`  <a name="cfn-medialive-channel-videoselectorcolorspacesettings-hdr10settings"></a>
Settings to configure color space settings in the incoming video\.  
*Required*: No  
*Type*: [Hdr10Settings](aws-properties-medialive-channel-hdr10settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)