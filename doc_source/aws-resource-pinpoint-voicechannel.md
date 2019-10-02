# AWS::Pinpoint::VoiceChannel<a name="aws-resource-pinpoint-voicechannel"></a>

Updates the status and settings of the voice channel for an application\.

## Syntax<a name="aws-resource-pinpoint-voicechannel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-voicechannel-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::VoiceChannel",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-voicechannel-applicationid)" : String,
      "[Enabled](#cfn-pinpoint-voicechannel-enabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-pinpoint-voicechannel-syntax.yaml"></a>

```
Type: AWS::Pinpoint::VoiceChannel
Properties: 
  [ApplicationId](#cfn-pinpoint-voicechannel-applicationid): String
  [Enabled](#cfn-pinpoint-voicechannel-enabled): Boolean
```

## Properties<a name="aws-resource-pinpoint-voicechannel-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-voicechannel-applicationid"></a>
The unique ID of the Amazon Pinpoint app that you're setting up the voice channel for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Enabled`  <a name="cfn-pinpoint-voicechannel-enabled"></a>
Specifies whether to enable the voice channel for the application\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-voicechannel-return-values"></a>

### Ref<a name="aws-resource-pinpoint-voicechannel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Amazon Pinpoint app that the channel is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
