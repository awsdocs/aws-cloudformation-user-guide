# AWS::Pinpoint::Segment Behavior<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior"></a>

Specifies behavior\-based criteria for the segment, such as how recently users have used your app\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax.json"></a>

```
{
  "[Recency](#cfn-pinpoint-segment-segmentdimensions-behavior-recency)" : [Recency](aws-properties-pinpoint-segment-segmentdimensions-behavior-recency.md)
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax.yaml"></a>

```
  [Recency](#cfn-pinpoint-segment-segmentdimensions-behavior-recency): 
    [Recency](aws-properties-pinpoint-segment-segmentdimensions-behavior-recency.md)
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-properties"></a>

`Recency`  <a name="cfn-pinpoint-segment-segmentdimensions-behavior-recency"></a>
Specifies how recently segment members were active\.  
*Required*: No  
*Type*: [Recency](aws-properties-pinpoint-segment-segmentdimensions-behavior-recency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)