# AWS::MediaConvert::Preset<a name="aws-resource-mediaconvert-preset"></a>

The AWS::MediaConvert::Preset resource is an AWS Elemental MediaConvert resource type that you can use to specify encoding settings for a single output in a transcoding job\.

When you declare this entity in your AWS CloudFormation template, you pass in your transcoding job settings in JSON or YAML format\. This settings specification must be formed in a particular way that conforms to AWS Elemental MediaConvert job validation\. For more information about creating an output preset model for the `SettingsJson` property, see the Remarks section later in this topic\.

For more information about output MediaConvert presets, see [Working with AWS Elemental MediaConvert Output Presets](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-presets.html) in the *AWS Elemental MediaConvert User Guide*\.

## Syntax<a name="aws-resource-mediaconvert-preset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconvert-preset-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConvert::Preset",
  "Properties" : {
      "[Category](#cfn-mediaconvert-preset-category)" : String,
      "[Description](#cfn-mediaconvert-preset-description)" : String,
      "[Name](#cfn-mediaconvert-preset-name)" : String,
      "[SettingsJson](#cfn-mediaconvert-preset-settingsjson)" : Json,
      "[Tags](#cfn-mediaconvert-preset-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-mediaconvert-preset-syntax.yaml"></a>

```
Type: AWS::MediaConvert::Preset
Properties: 
  [Category](#cfn-mediaconvert-preset-category): String
  [Description](#cfn-mediaconvert-preset-description): String
  [Name](#cfn-mediaconvert-preset-name): String
  [SettingsJson](#cfn-mediaconvert-preset-settingsjson): 
    Json
  [Tags](#cfn-mediaconvert-preset-tags): Json
```

## Properties<a name="aws-resource-mediaconvert-preset-properties"></a>

`Category`  <a name="cfn-mediaconvert-preset-category"></a>
The new category for the preset, if you are changing it\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediaconvert-preset-description"></a>
The new description for the preset, if you are changing it\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-mediaconvert-preset-name"></a>
The name of the preset that you are modifying\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SettingsJson`  <a name="cfn-mediaconvert-preset-settingsjson"></a>
Specify, in JSON format, the transcoding job settings for this output preset\. This specification must conform to the AWS Elemental MediaConvert job validation\. For information about forming this specification, see the Remarks section later in this topic\.  
For more information about MediaConvert output presets, see [Working with AWS Elemental MediaConvert Output Presets](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-presets.html) in the *AWS Elemental MediaConvert User Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediaconvert-preset-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediaconvert-preset-return-values"></a>

### Ref<a name="aws-resource-mediaconvert-preset-return-values-ref"></a>

When you pass the logical ID of an `AWS::MediaConvert::Preset` resource to the intrinsic `Ref` function, the function returns the name of the output preset, such as `HEVC high res`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconvert-preset-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediaconvert-preset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) of the output preset, such as `arn:aws:mediaconvert:us-west-2:123456789012`\. 

`Name`  <a name="Name-fn::getatt"></a>
 The name of the output preset, such as `HEVC high res`\. 

## Remarks<a name="aws-resource-mediaconvert-preset--remarks"></a>

 *Creating an Ouput Preset Model for the SettingsJson Property* 

When you declare an AWS::MediaConvert::Preset entity in your AWS CloudFormation template, you pass in your transcoding job settings as the value for the property `SettingsJson`\. This settings specification must be in in JSON or YAML format and must conform to AWS Elemental MediaConvert job validation\.

The following procedure is for generating the specification in JSON\. If you need it in YAML, you can create it in JSON and use a conversion utility\.

**To create a JSON job template model for `SettingsJson`**

1. Create an output preset using the MediaConvert [https://console\.aws\.amazon\.com/mediaconvert/](https://console.aws.amazon.com/mediaconvert/)\. For more information, see [Working with AWS Elemental MediaConvert Output Presets](https://docs.aws.amazon.com/mediaconvert/latest/ug/working-with-presets.html)\.

1. Use the AWS CLI to get just the settings structure using the following command:

   `aws mediaconvert https://abcd1234.mediaconvert.region-name-1.amazonaws.com get-preset --name HEVC-high-res --query 'Preset.Settings'`

1. Copy the settings as the value for the property `SettingsJson`\.

For an example output preset model in JSON and YAML, see the Examples section of this topic\.

## Examples<a name="aws-resource-mediaconvert-preset--examples"></a>



### Output Preset Model for SettingsJson<a name="aws-resource-mediaconvert-preset--examples--Output_Preset_Model_for_SettingsJson"></a>

For more information about creating an output preset model in JSON or YAML for the `SettingsJson` property, see the Remarks section of this topic\.

#### JSON<a name="aws-resource-mediaconvert-preset--examples--Output_Preset_Model_for_SettingsJson--json"></a>

```
{
    "AudioDescriptions": [
        {
            "AudioType": 0,
            "AudioTypeControl": "FOLLOW_INPUT",
            "CodecSettings": {
                "AacSettings": {
                    "AudioDescriptionBroadcasterMix": "NORMAL",
                    "Bitrate": 160000,
                    "CodecProfile": "LC",
                    "CodingMode": "CODING_MODE_2_0",
                    "RateControlMode": "CBR",
                    "RawFormat": "NONE",
                    "SampleRate": 48000,
                    "Specification": "MPEG4"
                },
                "Codec": "AAC"
            },
            "LanguageCodeControl": "FOLLOW_INPUT"
        }
    ],
    "ContainerSettings": {
        "Container": "MP4",
        "Mp4Settings": {
            "CslgAtom": "EXCLUDE",
            "FreeSpaceBox": "EXCLUDE",
            "MoovPlacement": "NORMAL"
        }
    },
    "VideoDescription": {
        "AfdSignaling": "NONE",
        "AntiAlias": "ENABLED",
        "CodecSettings": {
            "Codec": "H_265",
            "H265Settings": {
                "AdaptiveQuantization": "HIGH",
                "AlternateTransferFunctionSei": "DISABLED",
                "Bitrate": 10000000,
                "CodecLevel": "LEVEL_5",
                "CodecProfile": "MAIN_MAIN",
                "FlickerAdaptiveQuantization": "DISABLED",
                "FramerateControl": "SPECIFIED",
                "FramerateConversionAlgorithm": "DUPLICATE_DROP",
                "FramerateDenominator": 1001,
                "FramerateNumerator": 24000,
                "GopBReference": "ENABLED",
                "GopClosedCadence": 1,
                "GopSize": 48.0,
                "GopSizeUnits": "FRAMES",
                "HrdBufferInitialFillPercentage": 90,
                "HrdBufferSize": 20000000,
                "InterlaceMode": "PROGRESSIVE",
                "MinIInterval": 0,
                "NumberBFramesBetweenReferenceFrames": 3,
                "NumberReferenceFrames": 3,
                "ParControl": "SPECIFIED",
                "ParDenominator": 1,
                "ParNumerator": 1,
                "QualityTuningLevel": "SINGLE_PASS",
                "RateControlMode": "CBR",
                "SampleAdaptiveOffsetFilterMode": "ADAPTIVE",
                "SceneChangeDetect": "ENABLED",
                "Slices": 4,
                "SlowPal": "DISABLED",
                "SpatialAdaptiveQuantization": "ENABLED",
                "Telecine": "NONE",
                "TemporalAdaptiveQuantization": "ENABLED",
                "TemporalIds": "DISABLED",
                "Tiles": "ENABLED",
                "UnregisteredSeiTimecode": "DISABLED"
            }
        },
        "ColorMetadata": "INSERT",
        "DropFrameTimecode": "ENABLED",
        "Height": 2160,
        "RespondToAfd": "NONE",
        "ScalingBehavior": "DEFAULT",
        "Sharpness": 50,
        "TimecodeInsertion": "DISABLED",
        "VideoPreprocessors": {
            "Deinterlacer": {
                "Algorithm": "INTERPOLATE",
                "Control": "NORMAL",
                "Mode": "DEINTERLACE"
            }
        },
        "Width": 3840
    }
}
```

#### YAML<a name="aws-resource-mediaconvert-preset--examples--Output_Preset_Model_for_SettingsJson--yaml"></a>

```
---
AudioDescriptions:
- AudioType: 0
  AudioTypeControl: FOLLOW_INPUT
  CodecSettings:
    AacSettings:
      AudioDescriptionBroadcasterMix: NORMAL
      Bitrate: 160000
      CodecProfile: LC
      CodingMode: CODING_MODE_2_0
      RateControlMode: CBR
      RawFormat: NONE
      SampleRate: 48000
      Specification: MPEG4
    Codec: AAC
  LanguageCodeControl: FOLLOW_INPUT
ContainerSettings:
  Container: MP4
  Mp4Settings:
    CslgAtom: EXCLUDE
    FreeSpaceBox: EXCLUDE
    MoovPlacement: NORMAL
VideoDescription:
  AfdSignaling: NONE
  AntiAlias: ENABLED
  CodecSettings:
    Codec: H_265
    H265Settings:
      AdaptiveQuantization: HIGH
      AlternateTransferFunctionSei: DISABLED
      Bitrate: 10000000
      CodecLevel: LEVEL_5
      CodecProfile: MAIN_MAIN
      FlickerAdaptiveQuantization: DISABLED
      FramerateControl: SPECIFIED
      FramerateConversionAlgorithm: DUPLICATE_DROP
      FramerateDenominator: 1001
      FramerateNumerator: 24000
      GopBReference: ENABLED
      GopClosedCadence: 1
      GopSize: 48.0
      GopSizeUnits: FRAMES
      HrdBufferInitialFillPercentage: 90
      HrdBufferSize: 20000000
      InterlaceMode: PROGRESSIVE
      MinIInterval: 0
      NumberBFramesBetweenReferenceFrames: 3
      NumberReferenceFrames: 3
      ParControl: SPECIFIED
      ParDenominator: 1
      ParNumerator: 1
      QualityTuningLevel: SINGLE_PASS
      RateControlMode: CBR
      SampleAdaptiveOffsetFilterMode: ADAPTIVE
      SceneChangeDetect: ENABLED
      Slices: 4
      SlowPal: DISABLED
      SpatialAdaptiveQuantization: ENABLED
      Telecine: NONE
      TemporalAdaptiveQuantization: ENABLED
      TemporalIds: DISABLED
      Tiles: ENABLED
      UnregisteredSeiTimecode: DISABLED
  ColorMetadata: INSERT
  DropFrameTimecode: ENABLED
  Height: 2160
  RespondToAfd: NONE
  ScalingBehavior: DEFAULT
  Sharpness: 50
  TimecodeInsertion: DISABLED
  VideoPreprocessors:
    Deinterlacer:
      Algorithm: INTERPOLATE
      Control: NORMAL
      Mode: DEINTERLACE
  Width: 384
```