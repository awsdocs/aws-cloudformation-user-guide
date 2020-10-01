# AWS::MediaLive::Channel<a name="aws-resource-medialive-channel"></a>

The AWS::MediaLive::Channel resource is a MediaLive resource type that creates a channel\.

A MediaLive channel ingests and transcodes \(decodes and encodes\) source content from the inputs that are attached to that channel, and packages the new content into outputs\. 

## Syntax<a name="aws-resource-medialive-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-medialive-channel-syntax.json"></a>

```
{
  "Type" : "AWS::MediaLive::Channel",
  "Properties" : {
      "[ChannelClass](#cfn-medialive-channel-channelclass)" : String,
      "[Destinations](#cfn-medialive-channel-destinations)" : [ OutputDestination, ... ],
      "[EncoderSettings](#cfn-medialive-channel-encodersettings)" : Json,
      "[InputAttachments](#cfn-medialive-channel-inputattachments)" : [ InputAttachment, ... ],
      "[InputSpecification](#cfn-medialive-channel-inputspecification)" : InputSpecification,
      "[LogLevel](#cfn-medialive-channel-loglevel)" : String,
      "[Name](#cfn-medialive-channel-name)" : String,
      "[RoleArn](#cfn-medialive-channel-rolearn)" : String,
      "[Tags](#cfn-medialive-channel-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-medialive-channel-syntax.yaml"></a>

```
Type: AWS::MediaLive::Channel
Properties: 
  [ChannelClass](#cfn-medialive-channel-channelclass): String
  [Destinations](#cfn-medialive-channel-destinations): 
    - OutputDestination
  [EncoderSettings](#cfn-medialive-channel-encodersettings): Json
  [InputAttachments](#cfn-medialive-channel-inputattachments): 
    - InputAttachment
  [InputSpecification](#cfn-medialive-channel-inputspecification): 
    InputSpecification
  [LogLevel](#cfn-medialive-channel-loglevel): String
  [Name](#cfn-medialive-channel-name): String
  [RoleArn](#cfn-medialive-channel-rolearn): String
  [Tags](#cfn-medialive-channel-tags): Json
```

## Properties<a name="aws-resource-medialive-channel-properties"></a>

`ChannelClass`  <a name="cfn-medialive-channel-channelclass"></a>
The class for this channel\. STANDARD for a channel with two pipelines or SINGLE\_PIPELINE for a channel with one pipeline\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destinations`  <a name="cfn-medialive-channel-destinations"></a>
An ID for this destination information\. Must be unique in the channel\. This ID associates this destination information with its output group\.  
For most output groups, enter a value there, then enter the same value in the destinaton field in the output group\.  
For an RTMP output group or Multiplex output group, enter a value here, then enter the same value in the destination field in the output \(not the output group\)\.  
For a MediaPackage output group, this ID is not used to make this association\.  
*Required*: No  
*Type*: List of [OutputDestination](aws-properties-medialive-channel-outputdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncoderSettings`  <a name="cfn-medialive-channel-encodersettings"></a>
You must include this element once in the channel\. It contains information about all the output encodes \(video, audio, captions\), and about several channel\-wide fetures\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputAttachments`  <a name="cfn-medialive-channel-inputattachments"></a>
You must include this element\. It contains the list of inputs to attach to the channel\. The channel ingests and transcodes these inputs\.  
*Required*: No  
*Type*: List of [InputAttachment](aws-properties-medialive-channel-inputattachment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSpecification`  <a name="cfn-medialive-channel-inputspecification"></a>
Include this element if you want to change the default values for the input specification\.  
*Required*: No  
*Type*: [InputSpecification](aws-properties-medialive-channel-inputspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogLevel`  <a name="cfn-medialive-channel-loglevel"></a>
The log level to write to CloudWatch Logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-name"></a>
Name of channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-medialive-channel-rolearn"></a>
An optional Amazon Resource Name \(ARN\) of the role to assume when running the Channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-medialive-channel-tags"></a>
A collection of key\-value pairs\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-medialive-channel-return-values"></a>

### Ref<a name="aws-resource-medialive-channel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the channel\.

For example: `{ "Ref": "myChannel" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-medialive-channel-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-medialive-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the MediaLive channel\. For example: arn:aws:medialive:us\-west\-1:111122223333:medialive:channel:1234567

`Inputs`  <a name="Inputs-fn::getatt"></a>
The inputs that are attached to this channel\. The inputs are identified by their IDs \(not by their names or their ARNs\)\.