# AWS::MediaLive::Channel AacSettings<a name="aws-properties-medialive-channel-aacsettings"></a>

The settings for an AAC audio encode in the output\. 

The parent of this entity is AudioCodecSettings\.

## Syntax<a name="aws-properties-medialive-channel-aacsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-aacsettings-syntax.json"></a>

```
{
  "[Bitrate](#cfn-medialive-channel-aacsettings-bitrate)" : Double,
  "[CodingMode](#cfn-medialive-channel-aacsettings-codingmode)" : String,
  "[InputType](#cfn-medialive-channel-aacsettings-inputtype)" : String,
  "[Profile](#cfn-medialive-channel-aacsettings-profile)" : String,
  "[RateControlMode](#cfn-medialive-channel-aacsettings-ratecontrolmode)" : String,
  "[RawFormat](#cfn-medialive-channel-aacsettings-rawformat)" : String,
  "[SampleRate](#cfn-medialive-channel-aacsettings-samplerate)" : Double,
  "[Spec](#cfn-medialive-channel-aacsettings-spec)" : String,
  "[VbrQuality](#cfn-medialive-channel-aacsettings-vbrquality)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-aacsettings-syntax.yaml"></a>

```
  [Bitrate](#cfn-medialive-channel-aacsettings-bitrate): Double
  [CodingMode](#cfn-medialive-channel-aacsettings-codingmode): String
  [InputType](#cfn-medialive-channel-aacsettings-inputtype): String
  [Profile](#cfn-medialive-channel-aacsettings-profile): String
  [RateControlMode](#cfn-medialive-channel-aacsettings-ratecontrolmode): String
  [RawFormat](#cfn-medialive-channel-aacsettings-rawformat): String
  [SampleRate](#cfn-medialive-channel-aacsettings-samplerate): Double
  [Spec](#cfn-medialive-channel-aacsettings-spec): String
  [VbrQuality](#cfn-medialive-channel-aacsettings-vbrquality): String
```

## Properties<a name="aws-properties-medialive-channel-aacsettings-properties"></a>

`Bitrate`  <a name="cfn-medialive-channel-aacsettings-bitrate"></a>
The average bitrate in bits/second\. Valid values depend on the rate control mode and profile\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodingMode`  <a name="cfn-medialive-channel-aacsettings-codingmode"></a>
Mono, stereo, or 5\.1 channel layout\. Valid values depend on the rate control mode and profile\. The adReceiverMix setting receives a stereo description plus control track, and emits a mono AAC encode of the description track, with control data emitted in the PES header as per ETSI TS 101 154 Annex E\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputType`  <a name="cfn-medialive-channel-aacsettings-inputtype"></a>
Set to broadcasterMixedAd when the input contains pre\-mixed main audio \+ AD \(narration\) as a stereo pair\. The Audio Type field \(audioType\) will be set to 3, which signals to downstream systems that this stream contains broadcaster mixed AD\. Note that the input received by the encoder must contain pre\-mixed audio; MediaLive does not perform the mixing\. The values in audioTypeControl and audioType \(in AudioDescription\) are ignored when set to broadcasterMixedAd\. Leave this set to normal when the input does not contain pre\-mixed audio \+ AD\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Profile`  <a name="cfn-medialive-channel-aacsettings-profile"></a>
The AAC profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateControlMode`  <a name="cfn-medialive-channel-aacsettings-ratecontrolmode"></a>
The rate control mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RawFormat`  <a name="cfn-medialive-channel-aacsettings-rawformat"></a>
Sets the LATM/LOAS AAC output for raw containers\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleRate`  <a name="cfn-medialive-channel-aacsettings-samplerate"></a>
The sample rate in Hz\. Valid values depend on the rate control mode and profile\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Spec`  <a name="cfn-medialive-channel-aacsettings-spec"></a>
Uses MPEG\-2 AAC audio instead of MPEG\-4 AAC audio for raw or MPEG\-2 Transport Stream containers\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VbrQuality`  <a name="cfn-medialive-channel-aacsettings-vbrquality"></a>
The VBR quality level\. This is used only if rateControlMode is VBR\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)