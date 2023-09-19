# AWS::MediaPackageV2::OriginEndpointPolicy<a name="aws-resource-mediapackagev2-originendpointpolicy"></a>

Specifies the configuration parameters of a policy associated with a MediaPackage V2 origin endpoint\.

## Syntax<a name="aws-resource-mediapackagev2-originendpointpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackagev2-originendpointpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackageV2::OriginEndpointPolicy",
  "Properties" : {
      "[ChannelGroupName](#cfn-mediapackagev2-originendpointpolicy-channelgroupname)" : String,
      "[ChannelName](#cfn-mediapackagev2-originendpointpolicy-channelname)" : String,
      "[OriginEndpointName](#cfn-mediapackagev2-originendpointpolicy-originendpointname)" : String,
      "[Policy](#cfn-mediapackagev2-originendpointpolicy-policy)" : Json
    }
}
```

### YAML<a name="aws-resource-mediapackagev2-originendpointpolicy-syntax.yaml"></a>

```
Type: AWS::MediaPackageV2::OriginEndpointPolicy
Properties: 
  [ChannelGroupName](#cfn-mediapackagev2-originendpointpolicy-channelgroupname): String
  [ChannelName](#cfn-mediapackagev2-originendpointpolicy-channelname): String
  [OriginEndpointName](#cfn-mediapackagev2-originendpointpolicy-originendpointname): String
  [Policy](#cfn-mediapackagev2-originendpointpolicy-policy): Json
```

## Properties<a name="aws-resource-mediapackagev2-originendpointpolicy-properties"></a>

`ChannelGroupName`  <a name="cfn-mediapackagev2-originendpointpolicy-channelgroupname"></a>
The name of the channel group associated with the origin endpoint policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ChannelName`  <a name="cfn-mediapackagev2-originendpointpolicy-channelname"></a>
The channel name associated with the origin endpoint policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OriginEndpointName`  <a name="cfn-mediapackagev2-originendpointpolicy-originendpointname"></a>
The name of the origin endpoint associated with the origin endpoint policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-mediapackagev2-originendpointpolicy-policy"></a>
The policy associated with the origin endpoint\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackagev2-originendpointpolicy-return-values"></a>

### Ref<a name="aws-resource-mediapackagev2-originendpointpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `ChannelGroupName|ChannelName|OriginEndpointName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.