# AWS::MediaPackageV2::OriginEndpoint Segment<a name="aws-properties-mediapackagev2-originendpoint-segment"></a>

The segment configuration, including the segment name, duration, and other configuration values\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-segment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-segment-syntax.json"></a>

```
{
  "[Encryption](#cfn-mediapackagev2-originendpoint-segment-encryption)" : Encryption,
  "[IncludeIframeOnlyStreams](#cfn-mediapackagev2-originendpoint-segment-includeiframeonlystreams)" : Boolean,
  "[Scte](#cfn-mediapackagev2-originendpoint-segment-scte)" : Scte,
  "[SegmentDurationSeconds](#cfn-mediapackagev2-originendpoint-segment-segmentdurationseconds)" : Integer,
  "[SegmentName](#cfn-mediapackagev2-originendpoint-segment-segmentname)" : String,
  "[TsIncludeDvbSubtitles](#cfn-mediapackagev2-originendpoint-segment-tsincludedvbsubtitles)" : Boolean,
  "[TsUseAudioRenditionGroup](#cfn-mediapackagev2-originendpoint-segment-tsuseaudiorenditiongroup)" : Boolean
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-segment-syntax.yaml"></a>

```
  [Encryption](#cfn-mediapackagev2-originendpoint-segment-encryption): 
    Encryption
  [IncludeIframeOnlyStreams](#cfn-mediapackagev2-originendpoint-segment-includeiframeonlystreams): Boolean
  [Scte](#cfn-mediapackagev2-originendpoint-segment-scte): 
    Scte
  [SegmentDurationSeconds](#cfn-mediapackagev2-originendpoint-segment-segmentdurationseconds): Integer
  [SegmentName](#cfn-mediapackagev2-originendpoint-segment-segmentname): String
  [TsIncludeDvbSubtitles](#cfn-mediapackagev2-originendpoint-segment-tsincludedvbsubtitles): Boolean
  [TsUseAudioRenditionGroup](#cfn-mediapackagev2-originendpoint-segment-tsuseaudiorenditiongroup): Boolean
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-segment-properties"></a>

`Encryption`  <a name="cfn-mediapackagev2-originendpoint-segment-encryption"></a>
Whether to use encryption for the segment\.  
*Required*: No  
*Type*: [Encryption](aws-properties-mediapackagev2-originendpoint-encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeIframeOnlyStreams`  <a name="cfn-mediapackagev2-originendpoint-segment-includeiframeonlystreams"></a>
Whether the segment includes I\-frame\-only streams\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte`  <a name="cfn-mediapackagev2-originendpoint-segment-scte"></a>
The SCTE\-35 configuration associated with the segment\.  
*Required*: No  
*Type*: [Scte](aws-properties-mediapackagev2-originendpoint-scte.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentDurationSeconds`  <a name="cfn-mediapackagev2-originendpoint-segment-segmentdurationseconds"></a>
The duration of the segment, in seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentName`  <a name="cfn-mediapackagev2-originendpoint-segment-segmentname"></a>
The name of the segment associated with the origin endpoint\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9_-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TsIncludeDvbSubtitles`  <a name="cfn-mediapackagev2-originendpoint-segment-tsincludedvbsubtitles"></a>
Whether the segment includes DVB subtitles\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TsUseAudioRenditionGroup`  <a name="cfn-mediapackagev2-originendpoint-segment-tsuseaudiorenditiongroup"></a>
Whether the segment is an audio rendition group\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)