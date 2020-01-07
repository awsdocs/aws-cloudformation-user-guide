# AWS::MediaLive::Channel Scte27SourceSettings<a name="aws-properties-medialive-channel-scte27sourcesettings"></a>

Information about the SCTE\-27 captions to extract from the input\.

The parent of this entity is CaptionSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-scte27sourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-scte27sourcesettings-syntax.json"></a>

```
{
  "[Pid](#cfn-medialive-channel-scte27sourcesettings-pid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-scte27sourcesettings-syntax.yaml"></a>

```
  [Pid](#cfn-medialive-channel-scte27sourcesettings-pid): Integer
```

## Properties<a name="aws-properties-medialive-channel-scte27sourcesettings-properties"></a>

`Pid`  <a name="cfn-medialive-channel-scte27sourcesettings-pid"></a>
The PID field is used in conjunction with the captions selector languageCode field as follows: Specify PID and Language: Extracts captions from that PID; the language is "informational\." Specify PID and omit Language: Extracts the specified PID\. Omit PID and specify Language: Extracts the specified language, whichever PID that happens to be\. Omit PID and omit Language: Valid only if source is DVB\-Sub that is being passed through; all languages are passed through\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)