# AWS::MediaLive::Channel NielsenWatermarksSettings<a name="aws-properties-medialive-channel-nielsenwatermarkssettings"></a>

Settings to configure Nielsen Watermarks in the audio encode\.

The parent of this entity is AudioWatermarkSettings\.

## Syntax<a name="aws-properties-medialive-channel-nielsenwatermarkssettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-nielsenwatermarkssettings-syntax.json"></a>

```
{
  "[NielsenCbetSettings](#cfn-medialive-channel-nielsenwatermarkssettings-nielsencbetsettings)" : NielsenCBET,
  "[NielsenDistributionType](#cfn-medialive-channel-nielsenwatermarkssettings-nielsendistributiontype)" : String,
  "[NielsenNaesIiNwSettings](#cfn-medialive-channel-nielsenwatermarkssettings-nielsennaesiinwsettings)" : NielsenNaesIiNw
}
```

### YAML<a name="aws-properties-medialive-channel-nielsenwatermarkssettings-syntax.yaml"></a>

```
  [NielsenCbetSettings](#cfn-medialive-channel-nielsenwatermarkssettings-nielsencbetsettings): 
    NielsenCBET
  [NielsenDistributionType](#cfn-medialive-channel-nielsenwatermarkssettings-nielsendistributiontype): String
  [NielsenNaesIiNwSettings](#cfn-medialive-channel-nielsenwatermarkssettings-nielsennaesiinwsettings): 
    NielsenNaesIiNw
```

## Properties<a name="aws-properties-medialive-channel-nielsenwatermarkssettings-properties"></a>

`NielsenCbetSettings`  <a name="cfn-medialive-channel-nielsenwatermarkssettings-nielsencbetsettings"></a>
Complete these fields only if you want to insert watermarks of type Nielsen CBET  
*Required*: No  
*Type*: [NielsenCBET](aws-properties-medialive-channel-nielsencbet.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenDistributionType`  <a name="cfn-medialive-channel-nielsenwatermarkssettings-nielsendistributiontype"></a>
Choose the distribution types that you want to assign to the watermarks: \- PROGRAM\_CONTENT \- FINAL\_DISTRIBUTOR  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NielsenNaesIiNwSettings`  <a name="cfn-medialive-channel-nielsenwatermarkssettings-nielsennaesiinwsettings"></a>
Complete these fields only if you want to insert watermarks of type Nielsen NAES II \(N2\) and Nielsen NAES VI \(NW\)\.  
*Required*: No  
*Type*: [NielsenNaesIiNw](aws-properties-medialive-channel-nielsennaesiinw.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)