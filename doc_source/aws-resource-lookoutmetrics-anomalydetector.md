# AWS::LookoutMetrics::AnomalyDetector<a name="aws-resource-lookoutmetrics-anomalydetector"></a>

The `AWS::LookoutMetrics::AnomalyDetector` type creates an anomaly detector\.

## Syntax<a name="aws-resource-lookoutmetrics-anomalydetector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lookoutmetrics-anomalydetector-syntax.json"></a>

```
{
  "Type" : "AWS::LookoutMetrics::AnomalyDetector",
  "Properties" : {
      "[AnomalyDetectorConfig](#cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig)" : AnomalyDetectorConfig,
      "[AnomalyDetectorDescription](#cfn-lookoutmetrics-anomalydetector-anomalydetectordescription)" : String,
      "[AnomalyDetectorName](#cfn-lookoutmetrics-anomalydetector-anomalydetectorname)" : String,
      "[KmsKeyArn](#cfn-lookoutmetrics-anomalydetector-kmskeyarn)" : String,
      "[MetricSetList](#cfn-lookoutmetrics-anomalydetector-metricsetlist)" : [ MetricSet, ... ]
    }
}
```

### YAML<a name="aws-resource-lookoutmetrics-anomalydetector-syntax.yaml"></a>

```
Type: AWS::LookoutMetrics::AnomalyDetector
Properties: 
  [AnomalyDetectorConfig](#cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig): 
    AnomalyDetectorConfig
  [AnomalyDetectorDescription](#cfn-lookoutmetrics-anomalydetector-anomalydetectordescription): String
  [AnomalyDetectorName](#cfn-lookoutmetrics-anomalydetector-anomalydetectorname): String
  [KmsKeyArn](#cfn-lookoutmetrics-anomalydetector-kmskeyarn): String
  [MetricSetList](#cfn-lookoutmetrics-anomalydetector-metricsetlist): 
    - MetricSet
```

## Properties<a name="aws-resource-lookoutmetrics-anomalydetector-properties"></a>

`AnomalyDetectorConfig`  <a name="cfn-lookoutmetrics-anomalydetector-anomalydetectorconfig"></a>
Contains information about the configuration of the anomaly detector\.  
*Required*: Yes  
*Type*: [AnomalyDetectorConfig](aws-properties-lookoutmetrics-anomalydetector-anomalydetectorconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnomalyDetectorDescription`  <a name="cfn-lookoutmetrics-anomalydetector-anomalydetectordescription"></a>
A description of the detector\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnomalyDetectorName`  <a name="cfn-lookoutmetrics-anomalydetector-anomalydetectorname"></a>
The name of the detector\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyArn`  <a name="cfn-lookoutmetrics-anomalydetector-kmskeyarn"></a>
The ARN of the KMS key to use to encrypt your data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSetList`  <a name="cfn-lookoutmetrics-anomalydetector-metricsetlist"></a>
The detector's dataset\.  
*Required*: Yes  
*Type*: List of [MetricSet](aws-properties-lookoutmetrics-anomalydetector-metricset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lookoutmetrics-anomalydetector-return-values"></a>

### Ref<a name="aws-resource-lookoutmetrics-anomalydetector-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lookoutmetrics-anomalydetector-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lookoutmetrics-anomalydetector-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the detector\. For example, `arn:aws:lookoutmetrics:us-east-2:123456789012:AnomalyDetector:my-detector`