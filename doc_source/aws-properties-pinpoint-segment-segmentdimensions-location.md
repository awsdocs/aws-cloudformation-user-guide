# AWS::Pinpoint::Segment Location<a name="aws-properties-pinpoint-segment-segmentdimensions-location"></a>

Specifies location\-based criteria, such as country or region, for a segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-location-syntax.json"></a>

```
{
  "[Country](#cfn-pinpoint-segment-segmentdimensions-location-country)" : SetDimension,
  "[GPSPoint](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint)" : GPSPoint
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-location-syntax.yaml"></a>

```
  [Country](#cfn-pinpoint-segment-segmentdimensions-location-country): 
    SetDimension
  [GPSPoint](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint): 
    GPSPoint
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-location-properties"></a>

`Country`  <a name="cfn-pinpoint-segment-segmentdimensions-location-country"></a>
The country or region code, in ISO 3166\-1 alpha\-2 format, for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GPSPoint`  <a name="cfn-pinpoint-segment-segmentdimensions-location-gpspoint"></a>
The GPS location and range for the segment\.  
*Required*: No  
*Type*: [GPSPoint](aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)