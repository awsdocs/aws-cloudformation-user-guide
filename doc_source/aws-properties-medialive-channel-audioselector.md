# AWS::MediaLive::Channel AudioSelector<a name="aws-properties-medialive-channel-audioselector"></a>

Information about one audio to extract from the input\.

## Syntax<a name="aws-properties-medialive-channel-audioselector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audioselector-syntax.json"></a>

```
{
  "[Name](#cfn-medialive-channel-audioselector-name)" : String,
  "[SelectorSettings](#cfn-medialive-channel-audioselector-selectorsettings)" : [AudioSelectorSettings](aws-properties-medialive-channel-audioselectorsettings.md)
}
```

### YAML<a name="aws-properties-medialive-channel-audioselector-syntax.yaml"></a>

```
  [Name](#cfn-medialive-channel-audioselector-name): String
  [SelectorSettings](#cfn-medialive-channel-audioselector-selectorsettings): 
    [AudioSelectorSettings](aws-properties-medialive-channel-audioselectorsettings.md)
```

## Properties<a name="aws-properties-medialive-channel-audioselector-properties"></a>

`Name`  <a name="cfn-medialive-channel-audioselector-name"></a>
A name for this AudioSelector\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectorSettings`  <a name="cfn-medialive-channel-audioselector-selectorsettings"></a>
Information about the specific audio to extract from the input\.  
*Required*: No  
*Type*: [AudioSelectorSettings](aws-properties-medialive-channel-audioselectorsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `sa-east-1`
- `us-east-1`
- `us-west-2`
