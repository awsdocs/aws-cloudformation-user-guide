# AWS::MediaLive::Channel AudioSelector<a name="aws-properties-medialive-channel-audioselector"></a>

Audio Selector

## Syntax<a name="aws-properties-medialive-channel-audioselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audioselector-syntax.json"></a>

```
{
  "[Name](#cfn-medialive-channel-audioselector-name)" : String,
  "[SelectorSettings](#cfn-medialive-channel-audioselector-selectorsettings)" : AudioSelectorSettings
}
```

### YAML<a name="aws-properties-medialive-channel-audioselector-syntax.yaml"></a>

```
  [Name](#cfn-medialive-channel-audioselector-name): String
  [SelectorSettings](#cfn-medialive-channel-audioselector-selectorsettings): 
    AudioSelectorSettings
```

## Properties<a name="aws-properties-medialive-channel-audioselector-properties"></a>

`Name`  <a name="cfn-medialive-channel-audioselector-name"></a>
The name of this AudioSelector\. AudioDescriptions will use this name to uniquely identify this Selector\. Selector names should be unique per input\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectorSettings`  <a name="cfn-medialive-channel-audioselector-selectorsettings"></a>
The audio selector settings\.  
*Required*: No  
*Type*: [AudioSelectorSettings](aws-properties-medialive-channel-audioselectorsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)