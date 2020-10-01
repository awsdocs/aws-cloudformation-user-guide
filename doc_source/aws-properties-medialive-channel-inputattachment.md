# AWS::MediaLive::Channel InputAttachment<a name="aws-properties-medialive-channel-inputattachment"></a>

 Contains information to associate one input with this channel\. An array of these elements is in the top\-level of the channel\.

## Syntax<a name="aws-properties-medialive-channel-inputattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputattachment-syntax.json"></a>

```
{
  "[InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname)" : String,
  "[InputId](#cfn-medialive-channel-inputattachment-inputid)" : String,
  "[InputSettings](#cfn-medialive-channel-inputattachment-inputsettings)" : InputSettings
}
```

### YAML<a name="aws-properties-medialive-channel-inputattachment-syntax.yaml"></a>

```
  [InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname): String
  [InputId](#cfn-medialive-channel-inputattachment-inputid): String
  [InputSettings](#cfn-medialive-channel-inputattachment-inputsettings): 
    InputSettings
```

## Properties<a name="aws-properties-medialive-channel-inputattachment-properties"></a>

`InputAttachmentName`  <a name="cfn-medialive-channel-inputattachment-inputattachmentname"></a>
User\-specified name for the attachment\. This is required if the user wants to use this input in an input switch action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputId`  <a name="cfn-medialive-channel-inputattachment-inputid"></a>
The ID of the input\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputSettings`  <a name="cfn-medialive-channel-inputattachment-inputsettings"></a>
Include this element in order to identify the video, audio and captions to extract from the input, and to customize some of the handling of the input\.  
*Required*: No  
*Type*: [InputSettings](aws-properties-medialive-channel-inputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)