# AWS::MediaLive::Channel UdpContainerSettings<a name="aws-properties-medialive-channel-udpcontainersettings"></a>

The configuration of a UDP output\.

The parent of this entity is UdpOutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-udpcontainersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-udpcontainersettings-syntax.json"></a>

```
{
  "[M2tsSettings](#cfn-medialive-channel-udpcontainersettings-m2tssettings)" : M2tsSettings
}
```

### YAML<a name="aws-properties-medialive-channel-udpcontainersettings-syntax.yaml"></a>

```
  [M2tsSettings](#cfn-medialive-channel-udpcontainersettings-m2tssettings): 
    M2tsSettings
```

## Properties<a name="aws-properties-medialive-channel-udpcontainersettings-properties"></a>

`M2tsSettings`  <a name="cfn-medialive-channel-udpcontainersettings-m2tssettings"></a>
The M2TS configuration for this UDP output\.  
*Required*: No  
*Type*: [M2tsSettings](aws-properties-medialive-channel-m2tssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)