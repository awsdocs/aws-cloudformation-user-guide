# AWS::LookoutMetrics::AnomalyDetector MetricSource<a name="aws-properties-lookoutmetrics-anomalydetector-metricsource"></a>

Contains information about how the source data should be interpreted\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-metricsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-metricsource-syntax.json"></a>

```
{
  "[AppFlowConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-appflowconfig)" : AppFlowConfig,
  "[CloudwatchConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-cloudwatchconfig)" : CloudwatchConfig,
  "[RDSSourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-rdssourceconfig)" : RDSSourceConfig,
  "[RedshiftSourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-redshiftsourceconfig)" : RedshiftSourceConfig,
  "[S3SourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-s3sourceconfig)" : S3SourceConfig
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-metricsource-syntax.yaml"></a>

```
  [AppFlowConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-appflowconfig): 
    AppFlowConfig
  [CloudwatchConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-cloudwatchconfig): 
    CloudwatchConfig
  [RDSSourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-rdssourceconfig): 
    RDSSourceConfig
  [RedshiftSourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-redshiftsourceconfig): 
    RedshiftSourceConfig
  [S3SourceConfig](#cfn-lookoutmetrics-anomalydetector-metricsource-s3sourceconfig): 
    S3SourceConfig
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-metricsource-properties"></a>

`AppFlowConfig`  <a name="cfn-lookoutmetrics-anomalydetector-metricsource-appflowconfig"></a>
Details about an AppFlow datasource\.  
*Required*: No  
*Type*: [AppFlowConfig](aws-properties-lookoutmetrics-anomalydetector-appflowconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudwatchConfig`  <a name="cfn-lookoutmetrics-anomalydetector-metricsource-cloudwatchconfig"></a>
Details about an Amazon CloudWatch monitoring datasource\.  
*Required*: No  
*Type*: [CloudwatchConfig](aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RDSSourceConfig`  <a name="cfn-lookoutmetrics-anomalydetector-metricsource-rdssourceconfig"></a>
Details about an Amazon Relational Database Service \(RDS\) datasource\.  
*Required*: No  
*Type*: [RDSSourceConfig](aws-properties-lookoutmetrics-anomalydetector-rdssourceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedshiftSourceConfig`  <a name="cfn-lookoutmetrics-anomalydetector-metricsource-redshiftsourceconfig"></a>
Details about an Amazon Redshift database datasource\.  
*Required*: No  
*Type*: [RedshiftSourceConfig](aws-properties-lookoutmetrics-anomalydetector-redshiftsourceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3SourceConfig`  <a name="cfn-lookoutmetrics-anomalydetector-metricsource-s3sourceconfig"></a>
Contains information about the configuration of the S3 bucket that contains source files\.  
*Required*: No  
*Type*: [S3SourceConfig](aws-properties-lookoutmetrics-anomalydetector-s3sourceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)