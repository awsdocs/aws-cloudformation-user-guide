# AWS::MediaLive::Channel HlsWebdavSettings<a name="aws-properties-medialive-channel-hlswebdavsettings"></a>

Configures the connection between MediaLive and the downstream system that is a WebDAV server\. This element belongs to HlsCdnSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlswebdavsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlswebdavsettings-syntax.json"></a>

```
{
  "[ConnectionRetryInterval](#cfn-medialive-channel-hlswebdavsettings-connectionretryinterval)" : Integer,
  "[FilecacheDuration](#cfn-medialive-channel-hlswebdavsettings-filecacheduration)" : Integer,
  "[HttpTransferMode](#cfn-medialive-channel-hlswebdavsettings-httptransfermode)" : String,
  "[NumRetries](#cfn-medialive-channel-hlswebdavsettings-numretries)" : Integer,
  "[RestartDelay](#cfn-medialive-channel-hlswebdavsettings-restartdelay)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-hlswebdavsettings-syntax.yaml"></a>

```
  [ConnectionRetryInterval](#cfn-medialive-channel-hlswebdavsettings-connectionretryinterval): Integer
  [FilecacheDuration](#cfn-medialive-channel-hlswebdavsettings-filecacheduration): Integer
  [HttpTransferMode](#cfn-medialive-channel-hlswebdavsettings-httptransfermode): String
  [NumRetries](#cfn-medialive-channel-hlswebdavsettings-numretries): Integer
  [RestartDelay](#cfn-medialive-channel-hlswebdavsettings-restartdelay): Integer
```

## Properties<a name="aws-properties-medialive-channel-hlswebdavsettings-properties"></a>

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-hlswebdavsettings-connectionretryinterval"></a>
Number of seconds to wait before retrying connection to the CDN if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-hlswebdavsettings-filecacheduration"></a>
Size in seconds of file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpTransferMode`  <a name="cfn-medialive-channel-hlswebdavsettings-httptransfermode"></a>
Specify whether or not to use chunked transfer encoding to WebDAV\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-hlswebdavsettings-numretries"></a>
Number of retry attempts that will be made before the channel is put into an error state\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-hlswebdavsettings-restartdelay"></a>
If a streaming output fails, number of seconds to wait until a restart is initiated\. A value of 0 means never restart\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)