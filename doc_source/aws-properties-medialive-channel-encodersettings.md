# AWS::MediaLive::Channel EncoderSettings<a name="aws-properties-medialive-channel-encodersettings"></a>

The settings for the encoding of outputs\.

This entity is at the top level in the channel\.

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
The encoding information for output audio\.  
*Required*: No  
*Type*: List of [AudioDescription](aws-properties-medialive-channel-audiodescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailBlanking`  <a name="cfn-medialive-channel-encodersettings-availblanking"></a>
The settings for ad avail blanking\.  
*Required*: No  
*Type*: [AvailBlanking](aws-properties-medialive-channel-availblanking.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailConfiguration`  <a name="cfn-medialive-channel-encodersettings-availconfiguration"></a>
The configuration settings for the ad avail handling\.  
*Required*: No  
*Type*: [AvailConfiguration](aws-properties-medialive-channel-availconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlackoutSlate`  <a name="cfn-medialive-channel-encodersettings-blackoutslate"></a>
The settings for the blackout slate\.  
*Required*: No  
*Type*: [BlackoutSlate](aws-properties-medialive-channel-blackoutslate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionDescriptions`  <a name="cfn-medialive-channel-encodersettings-captiondescriptions"></a>
The encoding information for output captions\.  
*Required*: No  
*Type*: List of [CaptionDescription](aws-properties-medialive-channel-captiondescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FeatureActivations`  <a name="cfn-medialive-channel-encodersettings-featureactivations"></a>
Feature Activations  
*Required*: No  
*Type*: [FeatureActivations](aws-properties-medialive-channel-featureactivations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalConfiguration`  <a name="cfn-medialive-channel-encodersettings-globalconfiguration"></a>
The configuration settings that apply to the entire channel\.  
*Required*: No  
*Type*: [GlobalConfiguration](aws-properties-medialive-channel-globalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenConfiguration`  <a name="cfn-medialive-channel-encodersettings-nielsenconfiguration"></a>
Nielsen configuration settings\.  
*Required*: No  
*Type*: [NielsenConfiguration](aws-properties-medialive-channel-nielsenconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputGroups`  <a name="cfn-medialive-channel-encodersettings-outputgroups"></a>
The settings for the output groups in the channel\.  
*Required*: No  
*Type*: List of [OutputGroup](aws-properties-medialive-channel-outputgroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimecodeConfig`  <a name="cfn-medialive-channel-encodersettings-timecodeconfig"></a>
Contains settings used to acquire and adjust timecode information from the inputs\.  
*Required*: No  
*Type*: [TimecodeConfig](aws-properties-medialive-channel-timecodeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoDescriptions`  <a name="cfn-medialive-channel-encodersettings-videodescriptions"></a>
The encoding information for output videos\.  
*Required*: No  
*Type*: List of [VideoDescription](aws-properties-medialive-channel-videodescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)