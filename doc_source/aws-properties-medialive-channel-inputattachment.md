# AWS::MediaLive::Channel InputAttachment<a name="aws-properties-medialive-channel-inputattachment"></a>

An input to attach to this channel\.

This entity is at the top level in the channel\.

## Syntax<a name="aws-properties-medialive-channel-inputattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputattachment-syntax.json"></a>

```
{
  "[AutomaticInputFailoverSettings](#cfn-medialive-channel-inputattachment-automaticinputfailoversettings)" : AutomaticInputFailoverSettings,
  "[InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname)" : String,
  "[InputId](#cfn-medialive-channel-inputattachment-inputid)" : String,
  "[InputSettings](#cfn-medialive-channel-inputattachment-inputsettings)" : InputSettings
}
```

### YAML<a name="aws-properties-medialive-channel-inputattachment-syntax.yaml"></a>

```
  [AutomaticInputFailoverSettings](#cfn-medialive-channel-inputattachment-automaticinputfailoversettings): 
    AutomaticInputFailoverSettings
  [InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname): String
  [InputId](#cfn-medialive-channel-inputattachment-inputid): String
  [InputSettings](#cfn-medialive-channel-inputattachment-inputsettings): 
    InputSettings
```

## Properties<a name="aws-properties-medialive-channel-inputattachment-properties"></a>

`AutomaticInputFailoverSettings`  <a name="cfn-medialive-channel-inputattachment-automaticinputfailoversettings"></a>
User\-specified settings for defining what the conditions are for declaring the input unhealthy and failing over to a different input\.  
*Required*: No  
*Type*: [AutomaticInputFailoverSettings](aws-properties-medialive-channel-automaticinputfailoversettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputAttachmentName`  <a name="cfn-medialive-channel-inputattachment-inputattachmentname"></a>
A name for the attachment\. This is required if you want to use this input in an input switch action\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputId`  <a name="cfn-medialive-channel-inputattachment-inputid"></a>
The ID of the input to attach\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputSettings`  <a name="cfn-medialive-channel-inputattachment-inputsettings"></a>
Information about the content to extract from the input and about the general handling of the content\.  
*Required*: No  
*Type*: [InputSettings](aws-properties-medialive-channel-inputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)