# AWS::Pinpoint::Segment SegmentDimensions<a name="aws-properties-pinpoint-segment-segmentdimensions"></a>

Specifies the dimension settings for a segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-syntax.json"></a>

```
{
  "[Attributes](#cfn-pinpoint-segment-segmentdimensions-attributes)" : Json,
  "[Behavior](#cfn-pinpoint-segment-segmentdimensions-behavior)" : Behavior,
  "[Demographic](#cfn-pinpoint-segment-segmentdimensions-demographic)" : Demographic,
  "[Location](#cfn-pinpoint-segment-segmentdimensions-location)" : Location,
  "[Metrics](#cfn-pinpoint-segment-segmentdimensions-metrics)" : Json,
  "[UserAttributes](#cfn-pinpoint-segment-segmentdimensions-userattributes)" : Json
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-syntax.yaml"></a>

```
  [Attributes](#cfn-pinpoint-segment-segmentdimensions-attributes): Json
  [Behavior](#cfn-pinpoint-segment-segmentdimensions-behavior): 
    Behavior
  [Demographic](#cfn-pinpoint-segment-segmentdimensions-demographic): 
    Demographic
  [Location](#cfn-pinpoint-segment-segmentdimensions-location): 
    Location
  [Metrics](#cfn-pinpoint-segment-segmentdimensions-metrics): Json
  [UserAttributes](#cfn-pinpoint-segment-segmentdimensions-userattributes): Json
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-properties"></a>

`Attributes`  <a name="cfn-pinpoint-segment-segmentdimensions-attributes"></a>
One or more custom attributes to use as criteria for the segment\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Behavior`  <a name="cfn-pinpoint-segment-segmentdimensions-behavior"></a>
The behavior\-based criteria, such as how recently users have used your app, for the segment\.  
*Required*: No  
*Type*: [Behavior](aws-properties-pinpoint-segment-segmentdimensions-behavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Demographic`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic"></a>
The demographic\-based criteria, such as device platform, for the segment\.  
*Required*: No  
*Type*: [Demographic](aws-properties-pinpoint-segment-segmentdimensions-demographic.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-pinpoint-segment-segmentdimensions-location"></a>
The location\-based criteria, such as region or GPS coordinates, for the segment\.  
*Required*: No  
*Type*: [Location](aws-properties-pinpoint-segment-segmentdimensions-location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metrics`  <a name="cfn-pinpoint-segment-segmentdimensions-metrics"></a>
One or more custom metrics to use as criteria for the segment\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserAttributes`  <a name="cfn-pinpoint-segment-segmentdimensions-userattributes"></a>
One or more custom user attributes to use as criteria for the segment\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)