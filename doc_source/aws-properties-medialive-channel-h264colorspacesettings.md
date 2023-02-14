# AWS::MediaLive::Channel H264ColorSpaceSettings<a name="aws-properties-medialive-channel-h264colorspacesettings"></a>

Settings for configuring color space in an H264 video encode\.

The parent of this entity is H264Settings\.

## Syntax<a name="aws-properties-medialive-channel-h264colorspacesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-h264colorspacesettings-syntax.json"></a>

```
{
  "[ColorSpacePassthroughSettings](#cfn-medialive-channel-h264colorspacesettings-colorspacepassthroughsettings)" : ColorSpacePassthroughSettings,
  "[Rec601Settings](#cfn-medialive-channel-h264colorspacesettings-rec601settings)" : Rec601Settings,
  "[Rec709Settings](#cfn-medialive-channel-h264colorspacesettings-rec709settings)" : Rec709Settings
}
```

### YAML<a name="aws-properties-medialive-channel-h264colorspacesettings-syntax.yaml"></a>

```
  [ColorSpacePassthroughSettings](#cfn-medialive-channel-h264colorspacesettings-colorspacepassthroughsettings): 
    ColorSpacePassthroughSettings
  [Rec601Settings](#cfn-medialive-channel-h264colorspacesettings-rec601settings): 
    Rec601Settings
  [Rec709Settings](#cfn-medialive-channel-h264colorspacesettings-rec709settings): 
    Rec709Settings
```

## Properties<a name="aws-properties-medialive-channel-h264colorspacesettings-properties"></a>

`ColorSpacePassthroughSettings`  <a name="cfn-medialive-channel-h264colorspacesettings-colorspacepassthroughsettings"></a>
Passthrough applies no color space conversion to the output\.   
*Required*: No  
*Type*: [ColorSpacePassthroughSettings](aws-properties-medialive-channel-colorspacepassthroughsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rec601Settings`  <a name="cfn-medialive-channel-h264colorspacesettings-rec601settings"></a>
Settings to configure the handling of Rec601 color space\.  
*Required*: No  
*Type*: [Rec601Settings](aws-properties-medialive-channel-rec601settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rec709Settings`  <a name="cfn-medialive-channel-h264colorspacesettings-rec709settings"></a>
Settings to configure the handling of Rec709 color space\.  
*Required*: No  
*Type*: [Rec709Settings](aws-properties-medialive-channel-rec709settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)