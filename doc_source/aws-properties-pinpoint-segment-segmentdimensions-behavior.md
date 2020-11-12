# AWS::Pinpoint::Segment Behavior<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior"></a>

Specifies behavior\-based criteria, such as how recently users have used your app, for a segment\.

## Syntax<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax.json"></a>

```
{
  "[Recency](#cfn-pinpoint-segment-segmentdimensions-behavior-recency)" : Recency
}
```

### YAML<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-syntax.yaml"></a>

```
  [Recency](#cfn-pinpoint-segment-segmentdimensions-behavior-recency): 
    Recency
```

## Properties<a name="aws-properties-pinpoint-segment-segmentdimensions-behavior-properties"></a>

`Recency`  <a name="cfn-pinpoint-segment-segmentdimensions-behavior-recency"></a>
The dimension settings that are based on how recently an endpoint was active\.  
*Required*: No  
*Type*: [Recency](aws-properties-pinpoint-segment-segmentdimensions-behavior-recency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)