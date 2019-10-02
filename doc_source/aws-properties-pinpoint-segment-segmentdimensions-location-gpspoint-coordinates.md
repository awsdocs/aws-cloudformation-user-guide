# AWS::Pinpoint::Segment Coordinates<a name="aws-properties-pinpoint-segment-segmentdimensions-location-gpspoint-coordinates"></a>

The latitude and longitude of the location\.

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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
