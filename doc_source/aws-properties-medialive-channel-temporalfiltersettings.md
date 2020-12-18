# AWS::MediaLive::Channel TemporalFilterSettings<a name="aws-properties-medialive-channel-temporalfiltersettings"></a>

Temporal Filter Settings

## Syntax<a name="aws-properties-medialive-channel-temporalfiltersettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-temporalfiltersettings-syntax.json"></a>

```
{
  "[PostFilterSharpening](#cfn-medialive-channel-temporalfiltersettings-postfiltersharpening)" : String,
  "[Strength](#cfn-medialive-channel-temporalfiltersettings-strength)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-temporalfiltersettings-syntax.yaml"></a>

```
  [PostFilterSharpening](#cfn-medialive-channel-temporalfiltersettings-postfiltersharpening): String
  [Strength](#cfn-medialive-channel-temporalfiltersettings-strength): String
```

## Properties<a name="aws-properties-medialive-channel-temporalfiltersettings-properties"></a>

`PostFilterSharpening`  <a name="cfn-medialive-channel-temporalfiltersettings-postfiltersharpening"></a>
If you enable this filter, the results are the following: \- If the source content is noisy \(it contains excessive digital artifacts\), the filter cleans up the source\. \- If the source content is already clean, the filter tends to decrease the bitrate, especially when the rate control mode is QVBR\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Strength`  <a name="cfn-medialive-channel-temporalfiltersettings-strength"></a>
Choose a filter strength\. We recommend a strength of 1 or 2\. A higher strength might take out good information, resulting in an image that is overly soft\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)