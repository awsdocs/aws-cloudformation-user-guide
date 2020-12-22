# AWS::MediaLive::Channel StaticKeySettings<a name="aws-properties-medialive-channel-statickeysettings"></a>

The static key settings\.

The parent of this entity is KeyProviderSettings\.

## Syntax<a name="aws-properties-medialive-channel-statickeysettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-statickeysettings-syntax.json"></a>

```
{
  "[KeyProviderServer](#cfn-medialive-channel-statickeysettings-keyproviderserver)" : InputLocation,
  "[StaticKeyValue](#cfn-medialive-channel-statickeysettings-statickeyvalue)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-statickeysettings-syntax.yaml"></a>

```
  [KeyProviderServer](#cfn-medialive-channel-statickeysettings-keyproviderserver): 
    InputLocation
  [StaticKeyValue](#cfn-medialive-channel-statickeysettings-statickeyvalue): String
```

## Properties<a name="aws-properties-medialive-channel-statickeysettings-properties"></a>

`KeyProviderServer`  <a name="cfn-medialive-channel-statickeysettings-keyproviderserver"></a>
The URL of the license server that is used for protecting content\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticKeyValue`  <a name="cfn-medialive-channel-statickeysettings-statickeyvalue"></a>
The static key value as a 32 character hexadecimal string\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)