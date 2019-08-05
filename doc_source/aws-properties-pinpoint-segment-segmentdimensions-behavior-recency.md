# AWS::Pinpoint::Segment Recency<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-recency"></a>

Specifies how recently segment members were active\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-recency-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-recency-syntax.json"></a>

```
{
  "[Duration](#cfn-pinpoint-segment-segmentdimensions-behavior-recency-duration)" : String,
  "[RecencyType](#cfn-pinpoint-segment-segmentdimensions-behavior-recency-recencytype)" : String
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-recency-syntax.yaml"></a>

```
  [Duration](#cfn-pinpoint-segment-segmentdimensions-behavior-recency-duration): String
  [RecencyType](#cfn-pinpoint-segment-segmentdimensions-behavior-recency-recencytype): String
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-recency-properties"></a>

`Duration`  <a name="cfn-pinpoint-segment-segmentdimensions-behavior-recency-duration"></a>
The duration to use when determining which users have been active or inactive with your app\.
Possible values: `HR_24` \| `DAY_7` \| `DAY_14` \| `DAY_30`\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecencyType`  <a name="cfn-pinpoint-segment-segmentdimensions-behavior-recency-recencytype"></a>
The type of recency dimension to use for the segment\. Valid values are: `ACTIVE` and `INACTIVE`\. If the value is `ACTIVE`, the segment includes users who have used your app within the specified duration are included in the segment\. If the value is `INACTIVE`, the segment includes users who haven't used your app within the specified duration are included in the segment\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
