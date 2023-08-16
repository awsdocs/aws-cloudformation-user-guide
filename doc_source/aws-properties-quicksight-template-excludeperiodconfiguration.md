# AWS::QuickSight::Template ExcludePeriodConfiguration<a name="aws-properties-quicksight-template-excludeperiodconfiguration"></a>

The exclude period of `TimeRangeFilter` or `RelativeDatesFilter`\.

## Syntax<a name="aws-properties-quicksight-template-excludeperiodconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-excludeperiodconfiguration-syntax.json"></a>

```
{
  "[Amount](#cfn-quicksight-template-excludeperiodconfiguration-amount)" : Double,
  "[Granularity](#cfn-quicksight-template-excludeperiodconfiguration-granularity)" : String,
  "[Status](#cfn-quicksight-template-excludeperiodconfiguration-status)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-excludeperiodconfiguration-syntax.yaml"></a>

```
  [Amount](#cfn-quicksight-template-excludeperiodconfiguration-amount): Double
  [Granularity](#cfn-quicksight-template-excludeperiodconfiguration-granularity): String
  [Status](#cfn-quicksight-template-excludeperiodconfiguration-status): String
```

## Properties<a name="aws-properties-quicksight-template-excludeperiodconfiguration-properties"></a>

`Amount`  <a name="cfn-quicksight-template-excludeperiodconfiguration-amount"></a>
The amount or number of the exclude period\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Granularity`  <a name="cfn-quicksight-template-excludeperiodconfiguration-granularity"></a>
The granularity or unit \(day, month, year\) of the exclude period\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-template-excludeperiodconfiguration-status"></a>
The status of the exclude period\. Choose from the following options:  
+  `ENABLED` 
+  `DISABLED` 
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)