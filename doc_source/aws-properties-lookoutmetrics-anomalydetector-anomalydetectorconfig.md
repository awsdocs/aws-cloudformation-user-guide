# AWS::LookoutMetrics::AnomalyDetector AnomalyDetectorConfig<a name="aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig"></a>

Contains information about a detector's configuration\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig-syntax.json"></a>

```
{
  "[AnomalyDetectorFrequency](#cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig-anomalydetectorfrequency)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig-syntax.yaml"></a>

```
  [AnomalyDetectorFrequency](#cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig-anomalydetectorfrequency): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig-properties"></a>

`AnomalyDetectorFrequency`  <a name="cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig-anomalydetectorfrequency"></a>
The frequency at which the detector analyzes its source data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)