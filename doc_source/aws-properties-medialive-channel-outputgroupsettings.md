# AWS::MediaLive::Channel OutputGroupSettings<a name="aws-properties-medialive-channel-outputgroupsettings"></a>

The configuration of the output group\.

The parent of this entity is OutputGroup\.

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
The configuration of an archive output group\.  
The parent of this entity is OutputGroupSettings\.  
*Required*: No  
*Type*: [ArchiveGroupSettings](aws-properties-medialive-channel-archivegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameCaptureGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-framecapturegroupsettings"></a>
The configuration of a frame capture output group\.  
*Required*: No  
*Type*: [FrameCaptureGroupSettings](aws-properties-medialive-channel-framecapturegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-hlsgroupsettings"></a>
The configuration of an HLS output group\.  
*Required*: No  
*Type*: [HlsGroupSettings](aws-properties-medialive-channel-hlsgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaPackageGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-mediapackagegroupsettings"></a>
The configuration of a MediaPackage output group\.  
*Required*: No  
*Type*: [MediaPackageGroupSettings](aws-properties-medialive-channel-mediapackagegroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MsSmoothGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-mssmoothgroupsettings"></a>
The configuration of a Microsoft Smooth output group\.  
*Required*: No  
*Type*: [MsSmoothGroupSettings](aws-properties-medialive-channel-mssmoothgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiplexGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-multiplexgroupsettings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [MultiplexGroupSettings](aws-properties-medialive-channel-multiplexgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RtmpGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-rtmpgroupsettings"></a>
The configuration of an RTMP output group\.  
*Required*: No  
*Type*: [RtmpGroupSettings](aws-properties-medialive-channel-rtmpgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UdpGroupSettings`  <a name="cfn-medialive-channel-outputgroupsettings-udpgroupsettings"></a>
The configuration of a UDP output group\.  
*Required*: No  
*Type*: [UdpGroupSettings](aws-properties-medialive-channel-udpgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)