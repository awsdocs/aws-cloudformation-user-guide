# AWS::Pinpoint::Campaign AttributeDimension<a name="aws-properties-pinpoint-campaign-attributedimension"></a>

Specifies attribute\-based criteria for including or excluding endpoints from a segment\.

## Syntax<a name="aws-properties-pinpoint-campaign-attributedimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-attributedimension-syntax.json"></a>

```
{
  "[AttributeType](#cfn-pinpoint-campaign-attributedimension-attributetype)" : String,
  "[Values](#cfn-pinpoint-campaign-attributedimension-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pinpoint-campaign-attributedimension-syntax.yaml"></a>

```
  [AttributeType](#cfn-pinpoint-campaign-attributedimension-attributetype): String
  [Values](#cfn-pinpoint-campaign-attributedimension-values): 
    - String
```

## Properties<a name="aws-properties-pinpoint-campaign-attributedimension-properties"></a>

`AttributeType`  <a name="cfn-pinpoint-campaign-attributedimension-attributetype"></a>
The type of segment dimension to use\. Valid values are:  
+  `INCLUSIVE` – endpoints that have attributes matching the values are included in the segment\.
+  `EXCLUSIVE` – endpoints that have attributes matching the values are excluded from the segment\.
+  `CONTAINS` – endpoints that have attributes' substrings match the values are included in the segment\.
+  `BEFORE` – endpoints with attributes read as ISO\_INSTANT datetimes before the value are included in the segment\.
+  `AFTER` – endpoints with attributes read as ISO\_INSTANT datetimes after the value are included in the segment\.
+  `BETWEEN` – endpoints with attributes read as ISO\_INSTANT datetimes between the values are included in the segment\.
+  `ON` – endpoints with attributes read as ISO\_INSTANT dates on the value are included in the segment\. Time is ignored in this comparison\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-pinpoint-campaign-attributedimension-values"></a>
The criteria values to use for the segment dimension\. Depending on the value of the `AttributeType` property, endpoints are included or excluded from the segment if their attribute values match the criteria values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)