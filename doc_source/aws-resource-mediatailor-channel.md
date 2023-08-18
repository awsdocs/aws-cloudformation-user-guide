# AWS::MediaTailor::Channel<a name="aws-resource-mediatailor-channel"></a>

The configuration parameters for a channel\. For information about MediaTailor channels, see [Working with channels](https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-channels.html) in the *MediaTailor User Guide*\.

## Syntax<a name="aws-resource-mediatailor-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediatailor-channel-syntax.json"></a>

```
{
  "Type" : "AWS::MediaTailor::Channel",
  "Properties" : {
      "[ChannelName](#cfn-mediatailor-channel-channelname)" : String,
      "[FillerSlate](#cfn-mediatailor-channel-fillerslate)" : SlateSource,
      "[LogConfiguration](#cfn-mediatailor-channel-logconfiguration)" : LogConfigurationForChannel,
      "[Outputs](#cfn-mediatailor-channel-outputs)" : [ RequestOutputItem, ... ],
      "[PlaybackMode](#cfn-mediatailor-channel-playbackmode)" : String,
      "[Tags](#cfn-mediatailor-channel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Tier](#cfn-mediatailor-channel-tier)" : String
    }
}
```

### YAML<a name="aws-resource-mediatailor-channel-syntax.yaml"></a>

```
Type: AWS::MediaTailor::Channel
Properties: 
  [ChannelName](#cfn-mediatailor-channel-channelname): String
  [FillerSlate](#cfn-mediatailor-channel-fillerslate): 
    SlateSource
  [LogConfiguration](#cfn-mediatailor-channel-logconfiguration): 
    LogConfigurationForChannel
  [Outputs](#cfn-mediatailor-channel-outputs): 
    - RequestOutputItem
  [PlaybackMode](#cfn-mediatailor-channel-playbackmode): String
  [Tags](#cfn-mediatailor-channel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Tier](#cfn-mediatailor-channel-tier): String
```

## Properties<a name="aws-resource-mediatailor-channel-properties"></a>

`ChannelName`  <a name="cfn-mediatailor-channel-channelname"></a>
The name of the channel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FillerSlate`  <a name="cfn-mediatailor-channel-fillerslate"></a>
The slate used to fill gaps between programs in the schedule\. You must configure filler slate if your channel uses the `LINEAR` `PlaybackMode`\. MediaTailor doesn't support filler slate for channels using the `LOOP` `PlaybackMode`\.  
*Required*: No  
*Type*: [SlateSource](aws-properties-mediatailor-channel-slatesource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfiguration`  <a name="cfn-mediatailor-channel-logconfiguration"></a>
The log configuration\.  
*Required*: No  
*Type*: [LogConfigurationForChannel](aws-properties-mediatailor-channel-logconfigurationforchannel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-mediatailor-channel-outputs"></a>
The channel's output properties\.  
*Required*: Yes  
*Type*: List of [RequestOutputItem](aws-properties-mediatailor-channel-requestoutputitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaybackMode`  <a name="cfn-mediatailor-channel-playbackmode"></a>
The type of playback mode for this channel\.  
`LINEAR` \- Programs play back\-to\-back only once\.  
`LOOP` \- Programs play back\-to\-back in an endless loop\. When the last program in the schedule plays, playback loops back to the first program in the schedule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediatailor-channel-tags"></a>
The tags to assign to the channel\. Tags are key\-value pairs that you can associate with Amazon resources to help with organization, access control, and cost tracking\. For more information, see [Tagging AWS Elemental MediaTailor Resources](https://docs.aws.amazon.com/mediatailor/latest/ug/tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tier`  <a name="cfn-mediatailor-channel-tier"></a>
The tier for this channel\. STANDARD tier channels can contain live programs\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-mediatailor-channel-return-values"></a>

### Ref<a name="aws-resource-mediatailor-channel-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediatailor-channel-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediatailor-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.