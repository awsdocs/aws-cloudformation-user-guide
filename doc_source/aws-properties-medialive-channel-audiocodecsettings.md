# AWS::MediaLive::Channel AudioCodecSettings<a name="aws-properties-medialive-channel-audiocodecsettings"></a>

The configuration of the audio codec in the audio output\.

The parent of this entity is AudioDescription\.

## Syntax<a name="aws-properties-medialive-channel-audiocodecsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiocodecsettings-syntax.json"></a>

```
{
  "[AacSettings](#cfn-medialive-channel-audiocodecsettings-aacsettings)" : AacSettings,
  "[Ac3Settings](#cfn-medialive-channel-audiocodecsettings-ac3settings)" : Ac3Settings,
  "[Eac3Settings](#cfn-medialive-channel-audiocodecsettings-eac3settings)" : Eac3Settings,
  "[Mp2Settings](#cfn-medialive-channel-audiocodecsettings-mp2settings)" : Mp2Settings,
  "[PassThroughSettings](#cfn-medialive-channel-audiocodecsettings-passthroughsettings)" : PassThroughSettings
}
```

### YAML<a name="aws-properties-medialive-channel-audiocodecsettings-syntax.yaml"></a>

```
  [AacSettings](#cfn-medialive-channel-audiocodecsettings-aacsettings): 
    AacSettings
  [Ac3Settings](#cfn-medialive-channel-audiocodecsettings-ac3settings): 
    Ac3Settings
  [Eac3Settings](#cfn-medialive-channel-audiocodecsettings-eac3settings): 
    Eac3Settings
  [Mp2Settings](#cfn-medialive-channel-audiocodecsettings-mp2settings): 
    Mp2Settings
  [PassThroughSettings](#cfn-medialive-channel-audiocodecsettings-passthroughsettings): 
    PassThroughSettings
```

## Properties<a name="aws-properties-medialive-channel-audiocodecsettings-properties"></a>

`AacSettings`  <a name="cfn-medialive-channel-audiocodecsettings-aacsettings"></a>
The setup of the AAC audio codec in the output\.  
*Required*: No  
*Type*: [AacSettings](aws-properties-medialive-channel-aacsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ac3Settings`  <a name="cfn-medialive-channel-audiocodecsettings-ac3settings"></a>
The setup of an AC3 audio codec in the output\.  
*Required*: No  
*Type*: [Ac3Settings](aws-properties-medialive-channel-ac3settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Eac3Settings`  <a name="cfn-medialive-channel-audiocodecsettings-eac3settings"></a>
The setup of an EAC3 audio codec in the output\.  
*Required*: No  
*Type*: [Eac3Settings](aws-properties-medialive-channel-eac3settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mp2Settings`  <a name="cfn-medialive-channel-audiocodecsettings-mp2settings"></a>
The setup of an MP2 audio codec in the output\.  
*Required*: No  
*Type*: [Mp2Settings](aws-properties-medialive-channel-mp2settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PassThroughSettings`  <a name="cfn-medialive-channel-audiocodecsettings-passthroughsettings"></a>
The setup to pass through the Dolby audio codec to the output\.  
*Required*: No  
*Type*: [PassThroughSettings](aws-properties-medialive-channel-passthroughsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)