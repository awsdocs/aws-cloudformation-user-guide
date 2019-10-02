# AWS::MediaLive::Channel InputAttachment<a name="aws-properties-medialive-channel-inputattachment"></a>

An input to attach to this channel\.

This entity is at the top level in the channel\.

## Syntax<a name="aws-properties-medialive-channel-inputattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputattachment-syntax.json"></a>

```
{
  "[InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname)" : String,
  "[InputId](#cfn-medialive-channel-inputattachment-inputid)" : String,
  "[InputSettings](#cfn-medialive-channel-inputattachment-inputsettings)" : [InputSettings](aws-properties-medialive-channel-inputsettings.md)
}
```

### YAML<a name="aws-properties-medialive-channel-inputattachment-syntax.yaml"></a>

```
  [InputAttachmentName](#cfn-medialive-channel-inputattachment-inputattachmentname): String
  [InputId](#cfn-medialive-channel-inputattachment-inputid): String
  [InputSettings](#cfn-medialive-channel-inputattachment-inputsettings): 
    [InputSettings](aws-properties-medialive-channel-inputsettings.md)
```

## Properties<a name="aws-properties-medialive-channel-inputattachment-properties"></a>

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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `sa-east-1`
- `us-east-1`
- `us-west-2`
