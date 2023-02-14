# AWS::MediaLive::Channel OutputGroup<a name="aws-properties-medialive-channel-outputgroup"></a>

The settings for one output group\.

The parent of this entity is EncoderSettings\.

## Syntax<a name="aws-properties-medialive-channel-outputgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-outputgroup-syntax.json"></a>

```
{
  "[Name](#cfn-medialive-channel-outputgroup-name)" : String,
  "[OutputGroupSettings](#cfn-medialive-channel-outputgroup-outputgroupsettings)" : OutputGroupSettings,
  "[Outputs](#cfn-medialive-channel-outputgroup-outputs)" : [ Output, ... ]
}
```

### YAML<a name="aws-properties-medialive-channel-outputgroup-syntax.yaml"></a>

```
  [Name](#cfn-medialive-channel-outputgroup-name): String
  [OutputGroupSettings](#cfn-medialive-channel-outputgroup-outputgroupsettings): 
    OutputGroupSettings
  [Outputs](#cfn-medialive-channel-outputgroup-outputs): 
    - Output
```

## Properties<a name="aws-properties-medialive-channel-outputgroup-properties"></a>

`Name`  <a name="cfn-medialive-channel-outputgroup-name"></a>
A custom output group name that you can optionally define\. Only letters, numbers, and the underscore character are allowed\. The maximum length is 32 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputGroupSettings`  <a name="cfn-medialive-channel-outputgroup-outputgroupsettings"></a>
The settings associated with the output group\.  
*Required*: No  
*Type*: [OutputGroupSettings](aws-properties-medialive-channel-outputgroupsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-medialive-channel-outputgroup-outputs"></a>
The settings for the outputs in the output group\.  
*Required*: No  
*Type*: List of [Output](aws-properties-medialive-channel-output.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)