# AWS::MediaLive::Channel AudioNormalizationSettings<a name="aws-properties-medialive-channel-audionormalizationsettings"></a>

The settings for normalizing video\.

The parent of this entity is AudioDescription\.

## Syntax<a name="aws-properties-medialive-channel-audionormalizationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-audionormalizationsettings-syntax.json"></a>

```
{
  "[Algorithm](#cfn-medialive-channel-audionormalizationsettings-algorithm)" : String,
  "[AlgorithmControl](#cfn-medialive-channel-audionormalizationsettings-algorithmcontrol)" : String,
  "[TargetLkfs](#cfn-medialive-channel-audionormalizationsettings-targetlkfs)" : Double
}
```

### YAML<a name="aws-properties-medialive-channel-audionormalizationsettings-syntax.yaml"></a>

```
  [Algorithm](#cfn-medialive-channel-audionormalizationsettings-algorithm): String
  [AlgorithmControl](#cfn-medialive-channel-audionormalizationsettings-algorithmcontrol): String
  [TargetLkfs](#cfn-medialive-channel-audionormalizationsettings-targetlkfs): Double
```

## Properties<a name="aws-properties-medialive-channel-audionormalizationsettings-properties"></a>

`Algorithm`  <a name="cfn-medialive-channel-audionormalizationsettings-algorithm"></a>
The audio normalization algorithm to use\. itu17701 conforms to the CALM Act specification\. itu17702 conforms to the EBU R\-128 specification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlgorithmControl`  <a name="cfn-medialive-channel-audionormalizationsettings-algorithmcontrol"></a>
When set to correctAudio, the output audio is corrected using the chosen algorithm\. If set to measureOnly, the audio is measured but not adjusted\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetLkfs`  <a name="cfn-medialive-channel-audionormalizationsettings-targetlkfs"></a>
The Target LKFS\(loudness\) to adjust volume to\. If no value is entered, a default value is used according to the chosen algorithm\. The CALM Act \(1770\-1\) recommends a target of \-24 LKFS\. The EBU R\-128 specification \(1770\-2\) recommends a target of \-23 LKFS\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)