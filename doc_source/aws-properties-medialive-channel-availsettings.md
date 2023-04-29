# AWS::MediaLive::Channel AvailSettings<a name="aws-properties-medialive-channel-availsettings"></a>

The settings for the ad avail setup in the output\.

The parent of this entity is AvailConfiguration\.

## Syntax<a name="aws-properties-medialive-channel-availsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-availsettings-syntax.json"></a>

```
{
  "[Esam](#cfn-medialive-channel-availsettings-esam)" : Esam,
  "[Scte35SpliceInsert](#cfn-medialive-channel-availsettings-scte35spliceinsert)" : Scte35SpliceInsert,
  "[Scte35TimeSignalApos](#cfn-medialive-channel-availsettings-scte35timesignalapos)" : Scte35TimeSignalApos
}
```

### YAML<a name="aws-properties-medialive-channel-availsettings-syntax.yaml"></a>

```
  [Esam](#cfn-medialive-channel-availsettings-esam): 
    Esam
  [Scte35SpliceInsert](#cfn-medialive-channel-availsettings-scte35spliceinsert): 
    Scte35SpliceInsert
  [Scte35TimeSignalApos](#cfn-medialive-channel-availsettings-scte35timesignalapos): 
    Scte35TimeSignalApos
```

## Properties<a name="aws-properties-medialive-channel-availsettings-properties"></a>

`Esam`  <a name="cfn-medialive-channel-availsettings-esam"></a>
Property description not available\.  
*Required*: No  
*Type*: [Esam](aws-properties-medialive-channel-esam.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35SpliceInsert`  <a name="cfn-medialive-channel-availsettings-scte35spliceinsert"></a>
The setup for SCTE\-35 splice insert handling\.  
*Required*: No  
*Type*: [Scte35SpliceInsert](aws-properties-medialive-channel-scte35spliceinsert.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scte35TimeSignalApos`  <a name="cfn-medialive-channel-availsettings-scte35timesignalapos"></a>
The setup for SCTE\-35 time signal APOS handling\.  
*Required*: No  
*Type*: [Scte35TimeSignalApos](aws-properties-medialive-channel-scte35timesignalapos.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)