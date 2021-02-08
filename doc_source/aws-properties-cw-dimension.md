# AWS::CloudWatch::Alarm Dimension<a name="aws-properties-cw-dimension"></a>

Dimension is an embedded property of the `AWS::CloudWatch::Alarm` type\. Dimensions are name/value pairs that can be associated with a CloudWatch metric\. You can specify a maximum of 10 dimensions for a given metric\.

## Syntax<a name="aws-properties-cw-dimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cw-dimension-syntax.json"></a>

```
{
  "[Name](#cfn-cloudwatch-alarm-dimension-name)" : String,
  "[Value](#cfn-cloudwatch-alarm-dimension-value)" : String
}
```

### YAML<a name="aws-properties-cw-dimension-syntax.yaml"></a>

```
  [Name](#cfn-cloudwatch-alarm-dimension-name): String
  [Value](#cfn-cloudwatch-alarm-dimension-value): String
```

## Properties<a name="aws-properties-cw-dimension-properties"></a>

`Name`  <a name="cfn-cloudwatch-alarm-dimension-name"></a>
The name of the dimension, from 1–255 characters in length\. This dimension name must have been included when the metric was published\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-cloudwatch-alarm-dimension-value"></a>
The value for the dimension, from 1–255 characters in length\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-cw-dimension--examples"></a>



### Two CloudWatch alarms with dimension values supplied by the Ref function<a name="aws-properties-cw-dimension--examples--Two_CloudWatch_alarms_with_dimension_values_supplied_by_the_Ref_function"></a>

The [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) and [GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html) intrinsic functions are often used to supply values for CloudWatch metric dimensions\. Here is an example using the Ref function\.

#### JSON<a name="aws-properties-cw-dimension--examples--Two_CloudWatch_alarms_with_dimension_values_supplied_by_the_Ref_function--json"></a>

```
{
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
            "AlarmActions": [
                {
                    "Ref": "WebServerScaleUpPolicy"
                }
            ],
            "Dimensions": [
                {
                    "Name": "AutoScalingGroupName",
                    "Value": {
                        "Ref": "WebServerGroup"
                    }
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
            "AlarmActions": [
                {
                    "Ref": "WebServerScaleDownPolicy"
                }
            ],
            "Dimensions": [
                {
                    "Name": "AutoScalingGroupName",
                    "Value": {
                        "Ref": "WebServerGroup"
                    }
                }
            ],
            "ComparisonOperator": "LessThanThreshold"
        }
    }
}
```

#### YAML<a name="aws-properties-cw-dimension--examples--Two_CloudWatch_alarms_with_dimension_values_supplied_by_the_Ref_function--yaml"></a>

```
CPUAlarmHigh:
  Type: 'AWS::CloudWatch::Alarm'
  Properties:
    AlarmDescription: Scale-up if CPU is greater than 90% for 10 minutes
    MetricName: CPUUtilization
    Namespace: AWS/EC2
    Statistic: Average
    Period: '300'
    EvaluationPeriods: '2'
    Threshold: '90'
    AlarmActions:
      - !Ref WebServerScaleUpPolicy
    Dimensions:
      - Name: AutoScalingGroupName
        Value: !Ref WebServerGroup
    ComparisonOperator: GreaterThanThreshold
CPUAlarmLow:
  Type: 'AWS::CloudWatch::Alarm'
  Properties:
    AlarmDescription: Scale-down if CPU is less than 70% for 10 minutes
    MetricName: CPUUtilization
    Namespace: AWS/EC2
    Statistic: Average
    Period: '300'
    EvaluationPeriods: '2'
    Threshold: '70'
    AlarmActions:
      - !Ref WebServerScaleDownPolicy
    Dimensions:
      - Name: AutoScalingGroupName
        Value: !Ref WebServerGroup
    ComparisonOperator: LessThanThreshold
```