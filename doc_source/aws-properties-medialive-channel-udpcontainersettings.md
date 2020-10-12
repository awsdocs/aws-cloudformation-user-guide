# AWS::MediaLive::Channel UdpContainerSettings<a name="aws-properties-medialive-channel-udpcontainersettings"></a>

Configures the container in the output group\. This element belongs to UdpOutputSettings\.

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
You must include this element\. It configures MPEG2 TS stream in the output group\.  
*Required*: No  
*Type*: [M2tsSettings](aws-properties-medialive-channel-m2tssettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)