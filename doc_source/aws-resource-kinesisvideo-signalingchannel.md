# AWS::KinesisVideo::SignalingChannel<a name="aws-resource-kinesisvideo-signalingchannel"></a>

Specifies a signaling channel\.

 `CreateSignalingChannel` is an asynchronous operation\.

## Syntax<a name="aws-resource-kinesisvideo-signalingchannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisvideo-signalingchannel-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisVideo::SignalingChannel",
  "Properties" : {
      "[MessageTtlSeconds](#cfn-kinesisvideo-signalingchannel-messagettlseconds)" : Integer,
      "[Name](#cfn-kinesisvideo-signalingchannel-name)" : String,
      "[Tags](#cfn-kinesisvideo-signalingchannel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-kinesisvideo-signalingchannel-type)" : String
    }
}
```

### YAML<a name="aws-resource-kinesisvideo-signalingchannel-syntax.yaml"></a>

```
Type: AWS::KinesisVideo::SignalingChannel
Properties: 
  [MessageTtlSeconds](#cfn-kinesisvideo-signalingchannel-messagettlseconds): Integer
  [Name](#cfn-kinesisvideo-signalingchannel-name): String
  [Tags](#cfn-kinesisvideo-signalingchannel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-kinesisvideo-signalingchannel-type): String
```

## Properties<a name="aws-resource-kinesisvideo-signalingchannel-properties"></a>

`MessageTtlSeconds`  <a name="cfn-kinesisvideo-signalingchannel-messagettlseconds"></a>
The period of time a signaling channel retains undelivered messages before they are discarded\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `5`  
*Maximum*: `120`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kinesisvideo-signalingchannel-name"></a>
A name for the signaling channel that you are creating\. It must be unique for each AWS account and AWS Region\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-kinesisvideo-signalingchannel-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-kinesisvideo-signalingchannel-type"></a>
A type of the signaling channel that you are creating\. Currently, `SINGLE_MASTER` is the only supported channel type\.   
*Required*: No  
*Type*: String  
*Allowed values*: `FULL_MESH | SINGLE_MASTER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-kinesisvideo-signalingchannel-return-values"></a>

### Ref<a name="aws-resource-kinesisvideo-signalingchannel-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-kinesisvideo-signalingchannel-return-values-fn--getatt"></a>

#### <a name="aws-resource-kinesisvideo-signalingchannel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the signaling channel\.