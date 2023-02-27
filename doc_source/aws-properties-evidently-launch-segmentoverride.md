# AWS::Evidently::Launch SegmentOverride<a name="aws-properties-evidently-launch-segmentoverride"></a>

Use this structure to specify different traffic splits for one or more audience *segments*\. A segment is a portion of your audience that share one or more characteristics\. Examples could be Chrome browser users, users in Europe, or Firefox browser users in Europe who also fit other criteria that your application collects, such as age\.

For more information, see [ Use segments to focus your audience](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments.html)\.

This sructure is an array of up to six segment override objects\. Each of these objects specifies a segment that you have already created, and defines the traffic split for that segment\.

## Syntax<a name="aws-properties-evidently-launch-segmentoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-launch-segmentoverride-syntax.json"></a>

```
{
  "[EvaluationOrder](#cfn-evidently-launch-segmentoverride-evaluationorder)" : Integer,
  "[Segment](#cfn-evidently-launch-segmentoverride-segment)" : String,
  "[Weights](#cfn-evidently-launch-segmentoverride-weights)" : [ GroupToWeight, ... ]
}
```

### YAML<a name="aws-properties-evidently-launch-segmentoverride-syntax.yaml"></a>

```
  [EvaluationOrder](#cfn-evidently-launch-segmentoverride-evaluationorder): Integer
  [Segment](#cfn-evidently-launch-segmentoverride-segment): String
  [Weights](#cfn-evidently-launch-segmentoverride-weights): 
    - GroupToWeight
```

## Properties<a name="aws-properties-evidently-launch-segmentoverride-properties"></a>

`EvaluationOrder`  <a name="cfn-evidently-launch-segmentoverride-evaluationorder"></a>
A number indicating the order to use to evaluate segment overrides, if there are more than one\. Segment overrides with lower numbers are evaluated first\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Segment`  <a name="cfn-evidently-launch-segmentoverride-segment"></a>
The ARN of the segment to use for this override\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weights`  <a name="cfn-evidently-launch-segmentoverride-weights"></a>
The traffic allocation percentages among the feature variations to assign to this segment\. This is a set of key\-value pairs\. The keys are variation names\. The values represent the amount of traffic to allocate to that variation for this segment\. This is expressed in thousandths of a percent, so a weight of 50000 represents 50% of traffic\.  
*Required*: Yes  
*Type*: List of [GroupToWeight](aws-properties-evidently-launch-grouptoweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)