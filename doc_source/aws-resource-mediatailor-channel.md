# AWS::MediaTailor::Channel<a name="aws-resource-mediatailor-channel"></a>

<a name="aws-resource-mediatailor-channel-description"></a>The `AWS::MediaTailor::Channel` resource Property description not available\. for MediaTailor\.

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
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FillerSlate`  <a name="cfn-mediatailor-channel-fillerslate"></a>
Property description not available\.  
*Required*: No  
*Type*: [SlateSource](aws-properties-mediatailor-channel-slatesource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfiguration`  <a name="cfn-mediatailor-channel-logconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [LogConfigurationForChannel](aws-properties-mediatailor-channel-logconfigurationforchannel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Outputs`  <a name="cfn-mediatailor-channel-outputs"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [RequestOutputItem](aws-properties-mediatailor-channel-requestoutputitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaybackMode`  <a name="cfn-mediatailor-channel-playbackmode"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediatailor-channel-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tier`  <a name="cfn-mediatailor-channel-tier"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-mediatailor-channel-return-values"></a>

### Ref<a name="aws-resource-mediatailor-channel-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-mediatailor-channel-return-values-fn--getatt"></a>

#### <a name="aws-resource-mediatailor-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.