# AWS::MediaLive::Channel CaptionLanguageMapping<a name="aws-properties-medialive-channel-captionlanguagemapping"></a>

Maps a captions channel to an ISO 693\-2 language code \(http://www\.loc\.gov/standards/iso639\-2\), with an optional description\.

The parent of this entity is HlsGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-captionlanguagemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captionlanguagemapping-syntax.json"></a>

```
{
  "[CaptionChannel](#cfn-medialive-channel-captionlanguagemapping-captionchannel)" : Integer,
  "[LanguageCode](#cfn-medialive-channel-captionlanguagemapping-languagecode)" : String,
  "[LanguageDescription](#cfn-medialive-channel-captionlanguagemapping-languagedescription)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-captionlanguagemapping-syntax.yaml"></a>

```
  [CaptionChannel](#cfn-medialive-channel-captionlanguagemapping-captionchannel): Integer
  [LanguageCode](#cfn-medialive-channel-captionlanguagemapping-languagecode): String
  [LanguageDescription](#cfn-medialive-channel-captionlanguagemapping-languagedescription): String
```

## Properties<a name="aws-properties-medialive-channel-captionlanguagemapping-properties"></a>

`CaptionChannel`  <a name="cfn-medialive-channel-captionlanguagemapping-captionchannel"></a>
The closed caption channel being described by this CaptionLanguageMapping\. Each channel mapping must have a unique channel number \(maximum of 4\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LanguageCode`  <a name="cfn-medialive-channel-captionlanguagemapping-languagecode"></a>
A three\-character ISO 639\-2 language code \(see http://www\.loc\.gov/standards/iso639\-2\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LanguageDescription`  <a name="cfn-medialive-channel-captionlanguagemapping-languagedescription"></a>
The textual description of language\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)