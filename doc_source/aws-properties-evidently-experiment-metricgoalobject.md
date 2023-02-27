# AWS::Evidently::Experiment MetricGoalObject<a name="aws-properties-evidently-experiment-metricgoalobject"></a>

Use this structure to tell Evidently whether higher or lower values are desired for a metric that is used in an experiment\.

## Syntax<a name="aws-properties-evidently-experiment-metricgoalobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-experiment-metricgoalobject-syntax.json"></a>

```
{
  "[DesiredChange](#cfn-evidently-experiment-metricgoalobject-desiredchange)" : String,
  "[EntityIdKey](#cfn-evidently-experiment-metricgoalobject-entityidkey)" : String,
  "[EventPattern](#cfn-evidently-experiment-metricgoalobject-eventpattern)" : String,
  "[MetricName](#cfn-evidently-experiment-metricgoalobject-metricname)" : String,
  "[UnitLabel](#cfn-evidently-experiment-metricgoalobject-unitlabel)" : String,
  "[ValueKey](#cfn-evidently-experiment-metricgoalobject-valuekey)" : String
}
```

### YAML<a name="aws-properties-evidently-experiment-metricgoalobject-syntax.yaml"></a>

```
  [DesiredChange](#cfn-evidently-experiment-metricgoalobject-desiredchange): String
  [EntityIdKey](#cfn-evidently-experiment-metricgoalobject-entityidkey): String
  [EventPattern](#cfn-evidently-experiment-metricgoalobject-eventpattern): String
  [MetricName](#cfn-evidently-experiment-metricgoalobject-metricname): String
  [UnitLabel](#cfn-evidently-experiment-metricgoalobject-unitlabel): String
  [ValueKey](#cfn-evidently-experiment-metricgoalobject-valuekey): String
```

## Properties<a name="aws-properties-evidently-experiment-metricgoalobject-properties"></a>

`DesiredChange`  <a name="cfn-evidently-experiment-metricgoalobject-desiredchange"></a>
`INCREASE` means that a variation with a higher number for this metric is performing better\.  
`DECREASE` means that a variation with a lower number for this metric is performing better\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityIdKey`  <a name="cfn-evidently-experiment-metricgoalobject-entityidkey"></a>
The entity, such as a user or session, that does an action that causes a metric value to be recorded\. An example is `userDetails.userID`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventPattern`  <a name="cfn-evidently-experiment-metricgoalobject-eventpattern"></a>
The EventBridge event pattern that defines how the metric is recorded\.  
For more information about EventBridge event patterns, see [Amazon EventBridge event patterns](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-evidently-experiment-metricgoalobject-metricname"></a>
A name for the metric\. It can include up to 255 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnitLabel`  <a name="cfn-evidently-experiment-metricgoalobject-unitlabel"></a>
A label for the units that the metric is measuring\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueKey`  <a name="cfn-evidently-experiment-metricgoalobject-valuekey"></a>
 The JSON path to reference the numerical metric value in the event\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)