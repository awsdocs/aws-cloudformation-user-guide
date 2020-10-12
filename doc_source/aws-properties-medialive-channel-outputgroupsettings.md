# AWS::MediaLive::Channel OutputGroupSettings<a name="aws-properties-medialive-channel-outputgroupsettings"></a>

Configures this output group\. In this element, include only one of the 'group settings' child elements\. This element belongs to OutputGroup\.

## Syntax<a name="aws-properties-medialive-channel-outputgroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-outputgroupsettings-syntax.json"></a>

```
{
  "[ArchiveGroupSettings](#cfn-medialive-channel-outputgroupsettings-archivegroupsettings)" : ArchiveGroupSettings,
  "[FrameCaptureGroupSettings](#cfn-medialive-channel-outputgroupsettings-framecapturegroupsettings)" : FrameCaptureGroupSettings,
  "[HlsGroupSettings](#cfn-medialive-channel-outputgroupsettings-hlsgroupsettings)" : HlsGroupSettings,
  "[MediaPackageGroupSettings](#cfn-medialive-channel-outputgroupsettings-mediapackagegroupsettings)" : MediaPackageGroupSettings,
  "[MsSmoothGroupSettings](#cfn-medialive-channel-outputgroupsettings-mssmoothgroupsettings)" : MsSmoothGroupSettings,
  "[MultiplexGroupSettings](#cfn-medialive-channel-outputgroupsettings-multiplexgroupsettings)" : MultiplexGroupSettings,
  "[RtmpGroupSettings](#cfn-medialive-channel-outputgroupsettings-rtmpgroupsettings)" : RtmpGroupSettings,
  "[UdpGroupSettings](#cfn-medialive-channel-outputgroupsettings-udpgroupsettings)" : UdpGroupSettings
}
```

### YAML<a name="aws-properties-medialive-channel-outputgroupsettings-syntax.yaml"></a>

```
  [ArchiveGroupSettings](#cfn-medialive-channel-outputgroupsettings-archivegroupsettings): 
    ArchiveGroupSettings
  [FrameCaptureGroupSettings](#cfn-medialive-channel-outputgroupsettings-framecapturegroupsettings): 
    FrameCaptureGroupSettings
  [HlsGroupSettings](#cfn-medialive-channel-outputgroupsettings-hlsgroupsettings): 
    HlsGroupSettings
  [MediaPackageGroupSettings](#cfn-medialive-channel-outputgroupsettings-mediapackagegroupsettings): 
    MediaPackageGroupSettings
  [MsSmoothGroupSettings](#cfn-medialive-channel-outputgroupsettings-mssmoothgroupsettings): 
    MsSmoothGroupSettings
  [MultiplexGroupSettings](#cfn-medialive-channel-outputgroupsettings-multiplexgroupsettings): 
    MultiplexGroupSettings
  [RtmpGroupSettings](#cfn-medialive-channel-outputgroupsettings-rtmpgroupsettings): 
    RtmpGroupSettings
  [UdpGroupSettings](#cfn-medialive-channel-outputgroupsettings-udpgroupsettings): 
    UdpGroupSettings
```

## Properties<a name="aws-properties-medialive-channel-outputgroupsettings-properties"></a>

`ArchiveGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-archivegroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as an Archive output group\.  
*Required*: No  
*Type*: [ArchiveGroupSettings](aws-properties-medialive-channel-archivegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameCaptureGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-framecapturegroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as a FrameCapture output group\.  
*Required*: No  
*Type*: [FrameCaptureGroupSettings](aws-properties-medialive-channel-framecapturegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-hlsgroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as an HLS output group\.  
*Required*: No  
*Type*: [HlsGroupSettings](aws-properties-medialive-channel-hlsgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaPackageGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-mediapackagegroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as a MediaPackage output group\.  
*Required*: No  
*Type*: [MediaPackageGroupSettings](aws-properties-medialive-channel-mediapackagegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MsSmoothGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-mssmoothgroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as a Microsoft Smooth output group\.  
*Required*: No  
*Type*: [MsSmoothGroupSettings](aws-properties-medialive-channel-mssmoothgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiplexGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-multiplexgroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as a Multiplex output group\.  
*Required*: No  
*Type*: [MultiplexGroupSettings](aws-properties-medialive-channel-multiplexgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RtmpGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-rtmpgroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as an RTMP output group\.  
*Required*: No  
*Type*: [RtmpGroupSettings](aws-properties-medialive-channel-rtmpgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UdpGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-udpgroupsettings"></a>
Include this 'group settings' element if you want to set up this output group as a UDP output group\.  
*Required*: No  
*Type*: [UdpGroupSettings](aws-properties-medialive-channel-udpgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)