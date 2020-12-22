# AWS::MediaLive::Channel DvbTdtSettings<a name="aws-properties-medialive-channel-dvbtdtsettings"></a>

The DVB Time and Date Table \(TDT\)\.

The parent of this entity is M2tsSettings\.

## Syntax<a name="aws-properties-medialive-channel-dvbtdtsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbtdtsettings-syntax.json"></a>

```
{
  "[RepInterval](#cfn-medialive-channel-dvbtdtsettings-repinterval)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-dvbtdtsettings-syntax.yaml"></a>

```
  [RepInterval](#cfn-medialive-channel-dvbtdtsettings-repinterval): Integer
```

## Properties<a name="aws-properties-medialive-channel-dvbtdtsettings-properties"></a>

`RepInterval`  <a name="cfn-medialive-channel-dvbtdtsettings-repinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)