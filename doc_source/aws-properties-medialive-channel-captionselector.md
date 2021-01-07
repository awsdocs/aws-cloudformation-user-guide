# AWS::MediaLive::Channel CaptionSelector<a name="aws-properties-medialive-channel-captionselector"></a>

Information about one caption to extract from the input\.

The parent of this entity is InputSettings\.

## Syntax<a name="aws-properties-medialive-channel-captionselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captionselector-syntax.json"></a>

```
{
  "[LanguageCode](#cfn-medialive-channel-captionselector-languagecode)" : String,
  "[Name](#cfn-medialive-channel-captionselector-name)" : String,
  "[SelectorSettings](#cfn-medialive-channel-captionselector-selectorsettings)" : CaptionSelectorSettings
}
```

### YAML<a name="aws-properties-medialive-channel-captionselector-syntax.yaml"></a>

```
  [LanguageCode](#cfn-medialive-channel-captionselector-languagecode): String
  [Name](#cfn-medialive-channel-captionselector-name): String
  [SelectorSettings](#cfn-medialive-channel-captionselector-selectorsettings): 
    CaptionSelectorSettings
```

## Properties<a name="aws-properties-medialive-channel-captionselector-properties"></a>

`LanguageCode`  <a name="cfn-medialive-channel-captionselector-languagecode"></a>
When specified, this field indicates the three\-letter language code of the captions track to extract from the source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-medialive-channel-captionselector-name"></a>
The name identifier for a captions selector\. This name is used to associate this captions selector with one or more captions descriptions\. Names must be unique within a channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectorSettings`  <a name="cfn-medialive-channel-captionselector-selectorsettings"></a>
Information about the specific audio to extract from the input\.  
*Required*: No  
*Type*: [CaptionSelectorSettings](aws-properties-medialive-channel-captionselectorsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)