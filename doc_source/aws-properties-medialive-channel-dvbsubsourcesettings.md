# AWS::MediaLive::Channel DvbSubSourceSettings<a name="aws-properties-medialive-channel-dvbsubsourcesettings"></a>

Dvb Sub Source Settings

## Syntax<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax.json"></a>

```
{
  "[Pid](#cfn-medialive-channel-dvbsubsourcesettings-pid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax.yaml"></a>

```
  [Pid](#cfn-medialive-channel-dvbsubsourcesettings-pid): Integer
```

## Properties<a name="aws-properties-medialive-channel-dvbsubsourcesettings-properties"></a>

`Pid`  <a name="cfn-medialive-channel-dvbsubsourcesettings-pid"></a>
When using DVB\-Sub with Burn\-In or SMPTE\-TT, use this PID for the source content\. Unused for DVB\-Sub passthrough\. All DVB\-Sub content is passed through, regardless of selectors\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)