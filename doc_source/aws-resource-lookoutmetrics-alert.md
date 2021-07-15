# AWS::LookoutMetrics::Alert<a name="aws-resource-lookoutmetrics-alert"></a>

The `AWS::LookoutMetrics::Alert` type creates an alert for an anomaly detector\.

## Syntax<a name="aws-resource-lookoutmetrics-alert-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lookoutmetrics-alert-syntax.json"></a>

```
{
  "Type" : "AWS::LookoutMetrics::Alert",
  "Properties" : {
      "[Action](#cfn-lookoutmetrics-alert-action)" : Json,
      "[AlertDescription](#cfn-lookoutmetrics-alert-alertdescription)" : String,
      "[AlertName](#cfn-lookoutmetrics-alert-alertname)" : String,
      "[AlertSensitivityThreshold](#cfn-lookoutmetrics-alert-alertsensitivitythreshold)" : Integer,
      "[AnomalyDetectorArn](#cfn-lookoutmetrics-alert-anomalydetectorarn)" : String
    }
}
```

### YAML<a name="aws-resource-lookoutmetrics-alert-syntax.yaml"></a>

```
Type: AWS::LookoutMetrics::Alert
Properties: 
  [Action](#cfn-lookoutmetrics-alert-action): Json
  [AlertDescription](#cfn-lookoutmetrics-alert-alertdescription): String
  [AlertName](#cfn-lookoutmetrics-alert-alertname): String
  [AlertSensitivityThreshold](#cfn-lookoutmetrics-alert-alertsensitivitythreshold): Integer
  [AnomalyDetectorArn](#cfn-lookoutmetrics-alert-anomalydetectorarn): String
```

## Properties<a name="aws-resource-lookoutmetrics-alert-properties"></a>

`Action`  <a name="cfn-lookoutmetrics-alert-action"></a>
Action that will be triggered when there is an alert\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AlertDescription`  <a name="cfn-lookoutmetrics-alert-alertdescription"></a>
A description of the alert\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AlertName`  <a name="cfn-lookoutmetrics-alert-alertname"></a>
The name of the alert\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AlertSensitivityThreshold`  <a name="cfn-lookoutmetrics-alert-alertsensitivitythreshold"></a>
An integer from 0 to 100 specifying the alert sensitivity threshold\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AnomalyDetectorArn`  <a name="cfn-lookoutmetrics-alert-anomalydetectorarn"></a>
The ARN of the detector to which the alert is attached\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lookoutmetrics-alert-return-values"></a>

### Ref<a name="aws-resource-lookoutmetrics-alert-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lookoutmetrics-alert-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lookoutmetrics-alert-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the alert\. For example, `arn:aws:lookoutmetrics:us-east-2:123456789012:Alert:my-alert`