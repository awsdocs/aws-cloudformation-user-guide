# AWS::MediaTailor::Channel DashPlaylistSettings<a name="aws-properties-mediatailor-channel-dashplaylistsettings"></a>

Dash manifest configuration parameters\.

## Syntax<a name="aws-properties-mediatailor-channel-dashplaylistsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-channel-dashplaylistsettings-syntax.json"></a>

```
{
  "[ManifestWindowSeconds](#cfn-mediatailor-channel-dashplaylistsettings-manifestwindowseconds)" : Double,
  "[MinBufferTimeSeconds](#cfn-mediatailor-channel-dashplaylistsettings-minbuffertimeseconds)" : Double,
  "[MinUpdatePeriodSeconds](#cfn-mediatailor-channel-dashplaylistsettings-minupdateperiodseconds)" : Double,
  "[SuggestedPresentationDelaySeconds](#cfn-mediatailor-channel-dashplaylistsettings-suggestedpresentationdelayseconds)" : Double
}
```

### YAML<a name="aws-properties-mediatailor-channel-dashplaylistsettings-syntax.yaml"></a>

```
  [ManifestWindowSeconds](#cfn-mediatailor-channel-dashplaylistsettings-manifestwindowseconds): Double
  [MinBufferTimeSeconds](#cfn-mediatailor-channel-dashplaylistsettings-minbuffertimeseconds): Double
  [MinUpdatePeriodSeconds](#cfn-mediatailor-channel-dashplaylistsettings-minupdateperiodseconds): Double
  [SuggestedPresentationDelaySeconds](#cfn-mediatailor-channel-dashplaylistsettings-suggestedpresentationdelayseconds): Double
```

## Properties<a name="aws-properties-mediatailor-channel-dashplaylistsettings-properties"></a>

`ManifestWindowSeconds`  <a name="cfn-mediatailor-channel-dashplaylistsettings-manifestwindowseconds"></a>
The total duration \(in seconds\) of each manifest\. Minimum value: `30` seconds\. Maximum value: `3600` seconds\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinBufferTimeSeconds`  <a name="cfn-mediatailor-channel-dashplaylistsettings-minbuffertimeseconds"></a>
Minimum amount of content \(measured in seconds\) that a player must keep available in the buffer\. Minimum value: `2` seconds\. Maximum value: `60` seconds\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinUpdatePeriodSeconds`  <a name="cfn-mediatailor-channel-dashplaylistsettings-minupdateperiodseconds"></a>
Minimum amount of time \(in seconds\) that the player should wait before requesting updates to the manifest\. Minimum value: `2` seconds\. Maximum value: `60` seconds\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuggestedPresentationDelaySeconds`  <a name="cfn-mediatailor-channel-dashplaylistsettings-suggestedpresentationdelayseconds"></a>
Amount of time \(in seconds\) that the player should be from the live point at the end of the manifest\. Minimum value: `2` seconds\. Maximum value: `60` seconds\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)