# AWS::Pinpoint::VoiceChannel<a name="aws-resource-pinpoint-voicechannel"></a>

A *channel* is a type of platform that you can deliver messages to\. To send a voice message, you send the message through the voice channel\. Before you can use Amazon Pinpoint to send voice messages, you have to enable the voice channel for an Amazon Pinpoint application\.

The AWS::Pinpoint::VoiceChannel resource defines the status and other settings of the voice channel for an application\. 

## Syntax<a name="aws-resource-pinpoint-voicechannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-voicechannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::VoiceChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-voicechannel-applicationid)" : String,
      "[Enabled](#cfn-pinpoint-voicechannel-enabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-pinpoint-voicechannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::VoiceChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-voicechannel-applicationid): String
  [Enabled](#cfn-pinpoint-voicechannel-enabled): Boolean
```

## Properties<a name="aws-resource-pinpoint-voicechannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-voicechannel-applicationid"></a>
The unique identifier for the Amazon Pinpoint application that the voice channel applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-pinpoint-voicechannel-enabled"></a>
Specifies whether to enable the voice channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-voicechannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-voicechannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.