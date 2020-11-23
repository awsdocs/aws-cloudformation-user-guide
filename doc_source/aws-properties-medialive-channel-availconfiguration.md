# AWS::MediaLive::Channel AvailConfiguration<a name="aws-properties-medialive-channel-availconfiguration"></a>

This element configures some parts of the SCTE\-35 message processing feature in the channel\. This element belongs to EncoderSettings\.

## Syntax<a name="aws-properties-medialive-channel-availconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-availconfiguration-syntax.json"></a>

```
{
  "[AvailSettings](#cfn-medialive-channel-availconfiguration-availsettings)" : AvailSettings
}
```

### YAML<a name="aws-properties-medialive-channel-availconfiguration-syntax.yaml"></a>

```
  [AvailSettings](#cfn-medialive-channel-availconfiguration-availsettings): 
    AvailSettings
```

## Properties<a name="aws-properties-medialive-channel-availconfiguration-properties"></a>

`AvailSettings`  <a name="cfn-medialive-channel-availconfiguration-availsettings"></a>
Ad avail settings\.  
*Required*: No  
*Type*: [AvailSettings](aws-properties-medialive-channel-availsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)