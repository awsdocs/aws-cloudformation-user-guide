# AWS::MediaLive::Channel UdpOutputSettings<a name="aws-properties-medialive-channel-udpoutputsettings"></a>

The settings for one UDP output\.

The parent of this entity is OutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-udpoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-udpoutputsettings-syntax.json"></a>

```
{
  "[BufferMsec](#cfn-medialive-channel-udpoutputsettings-buffermsec)" : Integer,
  "[ContainerSettings](#cfn-medialive-channel-udpoutputsettings-containersettings)" : UdpContainerSettings,
  "[Destination](#cfn-medialive-channel-udpoutputsettings-destination)" : OutputLocationRef,
  "[FecOutputSettings](#cfn-medialive-channel-udpoutputsettings-fecoutputsettings)" : FecOutputSettings
}
```

### YAML<a name="aws-properties-medialive-channel-udpoutputsettings-syntax.yaml"></a>

```
  [BufferMsec](#cfn-medialive-channel-udpoutputsettings-buffermsec): Integer
  [ContainerSettings](#cfn-medialive-channel-udpoutputsettings-containersettings): 
    UdpContainerSettings
  [Destination](#cfn-medialive-channel-udpoutputsettings-destination): 
    OutputLocationRef
  [FecOutputSettings](#cfn-medialive-channel-udpoutputsettings-fecoutputsettings): 
    FecOutputSettings
```

## Properties<a name="aws-properties-medialive-channel-udpoutputsettings-properties"></a>

`BufferMsec`  <a name="cfn-medialive-channel-udpoutputsettings-buffermsec"></a>
The UDP output buffering in milliseconds\. Larger values increase latency through the transcoder but simultaneously assist the transcoder in maintaining a constant, low\-jitter UDP/RTP output while accommodating clock recovery, input switching, input disruptions, picture reordering, and so on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainerSettings`  <a name="cfn-medialive-channel-udpoutputsettings-containersettings"></a>
The settings for the UDP output\.  
*Required*: No  
*Type*: [UdpContainerSettings](aws-properties-medialive-channel-udpcontainersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-udpoutputsettings-destination"></a>
The destination address and port number for RTP or UDP packets\. These can be unicast or multicast RTP or UDP \(for example, rtp://239\.10\.10\.10:5001 or udp://10\.100\.100\.100:5002\)\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FecOutputSettings`  <a name="cfn-medialive-channel-udpoutputsettings-fecoutputsettings"></a>
The settings for enabling and adjusting Forward Error Correction on UDP outputs\.  
*Required*: No  
*Type*: [FecOutputSettings](aws-properties-medialive-channel-fecoutputsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)