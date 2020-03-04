# AWS::Pinpoint::Segment SourceSegments<a name="aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments"></a>

Specifies the base segment to build a segment on\. A base segment, also referred to as a *source segment*, defines the initial population of endpoints for a segment\. When you add dimensions to a segment, Amazon Pinpoint filters the base segment by using the dimensions that you specify\. You can specify more than one dimensional segment or only one imported segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments-syntax.json"></a>

```
{
  "[Id](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-id)" : String,
  "[Version](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-version)" : Integer
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments-syntax.yaml"></a>

```
  [Id](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-id): String
  [Version](#cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-version): Integer
```

## Properties<a name="aws-properties-pinpoint-segment-segmentgroups-groups-sourcesegments-properties"></a>

`Id`  <a name="cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-id"></a>
The unique identifier for the segment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-pinpoint-segment-segmentgroups-groups-sourcesegments-version"></a>
The version number of the segment\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)