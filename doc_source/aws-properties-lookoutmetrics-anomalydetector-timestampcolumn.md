# AWS::LookoutMetrics::AnomalyDetector TimestampColumn<a name="aws-properties-lookoutmetrics-anomalydetector-timestampcolumn"></a>

Contains information about the column used to track time in a source data file\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-timestampcolumn-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-timestampcolumn-syntax.json"></a>

```
{
  "[ColumnFormat](#cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnformat)" : String,
  "[ColumnName](#cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnname)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-timestampcolumn-syntax.yaml"></a>

```
  [ColumnFormat](#cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnformat): String
  [ColumnName](#cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnname): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-timestampcolumn-properties"></a>

`ColumnFormat`  <a name="cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnformat"></a>
The format of the timestamp column\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnName`  <a name="cfn-lookoutmetrics-anomalydetector-timestampcolumn-columnname"></a>
The name of the timestamp column\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)