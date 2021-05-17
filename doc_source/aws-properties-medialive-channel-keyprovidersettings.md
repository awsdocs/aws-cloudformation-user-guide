# AWS::MediaLive::Channel KeyProviderSettings<a name="aws-properties-medialive-channel-keyprovidersettings"></a>

The configuration of key provider settings\.

The parent of this entity is HlsGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-keyprovidersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-keyprovidersettings-syntax.json"></a>

```
{
  "[StaticKeySettings](#cfn-medialive-channel-keyprovidersettings-statickeysettings)" : StaticKeySettings
}
```

### YAML<a name="aws-properties-medialive-channel-keyprovidersettings-syntax.yaml"></a>

```
  [StaticKeySettings](#cfn-medialive-channel-keyprovidersettings-statickeysettings): 
    StaticKeySettings
```

## Properties<a name="aws-properties-medialive-channel-keyprovidersettings-properties"></a>

`StaticKeySettings`  <a name="cfn-medialive-channel-keyprovidersettings-statickeysettings"></a>
The configuration of static key settings\.  
*Required*: No  
*Type*: [StaticKeySettings](aws-properties-medialive-channel-statickeysettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)