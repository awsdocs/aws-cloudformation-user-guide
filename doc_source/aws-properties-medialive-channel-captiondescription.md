# AWS::MediaLive::Channel CaptionDescription<a name="aws-properties-medialive-channel-captiondescription"></a>

The configuration information for an individual output captions encode\. To associate this CaptionDescription with its Output, you enter the same value in the name field of the CaptionDescription and the CaptionDescriptionNames field of the Output\. This element belongs to EncoderSettings\.

## Syntax<a name="aws-properties-medialive-channel-captiondescription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captiondescription-syntax.json"></a>

```
{
  "[CaptionSelectorName](#cfn-medialive-channel-captiondescription-captionselectorname)" : String,
  "[DestinationSettings](#cfn-medialive-channel-captiondescription-destinationsettings)" : CaptionDestinationSettings,
  "[LanguageCode](#cfn-medialive-channel-captiondescription-languagecode)" : String,
  "[LanguageDescription](#cfn-medialive-channel-captiondescription-languagedescription)" : String,
  "[Name](#cfn-medialive-channel-captiondescription-name)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-captiondescription-syntax.yaml"></a>

```
  [CaptionSelectorName](#cfn-medialive-channel-captiondescription-captionselectorname): String
  [DestinationSettings](#cfn-medialive-channel-captiondescription-destinationsettings): 
    CaptionDestinationSettings
  [LanguageCode](#cfn-medialive-channel-captiondescription-languagecode): String
  [LanguageDescription](#cfn-medialive-channel-captiondescription-languagedescription): String
  [Name](#cfn-medialive-channel-captiondescription-name): String
```

## Properties<a name="aws-properties-medialive-channel-captiondescription-properties"></a>

`CaptionSelectorName`  <a name="cfn-medialive-channel-captiondescription-captionselectorname"></a>
Identifies the input captions asset that is the source for this output captions encode\. The input captions asset is one of the CaptionSelectors in the channel\. In this captionSelectorName field, enter the value from the name field of that CaptionSelector\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationSettings`  <a name="cfn-medialive-channel-captiondescription-destinationsettings"></a>
Include this element once in each CaptionDescription in the channel\. This element configures one output captions encode\.  
*Required*: No  
*Type*: [CaptionDestinationSettings](aws-properties-medialive-channel-captiondestinationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LanguageCode`  <a name="cfn-medialive-channel-captiondescription-languagecode"></a>
ISO 639\-2 three\-digit code: http://www\.loc\.gov/standards/iso639\-2/\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LanguageDescription`  <a name="cfn-medialive-channel-captiondescription-languagedescription"></a>
Human readable information to indicate captions available for players \(eg\. English, or Spanish\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-captiondescription-name"></a>
A name for this CaptionDescription\. Must be unique in the channel\. MediaLive uses this name to associate the CaptionDescription with the output group it belongs to: you enter the same value in this field and in the CaptionDescriptionNames field of the output in the appropriate output group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)