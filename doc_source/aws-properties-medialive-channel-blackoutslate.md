# AWS::MediaLive::Channel BlackoutSlate<a name="aws-properties-medialive-channel-blackoutslate"></a>

Configures the blackout feature in SCTE\-35 message processing\. This feature blacks out the content for an SCTE\-35 message that is not considered to be an ad avail\. This element belongs to EncoderSettings\.

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
Blackout slate image to be used\. Leave empty for solid black\. Only bmp and png images are supported\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkEndBlackout`  <a name="cfn-medialive-channel-blackoutslate-networkendblackout"></a>
Setting to enabled causes the encoder to blackout the video, audio, and captions, and raise the "Network Blackout Image" slate when an SCTE104/35 Network End Segmentation Descriptor is encountered\. The blackout will be lifted when the Network Start Segmentation Descriptor is encountered\. The Network End and Network Start descriptors must contain a network ID that matches the value entered in "Network ID"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkEndBlackoutImage`  <a name="cfn-medialive-channel-blackoutslate-networkendblackoutimage"></a>
Path to local file to use as Network End Blackout image\. Image will be scaled to fill the entire output raster\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkId`  <a name="cfn-medialive-channel-blackoutslate-networkid"></a>
Provides Network ID that matches EIDR ID format \(e\.g\., "10\.XXXX/XXXX\-XXXX\-XXXX\-XXXX\-XXXX\-C"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-medialive-channel-blackoutslate-state"></a>
When set to enabled, causes video, audio and captions to be blanked when indicated by program metadata\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)