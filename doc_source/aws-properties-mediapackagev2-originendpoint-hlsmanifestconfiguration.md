# AWS::MediaPackageV2::OriginEndpoint HlsManifestConfiguration<a name="aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration"></a>

The HLS manfiest configuration associated with the origin endpoint\.

## Syntax<a name="aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration-syntax.json"></a>

```
{
  "[ChildManifestName](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-childmanifestname)" : String,
  "[ManifestName](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestname)" : String,
  "[ManifestWindowSeconds](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestwindowseconds)" : Integer,
  "[ProgramDateTimeIntervalSeconds](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-programdatetimeintervalseconds)" : Integer,
  "[ScteHls](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-sctehls)" : ScteHls,
  "[Url](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-url)" : String
}
```

### YAML<a name="aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration-syntax.yaml"></a>

```
  [ChildManifestName](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-childmanifestname): String
  [ManifestName](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestname): String
  [ManifestWindowSeconds](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestwindowseconds): Integer
  [ProgramDateTimeIntervalSeconds](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-programdatetimeintervalseconds): Integer
  [ScteHls](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-sctehls): 
    ScteHls
  [Url](#cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-url): String
```

## Properties<a name="aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration-properties"></a>

`ChildManifestName`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-childmanifestname"></a>
The name of the child manifest associated with the HLS manifest configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestName`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestname"></a>
The name of the manifest associated with the HLS manifest configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestWindowSeconds`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-manifestwindowseconds"></a>
The duration of the manifest window, in seconds, for the HLS manifest configuration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimeIntervalSeconds`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-programdatetimeintervalseconds"></a>
The `EXT-X-PROGRAM-DATE-TIME` interval, in seconds, associated with the HLS manifest configuration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScteHls`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-sctehls"></a>
THE SCTE\-35 HLS configuration associated with the HLS manifest configuration\.  
*Required*: No  
*Type*: [ScteHls](aws-properties-mediapackagev2-originendpoint-sctehls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifestconfiguration-url"></a>
The URL of the HLS manifest configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)