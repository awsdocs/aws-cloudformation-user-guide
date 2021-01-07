# AWS::MediaLive::Channel AutomaticInputFailoverSettings<a name="aws-properties-medialive-channel-automaticinputfailoversettings"></a>

The settings for Automatic Input Failover\.

## Syntax<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax.json"></a>

```
{
  "[InputPreference](#cfn-medialive-channel-automaticinputfailoversettings-inputpreference)" : String,
  "[SecondaryInputId](#cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax.yaml"></a>

```
  [InputPreference](#cfn-medialive-channel-automaticinputfailoversettings-inputpreference): String
  [SecondaryInputId](#cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid): String
```

## Properties<a name="aws-properties-medialive-channel-automaticinputfailoversettings-properties"></a>

`InputPreference`  <a name="cfn-medialive-channel-automaticinputfailoversettings-inputpreference"></a>
Input preference when deciding which input to make active when a previously failed input has recovered\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryInputId`  <a name="cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid"></a>
The input ID of the secondary input in the automatic input failover pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)