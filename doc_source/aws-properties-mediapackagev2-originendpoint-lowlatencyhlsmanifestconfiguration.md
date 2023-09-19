# AWS::MediaPackageV2::OriginEndpoint LowLatencyHlsManifestConfiguration<a name="aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration"></a>

Specify a low\-latency HTTP live streaming \(LL\-HLS\) manifest configuration\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-syntax.json"></a>

```
{
  "[ChildManifestName](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-childmanifestname)" : String,
  "[ManifestName](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestname)" : String,
  "[ManifestWindowSeconds](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestwindowseconds)" : Integer,
  "[ProgramDateTimeIntervalSeconds](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-programdatetimeintervalseconds)" : Integer,
  "[ScteHls](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-sctehls)" : ScteHls,
  "[Url](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-url)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-syntax.yaml"></a>

```
  [ChildManifestName](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-childmanifestname): String
  [ManifestName](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestname): String
  [ManifestWindowSeconds](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestwindowseconds): Integer
  [ProgramDateTimeIntervalSeconds](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-programdatetimeintervalseconds): Integer
  [ScteHls](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-sctehls): 
    ScteHls
  [Url](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-url): String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-properties"></a>

`ChildManifestName`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-childmanifestname"></a>
The name of the child manifest associated with the low\-latency HLS \(LL\-HLS\) manifest configuration of the origin endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestName`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestname"></a>
A short short string that's appended to the endpoint URL\. The manifest name creates a unique path to this endpoint\. If you don't enter a value, MediaPackage uses the default manifest name, `index`\. MediaPackage automatically inserts the format extension, such as `.m3u8`\. You can't use the same manifest name if you use HLS manifest and low\-latency HLS manifest\. The `manifestName` on the `HLSManifest` object overrides the `manifestName` you provided on the `originEndpoint` object\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestWindowSeconds`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-manifestwindowseconds"></a>
The total duration \(in seconds\) of the manifest's content\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimeIntervalSeconds`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-programdatetimeintervalseconds"></a>
Inserts `EXT-X-PROGRAM-DATE-TIME` tags in the output manifest at the interval that you specify\. If you don't enter an interval, `EXT-X-PROGRAM-DATE-TIME` tags aren't included in the manifest\. The tags sync the stream to the wall clock so that viewers can seek to a specific time in the playback timeline on the player\. `ID3Timed` metadata messages generate every 5 seconds whenever MediaPackage ingests the content\.  
Irrespective of this parameter, if any `ID3Timed` metadata is in the HLS input, MediaPackage passes through that metadata to the HLS output\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScteHls`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-sctehls"></a>
The SCTE\-35 HLS configuration associated with the low\-latency HLS \(LL\-HLS\) manifest configuration of the origin endpoint\.  
*Required*: No  
*Type*: [ScteHls](aws-properties-mediapackagev2-originendpoint-sctehls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration-url"></a>
The URL of the low\-latency HLS \(LL\-HLS\) manifest configuration of the origin endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)