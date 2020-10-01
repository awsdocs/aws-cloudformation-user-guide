# AWS::MediaLive::Channel AudioLanguageSelection<a name="aws-properties-medialive-channel-audiolanguageselection"></a>

This element specifies the audio by its language ID\. This element belongs to AudioSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-audiolanguageselection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audiolanguageselection-syntax.json"></a>

```
{
  "[LanguageCode](#cfn-medialive-channel-audiolanguageselection-languagecode)" : String,
  "[LanguageSelectionPolicy](#cfn-medialive-channel-audiolanguageselection-languageselectionpolicy)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-audiolanguageselection-syntax.yaml"></a>

```
  [LanguageCode](#cfn-medialive-channel-audiolanguageselection-languagecode): String
  [LanguageSelectionPolicy](#cfn-medialive-channel-audiolanguageselection-languageselectionpolicy): String
```

## Properties<a name="aws-properties-medialive-channel-audiolanguageselection-properties"></a>

`LanguageCode`  <a name="cfn-medialive-channel-audiolanguageselection-languagecode"></a>
Selects a specific three\-letter language code from within an audio source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LanguageSelectionPolicy`  <a name="cfn-medialive-channel-audiolanguageselection-languageselectionpolicy"></a>
Include this element if you want to change the default selection policy\. When set to "strict", the transport stream demux strictly identifies audio streams by their language descriptor\. If a PMT update occurs such that an audio stream matching the initially selected language is no longer present then mute will be encoded until the language returns\. If "loose", then on a PMT update the demux will choose another audio stream in the program with the same stream type if it can't find one with the same language\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)