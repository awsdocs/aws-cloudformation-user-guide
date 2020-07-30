# AWS::Pinpoint::Segment SegmentGroups<a name="aws-properties-pinpoint-segment-segmentgroups"></a>

Specifies one or more segment groups that apply to a segment\. Each segment group consists of zero or more base segments and the dimensions that are applied to those base segments\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentgroups-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentgroups-syntax.json"></a>

```
{
  "[Groups](#cfn-pinpoint-segment-segmentgroups-groups)" : [ Groups, ... ],
  "[Include](#cfn-pinpoint-segment-segmentgroups-include)" : String
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentgroups-syntax.yaml"></a>

```
  [Groups](#cfn-pinpoint-segment-segmentgroups-groups): 
    - Groups
  [Include](#cfn-pinpoint-segment-segmentgroups-include): String
```

## Properties<a name="aws-properties-pinpoint-segment-segmentgroups-properties"></a>

`Groups`  <a name="cfn-pinpoint-segment-segmentgroups-groups"></a>
An array that defines the set of segment criteria to evaluate when handling segment groups for the segment\.  
*Required*: No  
*Type*: [List](aws-properties-pinpoint-segment-segmentgroups-groups.md) of [Groups](aws-properties-pinpoint-segment-segmentgroups-groups.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Include`  <a name="cfn-pinpoint-segment-segmentgroups-include"></a>
Specifies how to handle multiple segment groups for the segment\. For example, if the segment includes three segment groups, whether the resulting segment includes endpoints that match all, any, or none of the segment groups\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)