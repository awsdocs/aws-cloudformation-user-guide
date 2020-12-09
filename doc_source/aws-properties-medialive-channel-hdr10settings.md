# AWS::MediaLive::Channel Hdr10Settings<a name="aws-properties-medialive-channel-hdr10settings"></a>

Hdr10 Settings

## Syntax<a name="aws-properties-medialive-channel-hdr10settings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hdr10settings-syntax.json"></a>

```
{
  "[MaxCll](#cfn-medialive-channel-hdr10settings-maxcll)" : Integer,
  "[MaxFall](#cfn-medialive-channel-hdr10settings-maxfall)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-hdr10settings-syntax.yaml"></a>

```
  [MaxCll](#cfn-medialive-channel-hdr10settings-maxcll): Integer
  [MaxFall](#cfn-medialive-channel-hdr10settings-maxfall): Integer
```

## Properties<a name="aws-properties-medialive-channel-hdr10settings-properties"></a>

`MaxCll`  <a name="cfn-medialive-channel-hdr10settings-maxcll"></a>
Maximum Content Light Level An integer metadata value defining the maximum light level, in nits, of any single pixel within an encoded HDR video stream or file\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFall`  <a name="cfn-medialive-channel-hdr10settings-maxfall"></a>
Maximum Frame Average Light Level An integer metadata value defining the maximum average light level, in nits, for any single frame within an encoded HDR video stream or file\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)