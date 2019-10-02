# AWS::Pinpoint::Segment GPSPoint<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint"></a>

The GPS coordinates of the endpoint location\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-syntax.json"></a>

```
{
  "[Coordinates](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates)" : [Coordinates](aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates.md),
  "[RangeInKilometers](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-rangeinkilometers)" : Double
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-syntax.yaml"></a>

```
  [Coordinates](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates): 
    [Coordinates](aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates.md)
  [RangeInKilometers](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-rangeinkilometers): Double
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-properties"></a>

`Coordinates`  <a name="cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates"></a>
The GPS coordinates to measure distance from\.  
*Required*: Yes  
*Type*: [Coordinates](aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeInKilometers`  <a name="cfn-pinpoint-segment-segmentdimensions-location-gpspoint-rangeinkilometers"></a>
The range, in kilometers, from the GPS coordinates\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
