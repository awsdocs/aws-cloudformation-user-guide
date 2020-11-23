# AWS::MediaLive::Channel HlsBasicPutSettings<a name="aws-properties-medialive-channel-hlsbasicputsettings"></a>

Configures the connection between MediaLive and the downstream system that is a server that supports HTTP basic PUT\. This element belongs to HlsCdnSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlsbasicputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsbasicputsettings-syntax.json"></a>

```
{
  "[ConnectionRetryInterval](#cfn-medialive-channel-hlsbasicputsettings-connectionretryinterval)" : Integer,
  "[FilecacheDuration](#cfn-medialive-channel-hlsbasicputsettings-filecacheduration)" : Integer,
  "[NumRetries](#cfn-medialive-channel-hlsbasicputsettings-numretries)" : Integer,
  "[RestartDelay](#cfn-medialive-channel-hlsbasicputsettings-restartdelay)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-hlsbasicputsettings-syntax.yaml"></a>

```
  [ConnectionRetryInterval](#cfn-medialive-channel-hlsbasicputsettings-connectionretryinterval): Integer
  [FilecacheDuration](#cfn-medialive-channel-hlsbasicputsettings-filecacheduration): Integer
  [NumRetries](#cfn-medialive-channel-hlsbasicputsettings-numretries): Integer
  [RestartDelay](#cfn-medialive-channel-hlsbasicputsettings-restartdelay): Integer
```

## Properties<a name="aws-properties-medialive-channel-hlsbasicputsettings-properties"></a>

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-hlsbasicputsettings-connectionretryinterval"></a>
Number of seconds to wait before retrying connection to the CDN if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-hlsbasicputsettings-filecacheduration"></a>
Size in seconds of file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-hlsbasicputsettings-numretries"></a>
Number of retry attempts that will be made before the channel is put into an error state\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-hlsbasicputsettings-restartdelay"></a>
If a streaming output fails, number of seconds to wait until a restart is initiated\. A value of 0 means never restart\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)