# AWS::LookoutMetrics::AnomalyDetector CloudwatchConfig<a name="aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig"></a>

Details about an Amazon CloudWatch datasource\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig-syntax.json"></a>

```
{
  "[RoleArn](#cfn-lookoutmetrics-anomalydetector-cloudwatchconfig-rolearn)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig-syntax.yaml"></a>

```
  [RoleArn](#cfn-lookoutmetrics-anomalydetector-cloudwatchconfig-rolearn): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-cloudwatchconfig-properties"></a>

`RoleArn`  <a name="cfn-lookoutmetrics-anomalydetector-cloudwatchconfig-rolearn"></a>
An IAM role that gives Amazon Lookout for Metrics permission to access data in Amazon CloudWatch\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)