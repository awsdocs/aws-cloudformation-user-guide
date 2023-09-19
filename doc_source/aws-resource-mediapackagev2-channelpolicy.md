# AWS::MediaPackageV2::ChannelPolicy<a name="aws-resource-mediapackagev2-channelpolicy"></a>

Specifies the configuration parameters of a MediaPackage V2 channel policy\.

## Syntax<a name="aws-resource-mediapackagev2-channelpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackagev2-channelpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackageV2::ChannelPolicy",
  "Properties" : {
      "[ChannelGroupName](#cfn-mediapackagev2-channelpolicy-channelgroupname)" : String,
      "[ChannelName](#cfn-mediapackagev2-channelpolicy-channelname)" : String,
      "[Policy](#cfn-mediapackagev2-channelpolicy-policy)" : Json
    }
}
```

### YAML<a name="aws-resource-mediapackagev2-channelpolicy-syntax.yaml"></a>

```
Type: AWS::MediaPackageV2::ChannelPolicy
Properties: 
  [ChannelGroupName](#cfn-mediapackagev2-channelpolicy-channelgroupname): String
  [ChannelName](#cfn-mediapackagev2-channelpolicy-channelname): String
  [Policy](#cfn-mediapackagev2-channelpolicy-policy): Json
```

## Properties<a name="aws-resource-mediapackagev2-channelpolicy-properties"></a>

`ChannelGroupName`  <a name="cfn-mediapackagev2-channelpolicy-channelgroupname"></a>
The name of the channel group associated with the channel policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ChannelName`  <a name="cfn-mediapackagev2-channelpolicy-channelname"></a>
The name of the channel associated with the channel policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-mediapackagev2-channelpolicy-policy"></a>
The policy associated with the channel\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackagev2-channelpolicy-return-values"></a>

### Ref<a name="aws-resource-mediapackagev2-channelpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `ChannelGroupName|ChannelName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.