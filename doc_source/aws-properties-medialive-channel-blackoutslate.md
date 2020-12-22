# AWS::MediaLive::Channel BlackoutSlate<a name="aws-properties-medialive-channel-blackoutslate"></a>

The settings for a blackout slate\.

The parent of this entity is EncoderSettings\.

## Syntax<a name="aws-properties-medialive-channel-blackoutslate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-blackoutslate-syntax.json"></a>

```
{
  "[BlackoutSlateImage](#cfn-medialive-channel-blackoutslate-blackoutslateimage)" : InputLocation,
  "[NetworkEndBlackout](#cfn-medialive-channel-blackoutslate-networkendblackout)" : String,
  "[NetworkEndBlackoutImage](#cfn-medialive-channel-blackoutslate-networkendblackoutimage)" : InputLocation,
  "[NetworkId](#cfn-medialive-channel-blackoutslate-networkid)" : String,
  "[State](#cfn-medialive-channel-blackoutslate-state)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-blackoutslate-syntax.yaml"></a>

```
  [BlackoutSlateImage](#cfn-medialive-channel-blackoutslate-blackoutslateimage): 
    InputLocation
  [NetworkEndBlackout](#cfn-medialive-channel-blackoutslate-networkendblackout): String
  [NetworkEndBlackoutImage](#cfn-medialive-channel-blackoutslate-networkendblackoutimage): 
    InputLocation
  [NetworkId](#cfn-medialive-channel-blackoutslate-networkid): String
  [State](#cfn-medialive-channel-blackoutslate-state): String
```

## Properties<a name="aws-properties-medialive-channel-blackoutslate-properties"></a>

`BlackoutSlateImage`  <a name="cfn-medialive-channel-blackoutslate-blackoutslateimage"></a>
The blackout slate image to be used\. Keep empty for solid black\. Only \.bmp and \.png images are supported\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkEndBlackout`  <a name="cfn-medialive-channel-blackoutslate-networkendblackout"></a>
Setting to enabled causes MediaLive to blackout the video, audio, and captions, and raise the "Network Blackout Image" slate when an SCTE104/35 Network End Segmentation Descriptor is encountered\. The blackout is lifted when the Network Start Segmentation Descriptor is encountered\. The Network End and Network Start descriptors must contain a network ID that matches the value entered in Network ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkEndBlackoutImage`  <a name="cfn-medialive-channel-blackoutslate-networkendblackoutimage"></a>
The path to the local file to use as the Network End Blackout image\. The image is scaled to fill the entire output raster\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkId`  <a name="cfn-medialive-channel-blackoutslate-networkid"></a>
Provides a Network ID that matches EIDR ID format \(for example, "10\.XXXX/XXXX\-XXXX\-XXXX\-XXXX\-XXXX\-C"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-medialive-channel-blackoutslate-state"></a>
When set to enabled, this causes video, audio, and captions to be blanked when indicated by program metadata\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)