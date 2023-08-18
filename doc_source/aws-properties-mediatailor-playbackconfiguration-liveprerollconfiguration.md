# AWS::MediaTailor::PlaybackConfiguration LivePreRollConfiguration<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration"></a>

<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration-description"></a>The `LivePreRollConfiguration` property type specifies Property description not available\. for an [AWS::MediaTailor::PlaybackConfiguration](aws-resource-mediatailor-playbackconfiguration.md)\.

## Syntax<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration-syntax.json"></a>

```
{
  "[AdDecisionServerUrl](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-addecisionserverurl)" : String,
  "[MaxDurationSeconds](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-maxdurationseconds)" : Integer
}
```

### YAML<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration-syntax.yaml"></a>

```
  [AdDecisionServerUrl](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-addecisionserverurl): String
  [MaxDurationSeconds](#cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-maxdurationseconds): Integer
```

## Properties<a name="aws-properties-mediatailor-playbackconfiguration-liveprerollconfiguration-properties"></a>

`AdDecisionServerUrl`  <a name="cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-addecisionserverurl"></a>
The URL for the ad decision server \(ADS\) for pre\-roll ads\. This includes the specification of static parameters and placeholders for dynamic parameters\. AWS Elemental MediaTailor substitutes player\-specific and session\-specific parameters as needed when calling the ADS\. Alternately, for testing, you can provide a static VAST URL\. The maximum length is 25,000 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxDurationSeconds`  <a name="cfn-mediatailor-playbackconfiguration-liveprerollconfiguration-maxdurationseconds"></a>
The maximum allowed duration for the pre\-roll ad avail\. AWS Elemental MediaTailor won't play pre\-roll ads to exceed this duration, regardless of the total duration of ads that the ADS returns\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)