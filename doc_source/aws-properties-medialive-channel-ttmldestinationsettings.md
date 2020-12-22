# AWS::MediaLive::Channel TtmlDestinationSettings<a name="aws-properties-medialive-channel-ttmldestinationsettings"></a>

The setup of TTML captions in the output\.

The parent of this entity is CaptionDestinationSettings\.

## Syntax<a name="aws-properties-medialive-channel-ttmldestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-ttmldestinationsettings-syntax.json"></a>

```
{
  "[StyleControl](#cfn-medialive-channel-ttmldestinationsettings-stylecontrol)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-ttmldestinationsettings-syntax.yaml"></a>

```
  [StyleControl](#cfn-medialive-channel-ttmldestinationsettings-stylecontrol): String
```

## Properties<a name="aws-properties-medialive-channel-ttmldestinationsettings-properties"></a>

`StyleControl`  <a name="cfn-medialive-channel-ttmldestinationsettings-stylecontrol"></a>
When set to passthrough, passes through style and position information from a TTML\-like input source \(TTML, SMPTE\-TT, CFF\-TT\) to the CFF\-TT output or TTML output\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)