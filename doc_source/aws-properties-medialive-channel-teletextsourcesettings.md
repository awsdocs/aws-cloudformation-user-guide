# AWS::MediaLive::Channel TeletextSourceSettings<a name="aws-properties-medialive-channel-teletextsourcesettings"></a>

Information about the Teletext captions to extract from the input\.

The parent of this entity is CaptionSelectorSettings\.

## Syntax<a name="aws-properties-medialive-channel-teletextsourcesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-teletextsourcesettings-syntax.json"></a>

```
{
  "[PageNumber](#cfn-medialive-channel-teletextsourcesettings-pagenumber)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-teletextsourcesettings-syntax.yaml"></a>

```
  [PageNumber](#cfn-medialive-channel-teletextsourcesettings-pagenumber): String
```

## Properties<a name="aws-properties-medialive-channel-teletextsourcesettings-properties"></a>

`PageNumber`  <a name="cfn-medialive-channel-teletextsourcesettings-pagenumber"></a>
Specifies the Teletext page number within the data stream from which to extract captions\. The range is 0x100 \(256\) to 0x8FF \(2303\)\. This is unused for passthrough\. It should be specified as a hexadecimal string with no "0x" prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)