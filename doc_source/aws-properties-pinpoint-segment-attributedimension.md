# AWS::Pinpoint::Segment AttributeDimension<a name="aws-properties-pinpoint-segment-attributedimension"></a>

Specifies attribute\-based criteria for including or excluding endpoints from a segment\.

## Syntax<a name="aws-properties-pinpoint-segment-attributedimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-attributedimension-syntax.json"></a>

```
{
  "[AttributeType](#cfn-pinpoint-segment-attributedimension-attributetype)" : String,
  "[Values](#cfn-pinpoint-segment-attributedimension-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pinpoint-segment-attributedimension-syntax.yaml"></a>

```
  [AttributeType](#cfn-pinpoint-segment-attributedimension-attributetype): String
  [Values](#cfn-pinpoint-segment-attributedimension-values): 
    - String
```

## Properties<a name="aws-properties-pinpoint-segment-attributedimension-properties"></a>

`AttributeType`  <a name="cfn-pinpoint-segment-attributedimension-attributetype"></a>
The type of segment dimension to use\. Valid values are: `INCLUSIVE`, endpoints that match the criteria are included in the segment; and, `EXCLUSIVE`, endpoints that match the criteria are excluded from the segment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-pinpoint-segment-attributedimension-values"></a>
The criteria values to use for the segment dimension\. Depending on the value of the `AttributeType` property, endpoints are included or excluded from the segment if their attribute values match the criteria values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)