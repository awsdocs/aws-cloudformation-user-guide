# AWS::IVS::Channel<a name="aws-resource-ivs-channel"></a>

The `AWS::IVS::Channel` resource creates a new channel\. An Amazon IVS channel stores configuration information related to your live stream\. For more information see [CreateChannel](https://docs.aws.amazon.com/ivs/latest/APIReference/API_CreateChannel.html) in the *Amazon Interactive Video Service API Reference*\.

**Note**  
 By default, the IVS API CreateChannel endpoint creates a stream key in addition to a channel\. The Amazon IVS Channel resource *does not* create a stream key; to create a stream key, use the StreamKey resource instead\.

## Syntax<a name="aws-resource-ivs-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ivs-channel-syntax.json"></a>

```
{
  "Type" : "AWS::IVS::Channel",
  "Properties" : {
      "[Authorized](#cfn-ivs-channel-authorized)" : Boolean,
      "[LatencyMode](#cfn-ivs-channel-latencymode)" : String,
      "[Name](#cfn-ivs-channel-name)" : String,
      "[Tags](#cfn-ivs-channel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-ivs-channel-type)" : String
    }
}
```

### YAML<a name="aws-resource-ivs-channel-syntax.yaml"></a>

```
Type: AWS::IVS::Channel
Properties: 
  [Authorized](#cfn-ivs-channel-authorized): Boolean
  [LatencyMode](#cfn-ivs-channel-latencymode): String
  [Name](#cfn-ivs-channel-name): String
  [Tags](#cfn-ivs-channel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-ivs-channel-type): String
```

## Properties<a name="aws-resource-ivs-channel-properties"></a>

`Authorized`  <a name="cfn-ivs-channel-authorized"></a>
Whether the channel is authorized\.  
*Default*: `false`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LatencyMode`  <a name="cfn-ivs-channel-latencymode"></a>
Channel latency mode\. Valid values:  
+  `NORMAL`: Use NORMAL to broadcast and deliver live video up to Full HD\.
+  `LOW`: Use LOW for near real\-time interactions with viewers\.
In the Amazon IVS console, `LOW` and `NORMAL` correspond to `Ultra-low` and `Standard`, respectively\.
*Default*: `LOW`  
*Required*: No  
*Type*: String  
*Allowed values*: `LOW | NORMAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ivs-channel-name"></a>
Channel name\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ivs-channel-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-ivs-channel-type"></a>
The channel type, which determines the allowable resolution and bitrate\. *If you exceed the allowable resolution or bitrate, the stream probably will disconnect immediately\.* Valid values:  
+  `STANDARD`: Multiple qualities are generated from the original input, to automatically give viewers the best experience for their devices and network conditions\. Vertical resolution can be up to 1080 and bitrate can be up to 8\.5 Mbps\.
+  `BASIC`: delivers the original input to viewers\. The viewer’s video\-quality choice is limited to the original input\. Vertical resolution can be up to 480 and bitrate can be up to 1\.5 Mbps\.
*Default*: `STANDARD`  
*Required*: No  
*Type*: String  
*Allowed values*: `BASIC | STANDARD`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ivs-channel-return-values"></a>

### Ref<a name="aws-resource-ivs-channel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the channel ARN\. For example:

 `{ "Ref": "myChannel" }` 

For the Amazon IVS channel `myChannel`, Ref returns the channel ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ivs-channel-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ivs-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The channel ARN\. For example: `arn:aws:ivs:us-west-2:123456789012:channel/abcdABCDefgh`

`IngestEndpoint`  <a name="IngestEndpoint-fn::getatt"></a>
Channel ingest endpoint, part of the definition of an ingest server, used when you set up streaming software\.  
For example: `a1b2c3d4e5f6.global-contribute.live-video.net`

`PlaybackUrl`  <a name="PlaybackUrl-fn::getatt"></a>
Channel playback URL\. For example: `https://a1b2c3d4e5f6.us-west-2.playback.live-video.net/api/video/v1/us-west-2.123456789012.channel.abcdEFGH.m3u8`

## Examples<a name="aws-resource-ivs-channel--examples"></a>



### Channel and Stream Key Template Examples<a name="aws-resource-ivs-channel--examples--Channel_and_Stream_Key_Template_Examples"></a>

The following examples create an Amazon IVS channel and stream key\.

#### JSON<a name="aws-resource-ivs-channel--examples--Channel_and_Stream_Key_Template_Examples--json"></a>

```
{
     "AWSTemplateFormatVersion": "2010-09-09",
     "Resources": {
         "Channel": {
             "Type": "AWS::IVS::Channel",
             "Properties": {
                 "Name": "MyChannel",
                 "Tags": [
                     {
                         "Key": "MyKey",
                         "Value": "MyValue"
                     }
                 ]
             }
         },
         "StreamKey": {
             "Type": "AWS::IVS::StreamKey",
             "Properties": {
                 "ChannelArn": {"Ref": "Channel"},
                 "Tags": [
                     {
                         "Key": "MyKey",
                         "Value": "MyValue"
                     }
                 ]
             }
         }
     },
     "Outputs": {
         "ChannelArn": {
             "Value": {"Ref": "Channel"}
         },
         "ChannelIngestEndpoint": {
             "Value": {
                 "Fn::GetAtt": [
                     "Channel",
                     "IngestEndpoint"
                 ]
             }
         },
         "ChannelPlaybackUrl": {
             "Value": {
                 "Fn::GetAtt": [
                     "Channel",
                     "PlaybackUrl"
                 ]
             }
         },
         "StreamKeyArn": {
             "Value": {"Ref": "StreamKey"}
         }
     }
 }
```

#### YAML<a name="aws-resource-ivs-channel--examples--Channel_and_Stream_Key_Template_Examples--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
 Resources:
   Channel:
     Type: AWS::IVS::Channel
     Properties:
       Name: MyChannel
       Tags:
         - Key: MyKey
           Value: MyValue
   StreamKey:
     Type: AWS::IVS::StreamKey
     Properties:
       ChannelArn: !Ref Channel
       Tags:
         - Key: MyKey
           Value: MyValue
 Outputs:
   ChannelArn:
     Value: !Ref Channel
   ChannelIngestEndpoint:
     Value: !GetAtt Channel.IngestEndpoint
   ChannelPlaybackUrl:
     Value: !GetAtt Channel.PlaybackUrl
   StreamKeyArn:
     Value: !Ref StreamKey
```

## See also<a name="aws-resource-ivs-channel--seealso"></a>
+ [Getting Started with Amazon Interactive Video Service](https://docs.aws.amazon.com/ivs/latest/userguide/GSIVS.html)
+ [Channel](https://docs.aws.amazon.com/ivs/latest/APIReference/API_Channel.html) data type
+ [CreateChannel](https://docs.aws.amazon.com/ivs/latest/APIReference/API_CreateChannel.html) API endpoint