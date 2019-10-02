# AWS::Pinpoint::Segment Demographic<a name="aws-properties-pinpoint-segment-segmentdimensions-demographic"></a>

The demographic\-based criteria, such as device platform, for the segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-demographic-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-demographic-syntax.json"></a>

```
{
  "[AppVersion](#cfn-pinpoint-segment-segmentdimensions-demographic-appversion)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md),
  "[Channel](#cfn-pinpoint-segment-segmentdimensions-demographic-channel)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md),
  "[DeviceType](#cfn-pinpoint-segment-segmentdimensions-demographic-devicetype)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md),
  "[Make](#cfn-pinpoint-segment-segmentdimensions-demographic-make)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md),
  "[Model](#cfn-pinpoint-segment-segmentdimensions-demographic-model)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md),
  "[Platform](#cfn-pinpoint-segment-segmentdimensions-demographic-platform)" : [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-demographic-syntax.yaml"></a>

```
  [AppVersion](#cfn-pinpoint-segment-segmentdimensions-demographic-appversion): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
  [Channel](#cfn-pinpoint-segment-segmentdimensions-demographic-channel): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
  [DeviceType](#cfn-pinpoint-segment-segmentdimensions-demographic-devicetype): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
  [Make](#cfn-pinpoint-segment-segmentdimensions-demographic-make): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
  [Model](#cfn-pinpoint-segment-segmentdimensions-demographic-model): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
  [Platform](#cfn-pinpoint-segment-segmentdimensions-demographic-platform): 
    [SetDimension](aws-properties-pinpoint-segment-setdimension.md)
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-demographic-properties"></a>

`AppVersion`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-appversion"></a>
The app version criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Channel`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-channel"></a>
The channel criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceType`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-devicetype"></a>
The device type criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Make`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-make"></a>
The device make criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Model`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-model"></a>
The device model criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Platform`  <a name="cfn-pinpoint-segment-segmentdimensions-demographic-platform"></a>
The device platform criteria for the segment\.  
*Required*: No  
*Type*: [SetDimension](aws-properties-pinpoint-segment-setdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
