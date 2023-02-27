# AWS::MediaLive::Channel Output<a name="aws-properties-medialive-channel-output"></a>

The output settings\. 

The parent of this entity is OutputGroup\.

## Syntax<a name="aws-properties-medialive-channel-output-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-output-syntax.json"></a>

```
{
  "[AudioDescriptionNames](#cfn-medialive-channel-output-audiodescriptionnames)" : [ String, ... ],
  "[CaptionDescriptionNames](#cfn-medialive-channel-output-captiondescriptionnames)" : [ String, ... ],
  "[OutputName](#cfn-medialive-channel-output-outputname)" : String,
  "[OutputSettings](#cfn-medialive-channel-output-outputsettings)" : OutputSettings,
  "[VideoDescriptionName](#cfn-medialive-channel-output-videodescriptionname)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-output-syntax.yaml"></a>

```
  [AudioDescriptionNames](#cfn-medialive-channel-output-audiodescriptionnames): 
    - String
  [CaptionDescriptionNames](#cfn-medialive-channel-output-captiondescriptionnames): 
    - String
  [OutputName](#cfn-medialive-channel-output-outputname): String
  [OutputSettings](#cfn-medialive-channel-output-outputsettings): 
    OutputSettings
  [VideoDescriptionName](#cfn-medialive-channel-output-videodescriptionname): String
```

## Properties<a name="aws-properties-medialive-channel-output-properties"></a>

`AudioDescriptionNames`  <a name="cfn-medialive-channel-output-audiodescriptionnames"></a>
The names of the audio descriptions that are used as audio sources for this output\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionDescriptionNames`  <a name="cfn-medialive-channel-output-captiondescriptionnames"></a>
The names of the caption descriptions that are used as captions sources for this output\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputName`  <a name="cfn-medialive-channel-output-outputname"></a>
The name that is used to identify an output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSettings`  <a name="cfn-medialive-channel-output-outputsettings"></a>
The output type\-specific settings\.  
*Required*: No  
*Type*: [OutputSettings](aws-properties-medialive-channel-outputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoDescriptionName`  <a name="cfn-medialive-channel-output-videodescriptionname"></a>
The name of the VideoDescription that is used as the source for this output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)