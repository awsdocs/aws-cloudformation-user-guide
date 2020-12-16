# AWS::MediaLive::Channel HlsMediaStoreSettings<a name="aws-properties-medialive-channel-hlsmediastoresettings"></a>

Hls Media Store Settings

## Syntax<a name="aws-properties-medialive-channel-hlsmediastoresettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsmediastoresettings-syntax.json"></a>

```
{
  "[ConnectionRetryInterval](#cfn-medialive-channel-hlsmediastoresettings-connectionretryinterval)" : Integer,
  "[FilecacheDuration](#cfn-medialive-channel-hlsmediastoresettings-filecacheduration)" : Integer,
  "[MediaStoreStorageClass](#cfn-medialive-channel-hlsmediastoresettings-mediastorestorageclass)" : String,
  "[NumRetries](#cfn-medialive-channel-hlsmediastoresettings-numretries)" : Integer,
  "[RestartDelay](#cfn-medialive-channel-hlsmediastoresettings-restartdelay)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-hlsmediastoresettings-syntax.yaml"></a>

```
  [ConnectionRetryInterval](#cfn-medialive-channel-hlsmediastoresettings-connectionretryinterval): Integer
  [FilecacheDuration](#cfn-medialive-channel-hlsmediastoresettings-filecacheduration): Integer
  [MediaStoreStorageClass](#cfn-medialive-channel-hlsmediastoresettings-mediastorestorageclass): String
  [NumRetries](#cfn-medialive-channel-hlsmediastoresettings-numretries): Integer
  [RestartDelay](#cfn-medialive-channel-hlsmediastoresettings-restartdelay): Integer
```

## Properties<a name="aws-properties-medialive-channel-hlsmediastoresettings-properties"></a>

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-hlsmediastoresettings-connectionretryinterval"></a>
Number of seconds to wait before retrying connection to the CDN if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-hlsmediastoresettings-filecacheduration"></a>
Size in seconds of file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaStoreStorageClass`  <a name="cfn-medialive-channel-hlsmediastoresettings-mediastorestorageclass"></a>
When set to temporal, output files are stored in non\-persistent memory for faster reading and writing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-hlsmediastoresettings-numretries"></a>
Number of retry attempts that will be made before the channel is put into an error state\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-hlsmediastoresettings-restartdelay"></a>
If a streaming output fails, number of seconds to wait until a restart is initiated\. A value of 0 means never restart\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)