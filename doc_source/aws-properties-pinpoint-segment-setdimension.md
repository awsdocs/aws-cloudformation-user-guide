# AWS::Pinpoint::Segment SetDimension<a name="aws-properties-pinpoint-segment-setdimension"></a>

Specifies the dimension type and values for a segment dimension\.

## Syntax<a name="aws-properties-pinpoint-segment-setdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-setdimension-syntax.json"></a>

```
{
  "[DimensionType](#cfn-pinpoint-segment-setdimension-dimensiontype)" : String,
  "[Values](#cfn-pinpoint-segment-setdimension-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pinpoint-segment-setdimension-syntax.yaml"></a>

```
  [DimensionType](#cfn-pinpoint-segment-setdimension-dimensiontype): String
  [Values](#cfn-pinpoint-segment-setdimension-values): 
    - String
```

## Properties<a name="aws-properties-pinpoint-segment-setdimension-properties"></a>

`DimensionType`  <a name="cfn-pinpoint-segment-setdimension-dimensiontype"></a>
The type of segment dimension to use\. Valid values are: `INCLUSIVE`, endpoints that match the criteria are included in the segment; and, `EXCLUSIVE`, endpoints that match the criteria are excluded from the segment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-pinpoint-segment-setdimension-values"></a>
The criteria values to use for the segment dimension\. Depending on the value of the `DimensionType` property, endpoints are included or excluded from the segment if their values match the criteria values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)