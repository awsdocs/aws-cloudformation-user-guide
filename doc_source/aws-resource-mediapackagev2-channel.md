# AWS::MediaPackageV2::Channel<a name="aws-resource-mediapackagev2-channel"></a>

Creates a channel to receive content\.

After it's created, a channel provides static input URLs\. These URLs remain the same throughout the lifetime of the channel, regardless of any failures or upgrades that might occur\. Use these URLs to configure the outputs of your upstream encoder\.

## Syntax<a name="aws-resource-mediapackagev2-channel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackagev2-channel-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackageV2::Channel",
  "Properties" : {
      "[ChannelGroupName](#cfn-mediapackagev2-channel-channelgroupname)" : String,
      "[ChannelName](#cfn-mediapackagev2-channel-channelname)" : String,
      "[Description](#cfn-mediapackagev2-channel-description)" : String,
      "[Tags](#cfn-mediapackagev2-channel-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackagev2-channel-syntax.yaml"></a>

```
Type: AWS::MediaPackageV2::Channel
Properties: 
  [ChannelGroupName](#cfn-mediapackagev2-channel-channelgroupname): String
  [ChannelName](#cfn-mediapackagev2-channel-channelname): String
  [Description](#cfn-mediapackagev2-channel-description): String
  [Tags](#cfn-mediapackagev2-channel-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackagev2-channel-properties"></a>

`ChannelGroupName`  <a name="cfn-mediapackagev2-channel-channelgroupname"></a>
The name of the channel group associated with the channel configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ChannelName`  <a name="cfn-mediapackagev2-channel-channelname"></a>
The name of the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-mediapackagev2-channel-description"></a>
The description of the channel\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediapackagev2-channel-tags"></a>
The tags associated with the channel\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackagev2-channel-return-values"></a>

### Ref<a name="aws-resource-mediapackagev2-channel-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `arn:aws:mediapackagev2:region:AccountId:ChannelGroup/ChannelGroupName/Channel/ChannelName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediapackagev2-channel-return-values-fn--getatt"></a>

The attributes of the channelsf\. You can only use the `GetAtt` function for `readOnly` properties\. For example, you can use the `GetAtt` function to retrieve the read\-only `CreatedAt` property\.

#### <a name="aws-resource-mediapackagev2-channel-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the channel\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of the ccreation of the channel\.

`IngestEndpoints`  <a name="IngestEndpoints-fn::getatt"></a>
The ingest endpoints associated with the channel\.

`ModifiedAt`  <a name="ModifiedAt-fn::getatt"></a>
The timestamp of the modification of the channel\.