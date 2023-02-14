# AWS::MediaLive::Channel HlsInputSettings<a name="aws-properties-medialive-channel-hlsinputsettings"></a>

Information about how to connect to the upstream system\.

The parent of this entity is NetworkInputSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlsinputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsinputsettings-syntax.json"></a>

```
{
  "[Bandwidth](#cfn-medialive-channel-hlsinputsettings-bandwidth)" : Integer,
  "[BufferSegments](#cfn-medialive-channel-hlsinputsettings-buffersegments)" : Integer,
  "[Retries](#cfn-medialive-channel-hlsinputsettings-retries)" : Integer,
  "[RetryInterval](#cfn-medialive-channel-hlsinputsettings-retryinterval)" : Integer,
  "[Scte35Source](#cfn-medialive-channel-hlsinputsettings-scte35source)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-hlsinputsettings-syntax.yaml"></a>

```
  [Bandwidth](#cfn-medialive-channel-hlsinputsettings-bandwidth): Integer
  [BufferSegments](#cfn-medialive-channel-hlsinputsettings-buffersegments): Integer
  [Retries](#cfn-medialive-channel-hlsinputsettings-retries): Integer
  [RetryInterval](#cfn-medialive-channel-hlsinputsettings-retryinterval): Integer
  [Scte35Source](#cfn-medialive-channel-hlsinputsettings-scte35source): String
```

## Properties<a name="aws-properties-medialive-channel-hlsinputsettings-properties"></a>

`Bandwidth`  <a name="cfn-medialive-channel-hlsinputsettings-bandwidth"></a>
When specified, the HLS stream with the m3u8 bandwidth that most closely matches this value is chosen\. Otherwise, the highest bandwidth stream in the m3u8 is chosen\. The bitrate is specified in bits per second, as in an HLS manifest\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BufferSegments`  <a name="cfn-medialive-channel-hlsinputsettings-buffersegments"></a>
When specified, reading of the HLS input begins this many buffer segments from the end \(most recently written segment\)\. When not specified, the HLS input begins with the first segment specified in the m3u8\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Retries`  <a name="cfn-medialive-channel-hlsinputsettings-retries"></a>
The number of consecutive times that attempts to read a manifest or segment must fail before the input is considered unavailable\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryInterval`  <a name="cfn-medialive-channel-hlsinputsettings-retryinterval"></a>
The number of seconds between retries when an attempt to read a manifest or segment fails\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35Source`  <a name="cfn-medialive-channel-hlsinputsettings-scte35source"></a>
Identifies the source for the SCTE\-35 messages that MediaLive will ingest\. Messages can be ingested from the content segments \(in the stream\) or from tags in the playlist \(the HLS manifest\)\. MediaLive ignores SCTE\-35 information in the source that is not selected\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)