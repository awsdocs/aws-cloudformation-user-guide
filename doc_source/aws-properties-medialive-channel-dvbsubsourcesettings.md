# AWS::MediaLive::Channel DvbSubSourceSettings<a name="aws-properties-medialive-channel-dvbsubsourcesettings"></a>

Information about the DVB Sub captions to extract from the input\.

The parent of this entity is CaptionSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax.json"></a>

```
{
  "[OcrLanguage](#cfn-medialive-channel-dvbsubsourcesettings-ocrlanguage)" : String,
  "[Pid](#cfn-medialive-channel-dvbsubsourcesettings-pid)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-dvbsubsourcesettings-syntax.yaml"></a>

```
  [OcrLanguage](#cfn-medialive-channel-dvbsubsourcesettings-ocrlanguage): String
  [Pid](#cfn-medialive-channel-dvbsubsourcesettings-pid): Integer
```

## Properties<a name="aws-properties-medialive-channel-dvbsubsourcesettings-properties"></a>

`OcrLanguage`  <a name="cfn-medialive-channel-dvbsubsourcesettings-ocrlanguage"></a>
If you will configure a WebVTT caption description that references this caption selector, use this field to provide the language to consider when translating the image\-based source to text\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pid`  <a name="cfn-medialive-channel-dvbsubsourcesettings-pid"></a>
When using DVB\-Sub with burn\-in or SMPTE\-TT, use this PID for the source content\. It is unused for DVB\-Sub passthrough\. All DVB\-Sub content is passed through, regardless of selectors\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)