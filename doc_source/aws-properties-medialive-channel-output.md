# AWS::MediaLive::Channel Output<a name="aws-properties-medialive-channel-output"></a>

Configuration about one output, including the video encode, audio encode or encodes, and captions encode or encodes\. This element belongs to OutputGroup\.

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
A list of AudioDescriptions to include in this output\. For each item in the list, enter the value that is in the name field of the appropriate AudioDescription\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionDescriptionNames`  <a name="cfn-medialive-channel-output-captiondescriptionnames"></a>
A list of CaptionDescriptions to include in this output\. For each item in the list, enter the value that is in the name field of the appropriate CaptionDescription\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputName`  <a name="cfn-medialive-channel-output-outputname"></a>
The name used to identify an output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSettings`  <a name="cfn-medialive-channel-output-outputsettings"></a>
Identifies and configures the video, audio, and captions encodes to include in the output\.  
*Required*: No  
*Type*: [OutputSettings](aws-properties-medialive-channel-outputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoDescriptionName`  <a name="cfn-medialive-channel-output-videodescriptionname"></a>
The single VideoDescription to include in this output\. Enter the value that is in the name field of the appropriate VideoDescription\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)