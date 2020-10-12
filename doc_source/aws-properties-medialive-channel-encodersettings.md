# AWS::MediaLive::Channel EncoderSettings<a name="aws-properties-medialive-channel-encodersettings"></a>

This element contains information about all the output encodes \(video, audio, captions\), and about several channel\-wide features\. This element is a top\-level element in the channel\.

## Syntax<a name="aws-properties-medialive-channel-encodersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-encodersettings-syntax.json"></a>

```
{
  "[AudioDescriptions](#cfn-medialive-channel-encodersettings-audiodescriptions)" : [ AudioDescription, ... ],
  "[AvailBlanking](#cfn-medialive-channel-encodersettings-availblanking)" : AvailBlanking,
  "[AvailConfiguration](#cfn-medialive-channel-encodersettings-availconfiguration)" : AvailConfiguration,
  "[BlackoutSlate](#cfn-medialive-channel-encodersettings-blackoutslate)" : BlackoutSlate,
  "[CaptionDescriptions](#cfn-medialive-channel-encodersettings-captiondescriptions)" : [ CaptionDescription, ... ],
  "[FeatureActivations](#cfn-medialive-channel-encodersettings-featureactivations)" : FeatureActivations,
  "[GlobalConfiguration](#cfn-medialive-channel-encodersettings-globalconfiguration)" : GlobalConfiguration,
  "[NielsenConfiguration](#cfn-medialive-channel-encodersettings-nielsenconfiguration)" : NielsenConfiguration,
  "[OutputGroups](#cfn-medialive-channel-encodersettings-outputgroups)" : [ OutputGroup, ... ],
  "[TimecodeConfig](#cfn-medialive-channel-encodersettings-timecodeconfig)" : TimecodeConfig,
  "[VideoDescriptions](#cfn-medialive-channel-encodersettings-videodescriptions)" : [ VideoDescription, ... ]
}
```

### YAML<a name="aws-properties-medialive-channel-encodersettings-syntax.yaml"></a>

```
  [AudioDescriptions](#cfn-medialive-channel-encodersettings-audiodescriptions): 
    - AudioDescription
  [AvailBlanking](#cfn-medialive-channel-encodersettings-availblanking): 
    AvailBlanking
  [AvailConfiguration](#cfn-medialive-channel-encodersettings-availconfiguration): 
    AvailConfiguration
  [BlackoutSlate](#cfn-medialive-channel-encodersettings-blackoutslate): 
    BlackoutSlate
  [CaptionDescriptions](#cfn-medialive-channel-encodersettings-captiondescriptions): 
    - CaptionDescription
  [FeatureActivations](#cfn-medialive-channel-encodersettings-featureactivations): 
    FeatureActivations
  [GlobalConfiguration](#cfn-medialive-channel-encodersettings-globalconfiguration): 
    GlobalConfiguration
  [NielsenConfiguration](#cfn-medialive-channel-encodersettings-nielsenconfiguration): 
    NielsenConfiguration
  [OutputGroups](#cfn-medialive-channel-encodersettings-outputgroups): 
    - OutputGroup
  [TimecodeConfig](#cfn-medialive-channel-encodersettings-timecodeconfig): 
    TimecodeConfig
  [VideoDescriptions](#cfn-medialive-channel-encodersettings-videodescriptions): 
    - VideoDescription
```

## Properties<a name="aws-properties-medialive-channel-encodersettings-properties"></a>

`AudioDescriptions`  <a name="cfn-medialive-channel-encodersettings-audiodescriptions"></a>
Required if at least one output in the channel has at least one audio encode\. The list of all the audioDescriptions in all the outputs in this channel\.  
*Required*: No  
*Type*: List of [AudioDescription](aws-properties-medialive-channel-audiodescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailBlanking`  <a name="cfn-medialive-channel-encodersettings-availblanking"></a>
Settings for ad avail blanking\.  
*Required*: No  
*Type*: [AvailBlanking](aws-properties-medialive-channel-availblanking.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailConfiguration`  <a name="cfn-medialive-channel-encodersettings-availconfiguration"></a>
Include this element once in each channel, only if you want to configure the SCTE\-35 message processing feature in the channel\.  
*Required*: No  
*Type*: [AvailConfiguration](aws-properties-medialive-channel-availconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlackoutSlate`  <a name="cfn-medialive-channel-encodersettings-blackoutslate"></a>
Include this element once in each channel, only if you want to enable the blackout feature of SCTE\-35 message processing\.  
*Required*: No  
*Type*: [BlackoutSlate](aws-properties-medialive-channel-blackoutslate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionDescriptions`  <a name="cfn-medialive-channel-encodersettings-captiondescriptions"></a>
Required if at least one output in the channel has at least one captions encode\. The list of all the captionDescriptions in all the outputs in this channel\.  
*Required*: No  
*Type*: List of [CaptionDescription](aws-properties-medialive-channel-captiondescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FeatureActivations`  <a name="cfn-medialive-channel-encodersettings-featureactivations"></a>
Include this element only if you want to enable any of the features that must be explicitly enabled in the channel\.  
*Required*: No  
*Type*: [FeatureActivations](aws-properties-medialive-channel-featureactivations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalConfiguration`  <a name="cfn-medialive-channel-encodersettings-globalconfiguration"></a>
This element is optional\. Include it if you want to change any default behavior\. This element includes fields that apply to all the inputs, and fields for customizing the input loss behavior feature and output locking feature\.  
*Required*: No  
*Type*: [GlobalConfiguration](aws-properties-medialive-channel-globalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenConfiguration`  <a name="cfn-medialive-channel-encodersettings-nielsenconfiguration"></a>
Include this element once in each channel, if you want to configure for Nielsen watermark handling\.  
*Required*: No  
*Type*: [NielsenConfiguration](aws-properties-medialive-channel-nielsenconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputGroups`  <a name="cfn-medialive-channel-encodersettings-outputgroups"></a>
The list of all output groups in the Configuration information for one output group in thechannel\.  
*Required*: No  
*Type*: List of [OutputGroup](aws-properties-medialive-channel-outputgroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimecodeConfig`  <a name="cfn-medialive-channel-encodersettings-timecodeconfig"></a>
Include this element once in each channel, if you want to configure to include timecode metadata in the outputs\.  
*Required*: No  
*Type*: [TimecodeConfig](aws-properties-medialive-channel-timecodeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoDescriptions`  <a name="cfn-medialive-channel-encodersettings-videodescriptions"></a>
Required because every output group must include video\. The list of all the videoDescriptions in all the outputs in this channel\.  
*Required*: No  
*Type*: List of [VideoDescription](aws-properties-medialive-channel-videodescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)