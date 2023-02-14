# AWS::MediaLive::Channel AudioOnlyHlsSettings<a name="aws-properties-medialive-channel-audioonlyhlssettings"></a>

The configuration of an audio\-only HLS output\.

The parent of this entity is HlsSettings\.

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
Specifies the group that the audio rendition belongs to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioOnlyImage`  <a name="cfn-medialive-channel-audioonlyhlssettings-audioonlyimage"></a>
Used with an audio\-only stream\. It must be a \.jpg or \.png file\. If given, this image is used as the cover art for the audio\-only output\. Ideally, it should be formatted for an iPhone screen for two reasons\. The iPhone does not resize the image; instead, it crops a centered image on the top/bottom and left/right\. Additionally, this image file gets saved bit\-for\-bit into every 10\-second segment file, so it increases bandwidth by \{image file size\} \* \{segment count\} \* \{user count\.\}\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AudioTrackType`  <a name="cfn-medialive-channel-audioonlyhlssettings-audiotracktype"></a>
Four types of audio\-only tracks are supported: Audio\-Only Variant Stream The client can play back this audio\-only stream instead of video in low\-bandwidth scenarios\. Represented as an EXT\-X\-STREAM\-INF in the HLS manifest\. Alternate Audio, Auto Select, Default Alternate rendition that the client should try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=YES, AUTOSELECT=YES Alternate Audio, Auto Select, Not Default Alternate rendition that the client might try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=NO, AUTOSELECT=YES Alternate Audio, not Auto Select Alternate rendition that the client will not try to play back by default\. Represented as an EXT\-X\-MEDIA in the HLS manifest with DEFAULT=NO, AUTOSELECT=NO\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentType`  <a name="cfn-medialive-channel-audioonlyhlssettings-segmenttype"></a>
Specifies the segment type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)