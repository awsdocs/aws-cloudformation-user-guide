# AWS::Evidently::Launch MetricDefinitionObject<a name="aws-properties-evidently-launch-metricdefinitionobject"></a>

This structure defines a metric that you want to use to evaluate the variations during a launch or experiment\.

## Syntax<a name="aws-properties-evidently-launch-metricdefinitionobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-launch-metricdefinitionobject-syntax.json"></a>

```
{
  "[EntityIdKey](#cfn-evidently-launch-metricdefinitionobject-entityidkey)" : String,
  "[EventPattern](#cfn-evidently-launch-metricdefinitionobject-eventpattern)" : String,
  "[MetricName](#cfn-evidently-launch-metricdefinitionobject-metricname)" : String,
  "[UnitLabel](#cfn-evidently-launch-metricdefinitionobject-unitlabel)" : String,
  "[ValueKey](#cfn-evidently-launch-metricdefinitionobject-valuekey)" : String
}
```

### YAML<a name="aws-properties-evidently-launch-metricdefinitionobject-syntax.yaml"></a>

```
  [EntityIdKey](#cfn-evidently-launch-metricdefinitionobject-entityidkey): String
  [EventPattern](#cfn-evidently-launch-metricdefinitionobject-eventpattern): String
  [MetricName](#cfn-evidently-launch-metricdefinitionobject-metricname): String
  [UnitLabel](#cfn-evidently-launch-metricdefinitionobject-unitlabel): String
  [ValueKey](#cfn-evidently-launch-metricdefinitionobject-valuekey): String
```

## Properties<a name="aws-properties-evidently-launch-metricdefinitionobject-properties"></a>

`EntityIdKey`  <a name="cfn-evidently-launch-metricdefinitionobject-entityidkey"></a>
The entity, such as a user or session, that does an action that causes a metric value to be recorded\. An example is `userDetails.userID`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventPattern`  <a name="cfn-evidently-launch-metricdefinitionobject-eventpattern"></a>
The EventBridge event pattern that defines how the metric is recorded\.  
For more information about EventBridge event patterns, see [Amazon EventBridge event patterns](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-evidently-launch-metricdefinitionobject-metricname"></a>
A name for the metric\. It can include up to 255 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnitLabel`  <a name="cfn-evidently-launch-metricdefinitionobject-unitlabel"></a>
A label for the units that the metric is measuring\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueKey`  <a name="cfn-evidently-launch-metricdefinitionobject-valuekey"></a>
The value that is tracked to produce the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)