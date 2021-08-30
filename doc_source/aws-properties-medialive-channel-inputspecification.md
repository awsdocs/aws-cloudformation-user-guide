# AWS::MediaLive::Channel InputSpecification<a name="aws-properties-medialive-channel-inputspecification"></a>

The input specification for this channel\. It specifies the key characteristics of the inputs for this channel: the maximum bitrate, the resolution, and the codec\. 

This entity is at the top level in the channel\.

## Syntax<a name="aws-properties-medialive-channel-inputspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputspecification-syntax.json"></a>

```
{
  "[Codec](#cfn-medialive-channel-inputspecification-codec)" : String,
  "[MaximumBitrate](#cfn-medialive-channel-inputspecification-maximumbitrate)" : String,
  "[Resolution](#cfn-medialive-channel-inputspecification-resolution)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-inputspecification-syntax.yaml"></a>

```
  [Codec](#cfn-medialive-channel-inputspecification-codec): String
  [MaximumBitrate](#cfn-medialive-channel-inputspecification-maximumbitrate): String
  [Resolution](#cfn-medialive-channel-inputspecification-resolution): String
```

## Properties<a name="aws-properties-medialive-channel-inputspecification-properties"></a>

`Codec`  <a name="cfn-medialive-channel-inputspecification-codec"></a>
The codec to include in the input specification for this channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBitrate`  <a name="cfn-medialive-channel-inputspecification-maximumbitrate"></a>
The maximum input bitrate for any input attached to this channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resolution`  <a name="cfn-medialive-channel-inputspecification-resolution"></a>
The resolution for any input attached to this channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)