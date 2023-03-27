# AWS::Pinpoint::Segment<a name="aws-resource-pinpoint-segment"></a>

Updates the configuration, dimension, and other settings for an existing segment\.

## Syntax<a name="aws-resource-pinpoint-segment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-segment-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::Segment",
  "Properties" : {
      "[ApplicationId](#cfn-pinpoint-segment-applicationid)" : String,
      "[Dimensions](#cfn-pinpoint-segment-dimensions)" : SegmentDimensions,
      "[Name](#cfn-pinpoint-segment-name)" : String,
      "[SegmentGroups](#cfn-pinpoint-segment-segmentgroups)" : SegmentGroups,
      "[Tags](#cfn-pinpoint-segment-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-pinpoint-segment-syntax.yaml"></a>

```
Type: AWS::Pinpoint::Segment
Properties: 
  [ApplicationId](#cfn-pinpoint-segment-applicationid): String
  [Dimensions](#cfn-pinpoint-segment-dimensions): 
    SegmentDimensions
  [Name](#cfn-pinpoint-segment-name): String
  [SegmentGroups](#cfn-pinpoint-segment-segmentgroups): 
    SegmentGroups
  [Tags](#cfn-pinpoint-segment-tags): Json
```

## Properties<a name="aws-resource-pinpoint-segment-properties"></a>

`ApplicationId`  <a name="cfn-pinpoint-segment-applicationid"></a>
The unique identifier for the Amazon Pinpoint application that the segment is associated with\.  
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
A segment must have a name otherwise it will not appear in the Amazon Pinpoint console\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentGroups`  <a name="cfn-pinpoint-segment-segmentgroups"></a>
The segment group to use and the dimensions to apply to the group's base segments in order to build the segment\. A segment group can consist of zero or more base segments\. Your request can include only one segment group\.  
*Required*: No  
*Type*: [SegmentGroups](aws-properties-pinpoint-segment-segmentgroups.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pinpoint-segment-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-segment-return-values"></a>

### Ref<a name="aws-resource-pinpoint-segment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application that the segment is associated with\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-segment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-segment-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the segment\.

`SegmentId`  <a name="SegmentId-fn::getatt"></a>
The unique identifier for the segment\.