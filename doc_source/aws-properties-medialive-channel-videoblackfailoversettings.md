# AWS::MediaLive::Channel VideoBlackFailoverSettings<a name="aws-properties-medialive-channel-videoblackfailoversettings"></a>

<a name="aws-properties-medialive-channel-videoblackfailoversettings-description"></a>The `VideoBlackFailoverSettings` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::MediaLive::Channel](aws-resource-medialive-channel.md)\.

## Syntax<a name="aws-properties-medialive-channel-videoblackfailoversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-videoblackfailoversettings-syntax.json"></a>

```
{
  "[BlackDetectThreshold](#cfn-medialive-channel-videoblackfailoversettings-blackdetectthreshold)" : Double,
  "[VideoBlackThresholdMsec](#cfn-medialive-channel-videoblackfailoversettings-videoblackthresholdmsec)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-videoblackfailoversettings-syntax.yaml"></a>

```
  [BlackDetectThreshold](#cfn-medialive-channel-videoblackfailoversettings-blackdetectthreshold): Double
  [VideoBlackThresholdMsec](#cfn-medialive-channel-videoblackfailoversettings-videoblackthresholdmsec): Integer
```

## Properties<a name="aws-properties-medialive-channel-videoblackfailoversettings-properties"></a>

`BlackDetectThreshold`  <a name="cfn-medialive-channel-videoblackfailoversettings-blackdetectthreshold"></a>
A value used in calculating the threshold below which MediaLive considers a pixel to be 'black'\. For the input to be considered black, every pixel in a frame must be below this threshold\. The threshold is calculated as a percentage \(expressed as a decimal\) of white\. Therefore \.1 means 10% white \(or 90% black\)\. Note how the formula works for any color depth\. For example, if you set this field to 0\.1 in 10\-bit color depth: \(1023\*0\.1=102\.3\), which means a pixel value of 102 or less is 'black'\. If you set this field to \.1 in an 8\-bit color depth: \(255\*0\.1=25\.5\), which means a pixel value of 25 or less is 'black'\. The range is 0\.0 to 1\.0, with any number of decimal places\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VideoBlackThresholdMsec`  <a name="cfn-medialive-channel-videoblackfailoversettings-videoblackthresholdmsec"></a>
The amount of time \(in milliseconds\) that the active input must be black before automatic input failover occurs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)