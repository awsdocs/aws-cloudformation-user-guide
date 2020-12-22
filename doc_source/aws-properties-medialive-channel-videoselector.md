# AWS::MediaLive::Channel VideoSelector<a name="aws-properties-medialive-channel-videoselector"></a>

Information about the video to extract from the input\. An input can contain only one video selector\.

The parent of this entity is InputSettings\.

## Syntax<a name="aws-properties-medialive-channel-videoselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoselector-syntax.json"></a>

```
{
  "[ColorSpace](#cfn-medialive-channel-videoselector-colorspace)" : String,
  "[ColorSpaceUsage](#cfn-medialive-channel-videoselector-colorspaceusage)" : String,
  "[SelectorSettings](#cfn-medialive-channel-videoselector-selectorsettings)" : VideoSelectorSettings
}
```

### YAML<a name="aws-properties-medialive-channel-videoselector-syntax.yaml"></a>

```
  [ColorSpace](#cfn-medialive-channel-videoselector-colorspace): String
  [ColorSpaceUsage](#cfn-medialive-channel-videoselector-colorspaceusage): String
  [SelectorSettings](#cfn-medialive-channel-videoselector-selectorsettings): 
    VideoSelectorSettings
```

## Properties<a name="aws-properties-medialive-channel-videoselector-properties"></a>

`ColorSpace`  <a name="cfn-medialive-channel-videoselector-colorspace"></a>
Specifies the color space of an input\. This setting works in tandem with colorSpaceConversion to determine if MediaLive will perform any conversion\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorSpaceUsage`  <a name="cfn-medialive-channel-videoselector-colorspaceusage"></a>
Applies only if colorSpace is a value other than Follow\. This field controls how the value in the colorSpace field is used\. Fallback means that when the input does include color space data, that data is used, but when the input has no color space data, the value in colorSpace is used\. Choose fallback if your input is sometimes missing color space data, but when it does have color space data, that data is correct\. Force means to always use the value in colorSpace\. Choose force if your input usually has no color space data or might have unreliable color space data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectorSettings`  <a name="cfn-medialive-channel-videoselector-selectorsettings"></a>
Information about the video to select from the content\.  
*Required*: No  
*Type*: [VideoSelectorSettings](aws-properties-medialive-channel-videoselectorsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)