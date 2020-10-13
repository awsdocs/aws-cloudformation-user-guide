# AWS::MediaLive::Channel H265ColorSpaceSettings<a name="aws-properties-medialive-channel-h265colorspacesettings"></a>

Specifies how to handle colorspace metadata in this output video encode\. In this element, include only one of the child elements\. This element belongs to H265Settings\.

## Syntax<a name="aws-properties-medialive-channel-h265colorspacesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-h265colorspacesettings-syntax.json"></a>

```
{
  "[ColorSpacePassthroughSettings](#cfn-medialive-channel-h265colorspacesettings-colorspacepassthroughsettings)" : ColorSpacePassthroughSettings,
  "[Hdr10Settings](#cfn-medialive-channel-h265colorspacesettings-hdr10settings)" : Hdr10Settings,
  "[Rec601Settings](#cfn-medialive-channel-h265colorspacesettings-rec601settings)" : Rec601Settings,
  "[Rec709Settings](#cfn-medialive-channel-h265colorspacesettings-rec709settings)" : Rec709Settings
}
```

### YAML<a name="aws-properties-medialive-channel-h265colorspacesettings-syntax.yaml"></a>

```
  [ColorSpacePassthroughSettings](#cfn-medialive-channel-h265colorspacesettings-colorspacepassthroughsettings): 
    ColorSpacePassthroughSettings
  [Hdr10Settings](#cfn-medialive-channel-h265colorspacesettings-hdr10settings): 
    Hdr10Settings
  [Rec601Settings](#cfn-medialive-channel-h265colorspacesettings-rec601settings): 
    Rec601Settings
  [Rec709Settings](#cfn-medialive-channel-h265colorspacesettings-rec709settings): 
    Rec709Settings
```

## Properties<a name="aws-properties-medialive-channel-h265colorspacesettings-properties"></a>

`ColorSpacePassthroughSettings`  <a name="cfn-medialive-channel-h265colorspacesettings-colorspacepassthroughsettings"></a>
Include this element if you want to pass through the source color space to the output video encode\.  
*Required*: No  
*Type*: [ColorSpacePassthroughSettings](aws-properties-medialive-channel-colorspacepassthroughsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Hdr10Settings`  <a name="cfn-medialive-channel-h265colorspacesettings-hdr10settings"></a>
Include this element if you want to convert the color space to HDR10 in the output video encode\.  
*Required*: No  
*Type*: [Hdr10Settings](aws-properties-medialive-channel-hdr10settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rec601Settings`  <a name="cfn-medialive-channel-h265colorspacesettings-rec601settings"></a>
Include this element if you want to convert the color space to Rec 601 in the output video encode\.  
*Required*: No  
*Type*: [Rec601Settings](aws-properties-medialive-channel-rec601settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rec709Settings`  <a name="cfn-medialive-channel-h265colorspacesettings-rec709settings"></a>
Include this element if you want to convert the color space to Rec 709 in the output video encode\.  
*Required*: No  
*Type*: [Rec709Settings](aws-properties-medialive-channel-rec709settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)