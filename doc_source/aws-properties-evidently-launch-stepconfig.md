# AWS::Evidently::Launch StepConfig<a name="aws-properties-evidently-launch-stepconfig"></a>

A structure that defines when each step of the launch is to start, and how much launch traffic is to be allocated to each variation during each step\.

## Syntax<a name="aws-properties-evidently-launch-stepconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-launch-stepconfig-syntax.json"></a>

```
{
  "[GroupWeights](#cfn-evidently-launch-stepconfig-groupweights)" : [ GroupToWeight, ... ],
  "[SegmentOverrides](#cfn-evidently-launch-stepconfig-segmentoverrides)" : [ SegmentOverride, ... ],
  "[StartTime](#cfn-evidently-launch-stepconfig-starttime)" : String
}
```

### YAML<a name="aws-properties-evidently-launch-stepconfig-syntax.yaml"></a>

```
  [GroupWeights](#cfn-evidently-launch-stepconfig-groupweights): 
    - GroupToWeight
  [SegmentOverrides](#cfn-evidently-launch-stepconfig-segmentoverrides): 
    - SegmentOverride
  [StartTime](#cfn-evidently-launch-stepconfig-starttime): String
```

## Properties<a name="aws-properties-evidently-launch-stepconfig-properties"></a>

`GroupWeights`  <a name="cfn-evidently-launch-stepconfig-groupweights"></a>
An array of structures that define how much launch traffic to allocate to each launch group during this step of the launch\.  
*Required*: Yes  
*Type*: List of [GroupToWeight](aws-properties-evidently-launch-grouptoweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentOverrides`  <a name="cfn-evidently-launch-stepconfig-segmentoverrides"></a>
An array of structures that you can use to specify different traffic splits for one or more audience *segments*\. A segment is a portion of your audience that share one or more characteristics\. Examples could be Chrome browser users, users in Europe, or Firefox browser users in Europe who also fit other criteria that your application collects, such as age\.  
For more information, see [ Use segments to focus your audience](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments.html)\.  
*Required*: No  
*Type*: List of [SegmentOverride](aws-properties-evidently-launch-segmentoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-evidently-launch-stepconfig-starttime"></a>
The date and time to start this step of the launch\. Use UTC format, `yyyy-MM-ddTHH:mm:ssZ`\. For example, `2025-11-25T23:59:59Z`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)