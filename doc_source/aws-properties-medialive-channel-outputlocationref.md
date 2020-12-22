# AWS::MediaLive::Channel OutputLocationRef<a name="aws-properties-medialive-channel-outputlocationref"></a>

A reference to an OutputDestination ID that is defined in the channel\.

This entity is used by ArchiveGroupSettings, FrameCaptureGroupSettings, HlsGroupSettings, MediaPackageGroupSettings, MSSmoothGroupSettings, RtmpOutputSettings, and UdpOutputSettings\. 

## Syntax<a name="aws-properties-medialive-channel-outputlocationref-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-outputlocationref-syntax.json"></a>

```
{
  "[DestinationRefId](#cfn-medialive-channel-outputlocationref-destinationrefid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-outputlocationref-syntax.yaml"></a>

```
  [DestinationRefId](#cfn-medialive-channel-outputlocationref-destinationrefid): String
```

## Properties<a name="aws-properties-medialive-channel-outputlocationref-properties"></a>

`DestinationRefId`  <a name="cfn-medialive-channel-outputlocationref-destinationrefid"></a>
A reference ID for this destination\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)