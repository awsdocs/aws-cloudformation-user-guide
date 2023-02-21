# AWS::MediaTailor::PlaybackConfiguration<a name="aws-resource-mediatailor-playbackconfiguration"></a>

Adds a new playback configuration to AWS Elemental MediaTailor\.

## Syntax<a name="aws-resource-mediatailor-playbackconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediatailor-playbackconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::MediaTailor::PlaybackConfiguration",
  "Properties" : {
      "[AdDecisionServerUrl](#cfn-mediatailor-playbackconfiguration-addecisionserverurl)" : String,
      "[AvailSuppression](#cfn-mediatailor-playbackconfiguration-availsuppression)" : AvailSuppression,
      "[Bumper](#cfn-mediatailor-playbackconfiguration-bumper)" : Bumper,
      "[CdnConfiguration](#cfn-mediatailor-playbackconfiguration-cdnconfiguration)" : CdnConfiguration,
      "[ConfigurationAliases](#cfn-mediatailor-playbackconfiguration-configurationaliases)" : {Key : Value, ...},
      "[DashConfiguration](#cfn-mediatailor-playbackconfiguration-dashconfiguration)" : DashConfiguration,
      "[HlsConfiguration](#cfn-mediatailor-playbackconfiguration-hlsconfiguration)" : HlsConfiguration,
      "[LivePreRollConfiguration](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration)" : LivePreRollConfiguration,
      "[ManifestProcessingRules](#cfn-mediatailor-playbackconfiguration-manifestprocessingrules)" : ManifestProcessingRules,
      "[Name](#cfn-mediatailor-playbackconfiguration-name)" : String,
      "[PersonalizationThresholdSeconds](#cfn-mediatailor-playbackconfiguration-personalizationthresholdseconds)" : Integer,
      "[SlateAdUrl](#cfn-mediatailor-playbackconfiguration-slateadurl)" : String,
      "[Tags](#cfn-mediatailor-playbackconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TranscodeProfileName](#cfn-mediatailor-playbackconfiguration-transcodeprofilename)" : String,
      "[VideoContentSourceUrl](#cfn-mediatailor-playbackconfiguration-videocontentsourceurl)" : String
    }
}
```

### YAML<a name="aws-resource-mediatailor-playbackconfiguration-syntax.yaml"></a>

```
Type: AWS::MediaTailor::PlaybackConfiguration
Properties: 
  [AdDecisionServerUrl](#cfn-mediatailor-playbackconfiguration-addecisionserverurl): String
  [AvailSuppression](#cfn-mediatailor-playbackconfiguration-availsuppression): 
    AvailSuppression
  [Bumper](#cfn-mediatailor-playbackconfiguration-bumper): 
    Bumper
  [CdnConfiguration](#cfn-mediatailor-playbackconfiguration-cdnconfiguration): 
    CdnConfiguration
  [ConfigurationAliases](#cfn-mediatailor-playbackconfiguration-configurationaliases): 
    Key : Value
  [DashConfiguration](#cfn-mediatailor-playbackconfiguration-dashconfiguration): 
    DashConfiguration
  [HlsConfiguration](#cfn-mediatailor-playbackconfiguration-hlsconfiguration): 
    HlsConfiguration
  [LivePreRollConfiguration](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration): 
    LivePreRollConfiguration
  [ManifestProcessingRules](#cfn-mediatailor-playbackconfiguration-manifestprocessingrules): 
    ManifestProcessingRules
  [Name](#cfn-mediatailor-playbackconfiguration-name): String
  [PersonalizationThresholdSeconds](#cfn-mediatailor-playbackconfiguration-personalizationthresholdseconds): Integer
  [SlateAdUrl](#cfn-mediatailor-playbackconfiguration-slateadurl): String
  [Tags](#cfn-mediatailor-playbackconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TranscodeProfileName](#cfn-mediatailor-playbackconfiguration-transcodeprofilename): String
  [VideoContentSourceUrl](#cfn-mediatailor-playbackconfiguration-videocontentsourceurl): String
```

## Properties<a name="aws-resource-mediatailor-playbackconfiguration-properties"></a>

`AdDecisionServerUrl`  <a name="cfn-mediatailor-playbackconfiguration-addecisionserverurl"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailSuppression`  <a name="cfn-mediatailor-playbackconfiguration-availsuppression"></a>
Property description not available\.  
*Required*: No  
*Type*: [AvailSuppression](aws-properties-mediatailor-playbackconfiguration-availsuppression.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bumper`  <a name="cfn-mediatailor-playbackconfiguration-bumper"></a>
Property description not available\.  
*Required*: No  
*Type*: [Bumper](aws-properties-mediatailor-playbackconfiguration-bumper.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CdnConfiguration`  <a name="cfn-mediatailor-playbackconfiguration-cdnconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [CdnConfiguration](aws-properties-mediatailor-playbackconfiguration-cdnconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationAliases`  <a name="cfn-mediatailor-playbackconfiguration-configurationaliases"></a>
The player parameters and aliases used as dynamic variables during session initialization\. For more information, see [Domain Variables](https://docs.aws.amazon.com/mediatailor/latest/ug/variables-domain.html)\.  
*Required*: No  
*Type*: Map of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DashConfiguration`  <a name="cfn-mediatailor-playbackconfiguration-dashconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [DashConfiguration](aws-properties-mediatailor-playbackconfiguration-dashconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsConfiguration`  <a name="cfn-mediatailor-playbackconfiguration-hlsconfiguration"></a>
The configuration for HLS content\.  
*Required*: No  
*Type*: [HlsConfiguration](aws-properties-mediatailor-playbackconfiguration-hlsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LivePreRollConfiguration`  <a name="cfn-mediatailor-playbackconfiguration-liveprerollconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [LivePreRollConfiguration](aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestProcessingRules`  <a name="cfn-mediatailor-playbackconfiguration-manifestprocessingrules"></a>
Property description not available\.  
*Required*: No  
*Type*: [ManifestProcessingRules](aws-properties-mediatailor-playbackconfiguration-manifestprocessingrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediatailor-playbackconfiguration-name"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PersonalizationThresholdSeconds`  <a name="cfn-mediatailor-playbackconfiguration-personalizationthresholdseconds"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SlateAdUrl`  <a name="cfn-mediatailor-playbackconfiguration-slateadurl"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediatailor-playbackconfiguration-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TranscodeProfileName`  <a name="cfn-mediatailor-playbackconfiguration-transcodeprofilename"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoContentSourceUrl`  <a name="cfn-mediatailor-playbackconfiguration-videocontentsourceurl"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediatailor-playbackconfiguration-return-values"></a>

### Fn::GetAtt<a name="aws-resource-mediatailor-playbackconfiguration-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediatailor-playbackconfiguration-return-values-fn--getatt-fn--getatt"></a>

`DashConfiguration.ManifestEndpointPrefix`  <a name="DashConfiguration.ManifestEndpointPrefix-fn::getatt"></a>
The URL generated by MediaTailor to initiate a playback session\. The session uses server\-side reporting\. This setting is ignored in PUT operations\.

`HlsConfiguration.ManifestEndpointPrefix`  <a name="HlsConfiguration.ManifestEndpointPrefix-fn::getatt"></a>
The URL that is used to initiate a playback session for devices that support Apple HLS\. The session uses server\-side reporting\.

`PlaybackConfigurationArn`  <a name="PlaybackConfigurationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the playback configuration\.

`PlaybackEndpointPrefix`  <a name="PlaybackEndpointPrefix-fn::getatt"></a>
The URL that the player accesses to get a manifest from MediaTailor\. This session will use server\-side reporting\.

`SessionInitializationEndpointPrefix`  <a name="SessionInitializationEndpointPrefix-fn::getatt"></a>
The URL that the player uses to initialize a session that uses client\-side reporting\.