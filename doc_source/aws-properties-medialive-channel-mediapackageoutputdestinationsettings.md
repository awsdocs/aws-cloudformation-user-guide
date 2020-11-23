# AWS::MediaLive::Channel MediaPackageOutputDestinationSettings<a name="aws-properties-medialive-channel-mediapackageoutputdestinationsettings"></a>

This element specifies the destination information for one MediaPackage output group\. Create an array of one MediaPackageOutputDestinationSettings for each output group\. This element belongs to OutputDestination\.

## Syntax<a name="aws-properties-medialive-channel-mediapackageoutputdestinationsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-mediapackageoutputdestinationsettings-syntax.json"></a>

```
{
  "[ChannelId](#cfn-medialive-channel-mediapackageoutputdestinationsettings-channelid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-mediapackageoutputdestinationsettings-syntax.yaml"></a>

```
  [ChannelId](#cfn-medialive-channel-mediapackageoutputdestinationsettings-channelid): String
```

## Properties<a name="aws-properties-medialive-channel-mediapackageoutputdestinationsettings-properties"></a>

`ChannelId`  <a name="cfn-medialive-channel-mediapackageoutputdestinationsettings-channelid"></a>
ID of the channel in MediaPackage that is the destination for this output group\. This ID associates this destination information with the appropriate MediaPackage output group\. In that output group, enter a value in the destination field\. Then enter the same value in this channelID field\. Make sure that you then use this same ID when you create the channel in AWS Elemental MediaPackage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)