# AWS::MediaLive::Channel AudioOnlyHlsSettings<a name="aws-properties-medialive-channel-audioonlyhlssettings"></a>

Configures the output as an audio\-only output\. This element belongs to HlsSettings\.

## Syntax<a name="aws-properties-medialive-channel-audioonlyhlssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audioonlyhlssettings-syntax.json"></a>

```
{
  "[AudioGroupId](#cfn-medialive-channel-audioonlyhlssettings-audiogroupid)" : String,
  "[AudioOnlyImage](#cfn-medialive-channel-audioonlyhlssettings-audioonlyimage)" : InputLocation,
  "[AudioTrackType](#cfn-medialive-channel-audioonlyhlssettings-audiotracktype)" : String,
  "[SegmentType](#cfn-medialive-channel-audioonlyhlssettings-segmenttype)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-audioonlyhlssettings-syntax.yaml"></a>

```
  [AudioGroupId](#cfn-medialive-channel-audioonlyhlssettings-audiogroupid): String
  [AudioOnlyImage](#cfn-medialive-channel-audioonlyhlssettings-audioonlyimage): 
    InputLocation
  [AudioTrackType](#cfn-medialive-channel-audioonlyhlssettings-audiotracktype): String
  [SegmentType](#cfn-medialive-channel-audioonlyhlssettings-segmenttype): String
```

## Properties<a name="aws-properties-medialive-channel-audioonlyhlssettings-properties"></a>

`AudioGroupId`  <a name="cfn-medialive-channel-audioonlyhlssettings-audiogroupid"></a>
Specifies the group to which the audio Rendition belongs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioOnlyImage`  <a name="cfn-medialive-channel-audioonlyhlssettings-audioonlyimage"></a>
Optional\. Specifies the \.jpg or \.png image to use as the cover art for an audio\-only output\. We recommend a low bit\-size file because the image increases the output audio bandwidth\. The image is attached to the audio as an ID3 tag, frame type APIC, picture type 0x10, as per the "ID3 tag version 2\.4\.0 \- Native Frames" standard\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioTrackType`  <a name="cfn-medialive-channel-audioonlyhlssettings-audiotracktype"></a>
Four types of audio\-only tracks are supported: Audio\-Only Variant Stream The client can play back this audio\-only stream instead of video in low\-bandwidth scenarios\. Represented as an EXT\-X\-STREAM\-INF in the HLS manifest\. Alternate Audio, Auto Select, Default Alternate rendition that the client should try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=YES, AUTOSELECT=YES Alternate Audio, Auto Select, Not Default Alternate rendition that the client may try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=NO, AUTOSELECT=YES Alternate Audio, not Auto Select Alternate rendition that the client will not try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=NO, AUTOSELECT=NO\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentType`  <a name="cfn-medialive-channel-audioonlyhlssettings-segmenttype"></a>
Specifies the segment type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)