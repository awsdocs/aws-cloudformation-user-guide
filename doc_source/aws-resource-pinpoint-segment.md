# AWS::Pinpoint::Segment<a name="aws-resource-pinpoint-segment"></a>

Creates a new segment for an application or updates the configuration, dimension, and other settings for an existing segment that's associated with an application\.

## Syntax<a name="aws-resource-pinpoint-segment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-segment-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::Segment",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-segment-applicationid)" : String,
      "[Dimensions](#cfn-pinpoint-segment-dimensions)" : [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md),
      "[Name](#cfn-pinpoint-segment-name)" : String,
      "[SegmentGroups](#cfn-pinpoint-segment-segmentgroups)" : [SegmentGroups](aws-properties-pinpoint-segment-segmentgroups.md)
    }
}
```

### YAML<a name="aws-resource-pinpoint-segment-syntax.yaml"></a>

```
Type: AWS::Pinpoint::Segment
Properties: 
  [ApplicationId](#cfn-pinpoint-segment-applicationid): String
  [Dimensions](#cfn-pinpoint-segment-dimensions): 
    [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md)
  [Name](#cfn-pinpoint-segment-name): String
  [SegmentGroups](#cfn-pinpoint-segment-segmentgroups): 
    [SegmentGroups](aws-properties-pinpoint-segment-segmentgroups.md)
```

## Properties<a name="aws-resource-pinpoint-segment-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-segment-applicationid"></a>
The unique ID of the Amazon Pinpoint app that the segment is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Dimensions`  <a name="cfn-pinpoint-segment-dimensions"></a>
The criteria that define the dimensions for the segment\.  
*Required*: No  
*Type*: [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-pinpoint-segment-name"></a>
The name of the segment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentGroups`  <a name="cfn-pinpoint-segment-segmentgroups"></a>
The segment group, which consists of zero or more base segments, to use and the dimensions to apply to those base segments in order to build the segment\. Your request can include only one segment group\.  
*Required*: No  
*Type*: [SegmentGroups](aws-properties-pinpoint-segment-segmentgroups.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-pinpoint-segment-return-values"></a>

### Ref<a name="aws-resource-pinpoint-segment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Amazon Pinpoint app that the segment is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-segment-return-values-fn--getatt"></a>

#### <a name="aws-resource-pinpoint-segment-return-values-fn--getatt-fn--getatt"></a>

`SegmentId`  <a name="SegmentId-fn::getatt"></a>
The unique identifier for the segment\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
