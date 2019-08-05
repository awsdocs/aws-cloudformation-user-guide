# AWS::Pinpoint::Segment Groups<a name="aws-properties-pinpoint-segment-segmentgroups-groups"></a>

An array that defines the set of segment criteria to evaluate when handling segment groups for the segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentgroups-groups-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentgroups-groups-syntax.json"></a>

```
{
  "[Dimensions](#cfn-pinpoint-segment-segmentgroups-groups-dimensions)" : [ [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md), ... ],
  "[SourceSegments](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments)" : [ [SourceSegments](aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments.md), ... ],
  "[SourceType](#cfn-pinpoint-segment-segmentgroups-groups-sourcetype)" : String,
  "[Type](#cfn-pinpoint-segment-segmentgroups-groups-type)" : String
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentgroups-groups-syntax.yaml"></a>

```
  [Dimensions](#cfn-pinpoint-segment-segmentgroups-groups-dimensions):
    - [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md)
  [SourceSegments](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments):
    - [SourceSegments](aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments.md)
  [SourceType](#cfn-pinpoint-segment-segmentgroups-groups-sourcetype): String
  [Type](#cfn-pinpoint-segment-segmentgroups-groups-type): String
```

## Properties<a name="aws-properties-pinpoint-segment-segmentgroups-groups-properties"></a>

`Dimensions`  <a name="cfn-pinpoint-segment-segmentgroups-groups-dimensions"></a>
An array that defines the dimensions to include or exclude from the segment\.
*Required*: No
*Type*: List of [SegmentDimensions](aws-properties-pinpoint-segment-segmentdimensions.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSegments`  <a name="cfn-pinpoint-segment-segmentgroups-groups-sourcesegments"></a>
The base segment to build the segment on\. A base segment, also called a *source segment*, defines the initial population of endpoints for a segment\. When you add dimensions to the segment, Amazon Pinpoint filters the base segment by using the dimensions that you specify\.
You can specify more than one dimensional segment or only one imported segment\. If you specify an imported segment, the segment size estimate that displays on the Amazon Pinpoint console indicates the size of the imported segment without any filters applied to it\.
*Required*: No
*Type*: [List](aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments.md) of [SourceSegments](aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceType`  <a name="cfn-pinpoint-segment-segmentgroups-groups-sourcetype"></a>
Specifies how to handle multiple base segments for the segment\. For example, if you specify three base segments for the segment, whether the resulting segment is based on all, any, or none of the base segments\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-pinpoint-segment-segmentgroups-groups-type"></a>
Specifies how to handle multiple dimensions for the segment\. For example, if you specify three dimensions for the segment, whether the resulting segment includes endpoints that match all, any, or none of the dimensions\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
