# AWS::MediaPackageV2::OriginEndpoint<a name="aws-resource-mediapackagev2-originendpoint"></a>

Specifies the configuration parameters for a MediaPackage V2 origin endpoint\.

## Syntax<a name="aws-resource-mediapackagev2-originendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediapackagev2-originendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::MediaPackageV2::OriginEndpoint",
  "Properties" : {
      "[ChannelGroupName](#cfn-mediapackagev2-originendpoint-channelgroupname)" : String,
      "[ChannelName](#cfn-mediapackagev2-originendpoint-channelname)" : String,
      "[ContainerType](#cfn-mediapackagev2-originendpoint-containertype)" : String,
      "[Description](#cfn-mediapackagev2-originendpoint-description)" : String,
      "[HlsManifests](#cfn-mediapackagev2-originendpoint-hlsmanifests)" : [ HlsManifestConfiguration, ... ],
      "[LowLatencyHlsManifests](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifests)" : [ LowLatencyHlsManifestConfiguration, ... ],
      "[OriginEndpointName](#cfn-mediapackagev2-originendpoint-originendpointname)" : String,
      "[Segment](#cfn-mediapackagev2-originendpoint-segment)" : Segment,
      "[StartoverWindowSeconds](#cfn-mediapackagev2-originendpoint-startoverwindowseconds)" : Integer,
      "[Tags](#cfn-mediapackagev2-originendpoint-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-mediapackagev2-originendpoint-syntax.yaml"></a>

```
Type: AWS::MediaPackageV2::OriginEndpoint
Properties: 
  [ChannelGroupName](#cfn-mediapackagev2-originendpoint-channelgroupname): String
  [ChannelName](#cfn-mediapackagev2-originendpoint-channelname): String
  [ContainerType](#cfn-mediapackagev2-originendpoint-containertype): String
  [Description](#cfn-mediapackagev2-originendpoint-description): String
  [HlsManifests](#cfn-mediapackagev2-originendpoint-hlsmanifests): 
    - HlsManifestConfiguration
  [LowLatencyHlsManifests](#cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifests): 
    - LowLatencyHlsManifestConfiguration
  [OriginEndpointName](#cfn-mediapackagev2-originendpoint-originendpointname): String
  [Segment](#cfn-mediapackagev2-originendpoint-segment): 
    Segment
  [StartoverWindowSeconds](#cfn-mediapackagev2-originendpoint-startoverwindowseconds): Integer
  [Tags](#cfn-mediapackagev2-originendpoint-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-mediapackagev2-originendpoint-properties"></a>

`ChannelGroupName`  <a name="cfn-mediapackagev2-originendpoint-channelgroupname"></a>
The name of the channel group associated with the origin endpoint configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ChannelName`  <a name="cfn-mediapackagev2-originendpoint-channelname"></a>
The channel name associated with the origin endpoint\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerType`  <a name="cfn-mediapackagev2-originendpoint-containertype"></a>
The container type associated with the origin endpoint configuration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CMAF | TS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-mediapackagev2-originendpoint-description"></a>
The description associated with the origin endpoint\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsManifests`  <a name="cfn-mediapackagev2-originendpoint-hlsmanifests"></a>
The HLS manfiests associated with the origin endpoint configuration\.  
*Required*: No  
*Type*: List of [HlsManifestConfiguration](aws-properties-mediapackagev2-originendpoint-hlsmanifestconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LowLatencyHlsManifests`  <a name="cfn-mediapackagev2-originendpoint-lowlatencyhlsmanifests"></a>
The low\-latency HLS \(LL\-HLS\) manifests associated with the origin endpoint\.  
*Required*: No  
*Type*: List of [LowLatencyHlsManifestConfiguration](aws-properties-mediapackagev2-originendpoint-lowlatencyhlsmanifestconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginEndpointName`  <a name="cfn-mediapackagev2-originendpoint-originendpointname"></a>
The name of the origin endpoint associated with the origin endpoint configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Segment`  <a name="cfn-mediapackagev2-originendpoint-segment"></a>
The segment associated with the origin endpoint\.  
*Required*: No  
*Type*: [Segment](aws-properties-mediapackagev2-originendpoint-segment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartoverWindowSeconds`  <a name="cfn-mediapackagev2-originendpoint-startoverwindowseconds"></a>
The size of the window \(in seconds\) to specify a window of the live stream that's available for on\-demand viewing\. Viewers can start\-over or catch\-up on content that falls within the window\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-mediapackagev2-originendpoint-tags"></a>
The tags associated with the origin endpoint\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-mediapackagev2-originendpoint-return-values"></a>

### Ref<a name="aws-resource-mediapackagev2-originendpoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `arn:aws:mediapackagev2:region:AccountId:ChannelGroup|ChannelGroupName|Channel|ChannelName|OriginEndpoint|OriginEndpointName`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediapackagev2-originendpoint-return-values-fn--getatt"></a>

The attributes of the origin endpoint\. You can only use the `GetAtt` function for `readOnly` properties\. For example, you can use the `GetAtt` function to retrieve the read\-only `CreatedAt` property\.

#### <a name="aws-resource-mediapackagev2-originendpoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the origin endpoint\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of the creation of the origin endpoint\.

`ModifiedAt`  <a name="ModifiedAt-fn::getatt"></a>
The timestamp of the modification of the origin endpoint\.