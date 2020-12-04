# AWS::MediaLive::Channel RtmpGroupSettings<a name="aws-properties-medialive-channel-rtmpgroupsettings"></a>

Rtmp Group Settings

## Syntax<a name="aws-properties-medialive-channel-rtmpgroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-rtmpgroupsettings-syntax.json"></a>

```
{
  "[AuthenticationScheme](#cfn-medialive-channel-rtmpgroupsettings-authenticationscheme)" : String,
  "[CacheFullBehavior](#cfn-medialive-channel-rtmpgroupsettings-cachefullbehavior)" : String,
  "[CacheLength](#cfn-medialive-channel-rtmpgroupsettings-cachelength)" : Integer,
  "[CaptionData](#cfn-medialive-channel-rtmpgroupsettings-captiondata)" : String,
  "[InputLossAction](#cfn-medialive-channel-rtmpgroupsettings-inputlossaction)" : String,
  "[RestartDelay](#cfn-medialive-channel-rtmpgroupsettings-restartdelay)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-rtmpgroupsettings-syntax.yaml"></a>

```
  [AuthenticationScheme](#cfn-medialive-channel-rtmpgroupsettings-authenticationscheme): String
  [CacheFullBehavior](#cfn-medialive-channel-rtmpgroupsettings-cachefullbehavior): String
  [CacheLength](#cfn-medialive-channel-rtmpgroupsettings-cachelength): Integer
  [CaptionData](#cfn-medialive-channel-rtmpgroupsettings-captiondata): String
  [InputLossAction](#cfn-medialive-channel-rtmpgroupsettings-inputlossaction): String
  [RestartDelay](#cfn-medialive-channel-rtmpgroupsettings-restartdelay): Integer
```

## Properties<a name="aws-properties-medialive-channel-rtmpgroupsettings-properties"></a>

`AuthenticationScheme`  <a name="cfn-medialive-channel-rtmpgroupsettings-authenticationscheme"></a>
Authentication scheme to use when connecting with CDN  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheFullBehavior`  <a name="cfn-medialive-channel-rtmpgroupsettings-cachefullbehavior"></a>
Controls behavior when content cache fills up\. If remote origin server stalls the RTMP connection and does not accept content fast enough the 'Media Cache' will fill up\. When the cache reaches the duration specified by cacheLength the cache will stop accepting new content\. If set to disconnectImmediately, the RTMP output will force a disconnect\. Clear the media cache, and reconnect after restartDelay seconds\. If set to waitForServer, the RTMP output will wait up to 5 minutes to allow the origin server to begin accepting data again\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheLength`  <a name="cfn-medialive-channel-rtmpgroupsettings-cachelength"></a>
Cache length, in seconds, is used to calculate buffer size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionData`  <a name="cfn-medialive-channel-rtmpgroupsettings-captiondata"></a>
Controls the types of data that passes to onCaptionInfo outputs\. If set to 'all' then 608 and 708 carried DTVCC data will be passed\. If set to 'field1AndField2608' then DTVCC data will be stripped out, but 608 data from both fields will be passed\. If set to 'field1608' then only the data carried in 608 from field 1 video will be passed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossAction`  <a name="cfn-medialive-channel-rtmpgroupsettings-inputlossaction"></a>
Controls the behavior of this RTMP group if input becomes unavailable\. \- emitOutput: Emit a slate until input returns\. \- pauseOutput: Stop transmitting data until input returns\. This does not close the underlying RTMP connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-rtmpgroupsettings-restartdelay"></a>
If a streaming output fails, number of seconds to wait until a restart is initiated\. A value of 0 means never restart\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)