# AWS::IVS::StreamKey<a name="aws-resource-ivs-streamkey"></a>

The `AWS::IVS::StreamKey` resource creates a stream key for the specified channel\. Use a stream key to initiate a live stream\.

## Syntax<a name="aws-resource-ivs-streamkey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ivs-streamkey-syntax.json"></a>

```
{
  "Type" : "AWS::IVS::StreamKey",
  "Properties" : {
      "[ChannelArn](#cfn-ivs-streamkey-channelarn)" : String,
      "[Tags](#cfn-ivs-streamkey-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ivs-streamkey-syntax.yaml"></a>

```
Type: AWS::IVS::StreamKey
Properties: 
  [ChannelArn](#cfn-ivs-streamkey-channelarn): String
  [Tags](#cfn-ivs-streamkey-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ivs-streamkey-properties"></a>

`ChannelArn`  <a name="cfn-ivs-streamkey-channelarn"></a>
Channel ARN for the stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^arn:aws:[is]vs:[a-z0-9-]+:[0-9]+:channel/[a-zA-Z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ivs-streamkey-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ivs-streamkey-return-values"></a>

### Ref<a name="aws-resource-ivs-streamkey-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\. For example:

 `{ "Ref": "myStreamKey" }` 

For the Amazon IVS stream key `myStreamKey`, Ref returns the stream key ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ivs-streamkey-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ivs-streamkey-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The stream\-key ARN\. For example: `arn:aws:ivs:us-west-2:123456789012:stream-key/g1H2I3j4k5L6`

`Value`  <a name="Value-fn::getatt"></a>
The stream\-key value\. For example: `sk_us-west-2_abcdABCDefgh_567890abcdef`

## Examples<a name="aws-resource-ivs-streamkey--examples"></a>



### Channel and Stream Key Template Examples<a name="aws-resource-ivs-streamkey--examples--Channel_and_Stream_Key_Template_Examples"></a>

The following examples create an Amazon IVS channel and stream key\.

#### JSON<a name="aws-resource-ivs-streamkey--examples--Channel_and_Stream_Key_Template_Examples--json"></a>

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

#### YAML<a name="aws-resource-ivs-streamkey--examples--Channel_and_Stream_Key_Template_Examples--yaml"></a>

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

## See also<a name="aws-resource-ivs-streamkey--seealso"></a>
+ [Getting Started with Amazon Interactive Video Service](https://docs.aws.amazon.com/ivs/latest/userguide/GSIVS.html)
+ [StreamKey](https://docs.aws.amazon.com/ivs/latest/APIReference/API_StreamKey.html) data type
+ [CreateStreamKey](https://docs.aws.amazon.com/ivs/latest/APIReference/API_CreateStreamKey.html) API endpoint