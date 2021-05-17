# AWS::MediaLive::Channel DvbNitSettings<a name="aws-properties-medialive-channel-dvbnitsettings"></a>

The configuration of DVB NIT\.

The parent of this entity is M2tsSettings\.

## Syntax<a name="aws-properties-medialive-channel-dvbnitsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbnitsettings-syntax.json"></a>

```
{
  "[NetworkId](#cfn-medialive-channel-dvbnitsettings-networkid)" : Integer,
  "[NetworkName](#cfn-medialive-channel-dvbnitsettings-networkname)" : String,
  "[RepInterval](#cfn-medialive-channel-dvbnitsettings-repinterval)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-dvbnitsettings-syntax.yaml"></a>

```
  [NetworkId](#cfn-medialive-channel-dvbnitsettings-networkid): Integer
  [NetworkName](#cfn-medialive-channel-dvbnitsettings-networkname): String
  [RepInterval](#cfn-medialive-channel-dvbnitsettings-repinterval): Integer
```

## Properties<a name="aws-properties-medialive-channel-dvbnitsettings-properties"></a>

`NetworkId`  <a name="cfn-medialive-channel-dvbnitsettings-networkid"></a>
The numeric value placed in the Network Information Table \(NIT\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkName`  <a name="cfn-medialive-channel-dvbnitsettings-networkname"></a>
The network name text placed in the networkNameDescriptor inside the Network Information Table \(NIT\)\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepInterval`  <a name="cfn-medialive-channel-dvbnitsettings-repinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)