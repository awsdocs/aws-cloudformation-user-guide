# AWS::MediaLive::Channel FecOutputSettings<a name="aws-properties-medialive-channel-fecoutputsettings"></a>

The settings for FEC\.

The parent of this entity is UdpOutputSettings\.

## Syntax<a name="aws-properties-medialive-channel-fecoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-fecoutputsettings-syntax.json"></a>

```
{
  "[ColumnDepth](#cfn-medialive-channel-fecoutputsettings-columndepth)" : Integer,
  "[IncludeFec](#cfn-medialive-channel-fecoutputsettings-includefec)" : String,
  "[RowLength](#cfn-medialive-channel-fecoutputsettings-rowlength)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-fecoutputsettings-syntax.yaml"></a>

```
  [ColumnDepth](#cfn-medialive-channel-fecoutputsettings-columndepth): Integer
  [IncludeFec](#cfn-medialive-channel-fecoutputsettings-includefec): String
  [RowLength](#cfn-medialive-channel-fecoutputsettings-rowlength): Integer
```

## Properties<a name="aws-properties-medialive-channel-fecoutputsettings-properties"></a>

`ColumnDepth`  <a name="cfn-medialive-channel-fecoutputsettings-columndepth"></a>
The parameter D from SMPTE 2022\-1\. The height of the FEC protection matrix\. The number of transport stream packets per column error correction packet\. The number must be between 4 and 20, inclusive\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeFec`  <a name="cfn-medialive-channel-fecoutputsettings-includefec"></a>
Enables column only or column and row\-based FEC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowLength`  <a name="cfn-medialive-channel-fecoutputsettings-rowlength"></a>
The parameter L from SMPTE 2022\-1\. The width of the FEC protection matrix\. Must be between 1 and 20, inclusive\. If only Column FEC is used, then larger values increase robustness\. If Row FEC is used, then this is the number of transport stream packets per row error correction packet, and the value must be between 4 and 20, inclusive, if includeFec is columnAndRow\. If includeFec is column, this value must be 1 to 20, inclusive\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)