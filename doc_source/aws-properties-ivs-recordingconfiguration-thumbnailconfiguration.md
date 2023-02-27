# AWS::IVS::RecordingConfiguration ThumbnailConfiguration<a name="aws-properties-ivs-recordingconfiguration-thumbnailconfiguration"></a>

The ThumbnailConfiguration property type describes a configuration of thumbnails for recorded video\.

## Syntax<a name="aws-properties-ivs-recordingconfiguration-thumbnailconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ivs-recordingconfiguration-thumbnailconfiguration-syntax.json"></a>

```
{
  "[RecordingMode](#cfn-ivs-recordingconfiguration-thumbnailconfiguration-recordingmode)" : String,
  "[TargetIntervalSeconds](#cfn-ivs-recordingconfiguration-thumbnailconfiguration-targetintervalseconds)" : Integer
}
```

### YAML<a name="aws-properties-ivs-recordingconfiguration-thumbnailconfiguration-syntax.yaml"></a>

```
  [RecordingMode](#cfn-ivs-recordingconfiguration-thumbnailconfiguration-recordingmode): String
  [TargetIntervalSeconds](#cfn-ivs-recordingconfiguration-thumbnailconfiguration-targetintervalseconds): Integer
```

## Properties<a name="aws-properties-ivs-recordingconfiguration-thumbnailconfiguration-properties"></a>

`RecordingMode`  <a name="cfn-ivs-recordingconfiguration-thumbnailconfiguration-recordingmode"></a>
Thumbnail recording mode\. Valid values:  
+  `DISABLED`: Use DISABLED to disable the generation of thumbnails for recorded video\.
+  `INTERVAL`: Use INTERVAL to enable the generation of thumbnails for recorded video at a time interval controlled by the [TargetIntervalSeconds](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ivs-recordingconfiguration-thumbnailconfiguration.html#cfn-ivs-recordingconfiguration-thumbnailconfiguration-targetintervalseconds) property\.
*Default*: `INTERVAL`  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | INTERVAL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetIntervalSeconds`  <a name="cfn-ivs-recordingconfiguration-thumbnailconfiguration-targetintervalseconds"></a>
The targeted thumbnail\-generation interval in seconds\. This is configurable \(and required\) only if [RecordingMode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ivs-recordingconfiguration-thumbnailconfiguration.html#cfn-ivs-recordingconfiguration-thumbnailconfiguration-recordingmode) is `INTERVAL`\.  
Setting a value for `TargetIntervalSeconds` does not guarantee that thumbnails are generated at the specified interval\. For thumbnails to be generated at the `TargetIntervalSeconds` interval, the `IDR/Keyframe` value for the input video must be less than the `TargetIntervalSeconds` value\. See [Amazon IVS Streaming Configuration](https://docs.aws.amazon.com/ivs/latest/userguide/streaming-config.html) for information on setting `IDR/Keyframe` to the recommended value in video\-encoder settings\.
*Default*: 60  
*Valid Range*: Minumum value of 5\. Maximum value of 60\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)