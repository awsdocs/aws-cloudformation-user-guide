# AWS::MediaPackageV2::ChannelGroup<a name="aws-resource-mediapackagev2-channelgroup"></a>

Specifies the configuraiton for a MediaPackage V2 channel group\.

## Syntax<a name="aws-resource-mediapackagev2-channelgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackagev2-channelgroup-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackageV2::ChannelGroup",
  "Properties" : {
      "[ChannelGroupName](#cfn-mediapackagev2-channelgroup-channelgroupname)" : String,
      "[Description](#cfn-mediapackagev2-channelgroup-description)" : String,
      "[Tags](#cfn-mediapackagev2-channelgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackagev2-channelgroup-syntax.yaml"></a>

```
Type: AWS::MediaPackageV2::ChannelGroup
Properties: 
  [ChannelGroupName](#cfn-mediapackagev2-channelgroup-channelgroupname): String
  [Description](#cfn-mediapackagev2-channelgroup-description): String
  [Tags](#cfn-mediapackagev2-channelgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackagev2-channelgroup-properties"></a>

`ChannelGroupName`  <a name="cfn-mediapackagev2-channelgroup-channelgroupname"></a>
The name of the channel group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-mediapackagev2-channelgroup-description"></a>
The configuration for a MediaPackage V2 channel group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediapackagev2-channelgroup-tags"></a>
The tags associated with the channel group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackagev2-channelgroup-return-values"></a>

### Ref<a name="aws-resource-mediapackagev2-channelgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `arn:aws:mediapackagev2:region:AccountId:ChannelGroup|ChannelGroupName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediapackagev2-channelgroup-return-values-fn--getatt"></a>

The attributes of the channel group\. You can only use the `GetAtt` function for `readOnly` properties\. For example, you can use the `GetAtt` function to retrieve the read\-only `CreatedAt` property\.

#### <a name="aws-resource-mediapackagev2-channelgroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the channel group\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of the creation of the channel group\.

`EgressDomain`  <a name="EgressDomain-fn::getatt"></a>
The egress domain of the channel group\.

`ModifiedAt`  <a name="ModifiedAt-fn::getatt"></a>
The timestamp of the modification of the channel group\.