# AWS::MediaLive::Channel HlsAkamaiSettings<a name="aws-properties-medialive-channel-hlsakamaisettings"></a>

The Akamai settings in an HLS output\.

The parent of this entity is HlsCdnSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlsakamaisettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsakamaisettings-syntax.json"></a>

```
{
  "[ConnectionRetryInterval](#cfn-medialive-channel-hlsakamaisettings-connectionretryinterval)" : Integer,
  "[FilecacheDuration](#cfn-medialive-channel-hlsakamaisettings-filecacheduration)" : Integer,
  "[HttpTransferMode](#cfn-medialive-channel-hlsakamaisettings-httptransfermode)" : String,
  "[NumRetries](#cfn-medialive-channel-hlsakamaisettings-numretries)" : Integer,
  "[RestartDelay](#cfn-medialive-channel-hlsakamaisettings-restartdelay)" : Integer,
  "[Salt](#cfn-medialive-channel-hlsakamaisettings-salt)" : String,
  "[Token](#cfn-medialive-channel-hlsakamaisettings-token)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-hlsakamaisettings-syntax.yaml"></a>

```
  [ConnectionRetryInterval](#cfn-medialive-channel-hlsakamaisettings-connectionretryinterval): Integer
  [FilecacheDuration](#cfn-medialive-channel-hlsakamaisettings-filecacheduration): Integer
  [HttpTransferMode](#cfn-medialive-channel-hlsakamaisettings-httptransfermode): String
  [NumRetries](#cfn-medialive-channel-hlsakamaisettings-numretries): Integer
  [RestartDelay](#cfn-medialive-channel-hlsakamaisettings-restartdelay): Integer
  [Salt](#cfn-medialive-channel-hlsakamaisettings-salt): String
  [Token](#cfn-medialive-channel-hlsakamaisettings-token): String
```

## Properties<a name="aws-properties-medialive-channel-hlsakamaisettings-properties"></a>

`ConnectionRetryInterval`  <a name="cfn-medialive-channel-hlsakamaisettings-connectionretryinterval"></a>
The number of seconds to wait before retrying a connection to the CDN if the connection is lost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilecacheDuration`  <a name="cfn-medialive-channel-hlsakamaisettings-filecacheduration"></a>
The size, in seconds, of the file cache for streaming outputs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpTransferMode`  <a name="cfn-medialive-channel-hlsakamaisettings-httptransfermode"></a>
Specifies whether to use chunked transfer encoding to Akamai\. To enable this feature, contact Akamai\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRetries`  <a name="cfn-medialive-channel-hlsakamaisettings-numretries"></a>
The number of retry attempts that will be made before the channel is put into an error state\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestartDelay`  <a name="cfn-medialive-channel-hlsakamaisettings-restartdelay"></a>
If a streaming output fails, the number of seconds to wait until a restart is initiated\. A value of 0 means never restart\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salt`  <a name="cfn-medialive-channel-hlsakamaisettings-salt"></a>
The salt for authenticated Akamai\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Token`  <a name="cfn-medialive-channel-hlsakamaisettings-token"></a>
The token parameter for authenticated Akamai\. If this is not specified, \_gda\_ is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)