# CloudWatch Metric Dimension Property Type<a name="aws-properties-cw-dimension"></a>

The Metric Dimension is an embedded property of the [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md) type\. Dimensions are arbitrary name/value pairs that can be associated with a CloudWatch metric\. You can specify a maximum of 10 dimensions for a given metric\.

## Syntax<a name="w3ab2c21c14d337b5"></a>

### JSON<a name="aws-properties-cw-dimension-syntax.json"></a>

```
{
  "Name" : String,
  "Value" : String
}
```

### YAML<a name="aws-properties-cw-dimension-syntax.yaml"></a>

```
Name: String
Value: String
```

## Properties<a name="w3ab2c21c14d337b7"></a>

`Name`  
The name of the dimension, from 1–255 characters in length\.  
*Required*: Yes  
*Type*: String

`Value`  
The value representing the dimension measurement, from 1–255 characters in length\.  
*Required*: Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d337b9"></a>

### Two CloudWatch alarms with dimension values supplied by the Ref function<a name="w3ab2c21c14d337b9b2"></a>

The [Ref](intrinsic-function-reference-ref.md) and [Fn::GetAtt](intrinsic-function-reference-getatt.md) intrinsic functions are often used to supply values for CloudWatch metric dimensions\. Here is an example using the `Ref` function\.

```
"CPUAlarmHigh": {
   "Type": "AWS::CloudWatch::Alarm",
   "Properties": {
      "AlarmDescription": "Scale-up if CPU is greater than 90% for 10 minutes",
      "MetricName": "CPUUtilization",
      "Namespace": "AWS/EC2",
      "Statistic": "Average",
      "Period": "300",
      "EvaluationPeriods": "2",
      "Threshold": "90",
      "AlarmActions": [ { "Ref": "WebServerScaleUpPolicy" } ],
      "Dimensions": [
         {
            "Name": "AutoScalingGroupName",
            "Value": { "Ref": "WebServerGroup" }
         }
      ],
      "ComparisonOperator": "GreaterThanThreshold"
   }
},
"CPUAlarmLow": {
   "Type": "AWS::CloudWatch::Alarm",
   "Properties": {
      "AlarmDescription": "Scale-down if CPU is less than 70% for 10 minutes",
      "MetricName": "CPUUtilization",
      "Namespace": "AWS/EC2",
      "Statistic": "Average",
      "Period": "300",
      "EvaluationPeriods": "2",
      "Threshold": "70",
      "AlarmActions": [ { "Ref": "WebServerScaleDownPolicy" } ],
      "Dimensions": [
         {
            "Name": "AutoScalingGroupName",
            "Value": { "Ref": "WebServerGroup" }
         }
      ],
      "ComparisonOperator": "LessThanThreshold"
   }
}
```

## See Also<a name="w3ab2c21c14d337c11"></a>
+ [Dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_Dimension.html) in the *Amazon CloudWatch API Reference*
+ [Amazon CloudWatch Metrics, Namespaces, and Dimensions Reference](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/CW_Support_For_AWS.html) in the *Amazon CloudWatch Developer Guide*