# AWS::LookoutMetrics::AnomalyDetector MetricSet<a name="aws-properties-lookoutmetrics-anomalydetector-metricset"></a>

Contains information about a dataset\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-metricset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-metricset-syntax.json"></a>

```
{
  "[DimensionList](#cfn-lookoutmetrics-anomalydetector-metricset-dimensionlist)" : [ String, ... ],
  "[MetricList](#cfn-lookoutmetrics-anomalydetector-metricset-metriclist)" : [ Metric, ... ],
  "[MetricSetDescription](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetdescription)" : String,
  "[MetricSetFrequency](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetfrequency)" : String,
  "[MetricSetName](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetname)" : String,
  "[MetricSource](#cfn-lookoutmetrics-anomalydetector-metricset-metricsource)" : MetricSource,
  "[Offset](#cfn-lookoutmetrics-anomalydetector-metricset-offset)" : Integer,
  "[TimestampColumn](#cfn-lookoutmetrics-anomalydetector-metricset-timestampcolumn)" : TimestampColumn,
  "[Timezone](#cfn-lookoutmetrics-anomalydetector-metricset-timezone)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-metricset-syntax.yaml"></a>

```
  [DimensionList](#cfn-lookoutmetrics-anomalydetector-metricset-dimensionlist): 
    - String
  [MetricList](#cfn-lookoutmetrics-anomalydetector-metricset-metriclist): 
    - Metric
  [MetricSetDescription](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetdescription): String
  [MetricSetFrequency](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetfrequency): String
  [MetricSetName](#cfn-lookoutmetrics-anomalydetector-metricset-metricsetname): String
  [MetricSource](#cfn-lookoutmetrics-anomalydetector-metricset-metricsource): 
    MetricSource
  [Offset](#cfn-lookoutmetrics-anomalydetector-metricset-offset): Integer
  [TimestampColumn](#cfn-lookoutmetrics-anomalydetector-metricset-timestampcolumn): 
    TimestampColumn
  [Timezone](#cfn-lookoutmetrics-anomalydetector-metricset-timezone): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-metricset-properties"></a>

`DimensionList`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-dimensionlist"></a>
A list of the fields you want to treat as dimensions\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricList`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-metriclist"></a>
A list of metrics that the dataset will contain\.  
*Required*: Yes  
*Type*: List of [Metric](aws-properties-lookoutmetrics-anomalydetector-metric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSetDescription`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-metricsetdescription"></a>
A description of the dataset you are creating\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSetFrequency`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-metricsetfrequency"></a>
The frequency with which the source data will be analyzed for anomalies\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSetName`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-metricsetname"></a>
The name of the dataset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSource`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-metricsource"></a>
Contains information about how the source data should be interpreted\.  
*Required*: Yes  
*Type*: [MetricSource](aws-properties-lookoutmetrics-anomalydetector-metricsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Offset`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-offset"></a>
After an interval ends, the amount of seconds that the detector waits before importing data\. Offset is only supported for S3, Redshift, Athena and datasources\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampColumn`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-timestampcolumn"></a>
Contains information about the column used for tracking time in your source data\.  
*Required*: No  
*Type*: [TimestampColumn](aws-properties-lookoutmetrics-anomalydetector-timestampcolumn.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timezone`  <a name="cfn-lookoutmetrics-anomalydetector-metricset-timezone"></a>
The time zone in which your source data was recorded\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)