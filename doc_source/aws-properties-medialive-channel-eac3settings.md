# AWS::MediaLive::Channel Eac3Settings<a name="aws-properties-medialive-channel-eac3settings"></a>

Eac3 Settings

## Syntax<a name="aws-properties-medialive-channel-eac3settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-eac3settings-syntax.json"></a>

```
{
  "[AttenuationControl](#cfn-medialive-channel-eac3settings-attenuationcontrol)" : String,
  "[Bitrate](#cfn-medialive-channel-eac3settings-bitrate)" : Double,
  "[BitstreamMode](#cfn-medialive-channel-eac3settings-bitstreammode)" : String,
  "[CodingMode](#cfn-medialive-channel-eac3settings-codingmode)" : String,
  "[DcFilter](#cfn-medialive-channel-eac3settings-dcfilter)" : String,
  "[Dialnorm](#cfn-medialive-channel-eac3settings-dialnorm)" : Integer,
  "[DrcLine](#cfn-medialive-channel-eac3settings-drcline)" : String,
  "[DrcRf](#cfn-medialive-channel-eac3settings-drcrf)" : String,
  "[LfeControl](#cfn-medialive-channel-eac3settings-lfecontrol)" : String,
  "[LfeFilter](#cfn-medialive-channel-eac3settings-lfefilter)" : String,
  "[LoRoCenterMixLevel](#cfn-medialive-channel-eac3settings-lorocentermixlevel)" : Double,
  "[LoRoSurroundMixLevel](#cfn-medialive-channel-eac3settings-lorosurroundmixlevel)" : Double,
  "[LtRtCenterMixLevel](#cfn-medialive-channel-eac3settings-ltrtcentermixlevel)" : Double,
  "[LtRtSurroundMixLevel](#cfn-medialive-channel-eac3settings-ltrtsurroundmixlevel)" : Double,
  "[MetadataControl](#cfn-medialive-channel-eac3settings-metadatacontrol)" : String,
  "[PassthroughControl](#cfn-medialive-channel-eac3settings-passthroughcontrol)" : String,
  "[PhaseControl](#cfn-medialive-channel-eac3settings-phasecontrol)" : String,
  "[StereoDownmix](#cfn-medialive-channel-eac3settings-stereodownmix)" : String,
  "[SurroundExMode](#cfn-medialive-channel-eac3settings-surroundexmode)" : String,
  "[SurroundMode](#cfn-medialive-channel-eac3settings-surroundmode)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-eac3settings-syntax.yaml"></a>

```
  [AttenuationControl](#cfn-medialive-channel-eac3settings-attenuationcontrol): String
  [Bitrate](#cfn-medialive-channel-eac3settings-bitrate): Double
  [BitstreamMode](#cfn-medialive-channel-eac3settings-bitstreammode): String
  [CodingMode](#cfn-medialive-channel-eac3settings-codingmode): String
  [DcFilter](#cfn-medialive-channel-eac3settings-dcfilter): String
  [Dialnorm](#cfn-medialive-channel-eac3settings-dialnorm): Integer
  [DrcLine](#cfn-medialive-channel-eac3settings-drcline): String
  [DrcRf](#cfn-medialive-channel-eac3settings-drcrf): String
  [LfeControl](#cfn-medialive-channel-eac3settings-lfecontrol): String
  [LfeFilter](#cfn-medialive-channel-eac3settings-lfefilter): String
  [LoRoCenterMixLevel](#cfn-medialive-channel-eac3settings-lorocentermixlevel): Double
  [LoRoSurroundMixLevel](#cfn-medialive-channel-eac3settings-lorosurroundmixlevel): Double
  [LtRtCenterMixLevel](#cfn-medialive-channel-eac3settings-ltrtcentermixlevel): Double
  [LtRtSurroundMixLevel](#cfn-medialive-channel-eac3settings-ltrtsurroundmixlevel): Double
  [MetadataControl](#cfn-medialive-channel-eac3settings-metadatacontrol): String
  [PassthroughControl](#cfn-medialive-channel-eac3settings-passthroughcontrol): String
  [PhaseControl](#cfn-medialive-channel-eac3settings-phasecontrol): String
  [StereoDownmix](#cfn-medialive-channel-eac3settings-stereodownmix): String
  [SurroundExMode](#cfn-medialive-channel-eac3settings-surroundexmode): String
  [SurroundMode](#cfn-medialive-channel-eac3settings-surroundmode): String
```

## Properties<a name="aws-properties-medialive-channel-eac3settings-properties"></a>

`AttenuationControl`  <a name="cfn-medialive-channel-eac3settings-attenuationcontrol"></a>
When set to attenuate3Db, applies a 3 dB attenuation to the surround channels\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Bitrate`  <a name="cfn-medialive-channel-eac3settings-bitrate"></a>
Average bitrate in bits/second\. Valid bitrates depend on the coding mode\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BitstreamMode`  <a name="cfn-medialive-channel-eac3settings-bitstreammode"></a>
Specifies the bitstream mode \(bsmod\) for the emitted E\-AC\-3 stream\. See ATSC A/52\-2012 \(Annex E\) for background on these values\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodingMode`  <a name="cfn-medialive-channel-eac3settings-codingmode"></a>
Dolby Digital Plus coding mode\. Determines number of channels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DcFilter`  <a name="cfn-medialive-channel-eac3settings-dcfilter"></a>
When set to enabled, activates a DC highpass filter for all input channels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dialnorm`  <a name="cfn-medialive-channel-eac3settings-dialnorm"></a>
Sets the dialnorm for the output\. If blank and input audio is Dolby Digital Plus, dialnorm will be passed through\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrcLine`  <a name="cfn-medialive-channel-eac3settings-drcline"></a>
Sets the Dolby dynamic range compression profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrcRf`  <a name="cfn-medialive-channel-eac3settings-drcrf"></a>
Sets the profile for heavy Dolby dynamic range compression, ensures that the instantaneous signal peaks do not exceed specified levels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LfeControl`  <a name="cfn-medialive-channel-eac3settings-lfecontrol"></a>
When encoding 3/2 audio, setting to lfe enables the LFE channel  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LfeFilter`  <a name="cfn-medialive-channel-eac3settings-lfefilter"></a>
When set to enabled, applies a 120Hz lowpass filter to the LFE channel prior to encoding\. Only valid with codingMode32 coding mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRoCenterMixLevel`  <a name="cfn-medialive-channel-eac3settings-lorocentermixlevel"></a>
Left only/Right only center mix level\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoRoSurroundMixLevel`  <a name="cfn-medialive-channel-eac3settings-lorosurroundmixlevel"></a>
Left only/Right only surround mix level\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LtRtCenterMixLevel`  <a name="cfn-medialive-channel-eac3settings-ltrtcentermixlevel"></a>
Left total/Right total center mix level\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LtRtSurroundMixLevel`  <a name="cfn-medialive-channel-eac3settings-ltrtsurroundmixlevel"></a>
Left total/Right total surround mix level\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetadataControl`  <a name="cfn-medialive-channel-eac3settings-metadatacontrol"></a>
When set to followInput, encoder metadata will be sourced from the DD, DD\+, or DolbyE decoder that supplied this audio data\. If audio was not supplied from one of these streams, then the static metadata settings will be used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PassthroughControl`  <a name="cfn-medialive-channel-eac3settings-passthroughcontrol"></a>
When set to whenPossible, input DD\+ audio will be passed through if it is present on the input\. This detection is dynamic over the life of the transcode\. Inputs that alternate between DD\+ and non\-DD\+ content will have a consistent DD\+ output as the system alternates between passthrough and encoding\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhaseControl`  <a name="cfn-medialive-channel-eac3settings-phasecontrol"></a>
When set to shift90Degrees, applies a 90\-degree phase shift to the surround channels\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StereoDownmix`  <a name="cfn-medialive-channel-eac3settings-stereodownmix"></a>
Stereo downmix preference\. Only used for 3/2 coding mode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SurroundExMode`  <a name="cfn-medialive-channel-eac3settings-surroundexmode"></a>
When encoding 3/2 audio, sets whether an extra center back surround channel is matrix encoded into the left and right surround channels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SurroundMode`  <a name="cfn-medialive-channel-eac3settings-surroundmode"></a>
When encoding 2/0 audio, sets whether Dolby Surround is matrix encoded into the two channels\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)