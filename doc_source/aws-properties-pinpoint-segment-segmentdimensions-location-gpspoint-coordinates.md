# AWS::Pinpoint::Segment Coordinates<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates"></a>

Specifies the GPS coordinates of a location\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-syntax.json"></a>

```
{
  "[Latitude](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-latitude)" : Double,
  "[Longitude](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-longitude)" : Double
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-syntax.yaml"></a>

```
  [Latitude](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-latitude): Double
  [Longitude](#cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-longitude): Double
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-properties"></a>

`Latitude`  <a name="cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-latitude"></a>
The latitude coordinate of the location\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Longitude`  <a name="cfn-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates-longitude"></a>
The longitude coordinate of the location\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)