# Amazon CloudWatch template snippets<a name="quickref-cloudwatch"></a>

**Topics**
+ [Billing alarm](#cloudwatch-sample-billing-alarm)
+ [CPU utilization alarm](#cloudwatch-sample-cpu-utilization-alarm)
+ [Recover an Amazon Elastic Compute Cloud instance](#cloudwatch-sample-recover-instance)
+ [Create a basic dashboard](#cloudwatch-sample-dashboard-basic)
+ [Create a dashboard with side\-by\-side widgets](#cloudwatch-sample-dashboard-sidebyside)

## Billing alarm<a name="cloudwatch-sample-billing-alarm"></a>

In the following sample, Amazon CloudWatch sends an email notification when charges to your AWS account exceed the alarm threshold\. To receive usage notifications, enable [billing alerts](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/monitor-charges.html)\.

### JSON<a name="quickref-cloudwatch-example-1.json"></a>

```
"SpendingAlarm": {
  "Type": "AWS::CloudWatch::Alarm",
  "Properties": {
    "AlarmDescription": { "Fn::Join": ["", [
      "Alarm if AWS spending is over $",
      { "Ref": "AlarmThreshold" }
    ]]},
    "Namespace": "AWS/Billing",
    "MetricName": "EstimatedCharges",
    "Dimensions": [{
      "Name": "Currency",
      "Value" : "USD"
    }],
    "Statistic": "Maximum",
    "Period": "21600",
    "EvaluationPeriods": "1",
    "Threshold": { "Ref": "AlarmThreshold" },
    "ComparisonOperator": "GreaterThanThreshold",
    "AlarmActions": [{
      "Ref": "BillingAlarmNotification"
    }],
    "InsufficientDataActions": [{
      "Ref": "BillingAlarmNotification"
    }]
  }
}
```

### YAML<a name="quickref-cloudwatch-example-1.yaml"></a>

```
SpendingAlarm:
  Type: AWS::CloudWatch::Alarm
  Properties:
    AlarmDescription: 
      'Fn::Join':
        - ''
        - - Alarm if AWS spending is over $
          - Ref: AlarmThreshold
    Namespace: AWS/Billing
    MetricName: EstimatedCharges
    Dimensions:
    - Name: Currency
      Value: USD
    Statistic: Maximum
    Period: '21600'
    EvaluationPeriods: '1'
    Threshold:
      Ref: "AlarmThreshold"
    ComparisonOperator: GreaterThanThreshold
    AlarmActions:
    - Ref: "BillingAlarmNotification"
    InsufficientDataActions:
    - Ref: "BillingAlarmNotification"
```

## CPU utilization alarm<a name="cloudwatch-sample-cpu-utilization-alarm"></a>

The following sample snippet creates an alarm that sends a notification when the average CPU utilization of an Amazon EC2 instance exceeds 90 percent for more than 60 seconds over three evaluation periods\.

### JSON<a name="quickref-cloudwatch-example-2.json"></a>

```
 1. "CPUAlarm" : {
 2.   "Type" : "AWS::CloudWatch::Alarm",
 3.   "Properties" : {
 4.     "AlarmDescription" : "CPU alarm for my instance",
 5.     "AlarmActions" : [ { "Ref" : "logical name of an AWS::SNS::Topic resource" } ],
 6.     "MetricName" : "CPUUtilization",
 7.     "Namespace" : "AWS/EC2",
 8.     "Statistic" : "Average",
 9.     "Period" : "60",
10.     "EvaluationPeriods" : "3",
11.     "Threshold" : "90",
12.     "ComparisonOperator" : "GreaterThanThreshold",
13.     "Dimensions" : [ {
14.       "Name" : "InstanceId",
15.       "Value" : { "Ref" : "logical name of an AWS::EC2::Instance resource" }
16.     } ]
17.   }
18. }
```

### YAML<a name="quickref-cloudwatch-example-2.yaml"></a>

```
 1. CPUAlarm:
 2.   Type: AWS::CloudWatch::Alarm
 3.   Properties:
 4.     AlarmDescription: CPU alarm for my instance
 5.     AlarmActions:
 6.     - Ref: "logical name of an AWS::SNS::Topic resource"
 7.     MetricName: CPUUtilization
 8.     Namespace: AWS/EC2
 9.     Statistic: Average
10.     Period: '60'
11.     EvaluationPeriods: '3'
12.     Threshold: '90'
13.     ComparisonOperator: GreaterThanThreshold
14.     Dimensions:
15.     - Name: InstanceId
16.       Value:
17.         Ref: "logical name of an AWS::EC2::Instance resource"
```

## Recover an Amazon Elastic Compute Cloud instance<a name="cloudwatch-sample-recover-instance"></a>

The following CloudWatch alarm recovers an EC2 instance when it has status check failures for 15 consecutive minutes\. For more information about alarm actions, see [Create alarms that stop, terminate, or recover an instance](https://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/UsingAlarmActions.html) in the *Amazon CloudWatch User Guide*\.

### JSON<a name="quickref-cloudwatch-example-3.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters" : {
    "RecoveryInstance" : {
      "Description" : "The EC2 instance ID to associate this alarm with.",
      "Type" : "AWS::EC2::Instance::Id"
    }
  },
  "Resources": {
    "RecoveryTestAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "AlarmDescription": "Trigger a recovery when instance status check fails for 15 consecutive minutes.",
        "Namespace": "AWS/EC2" ,
        "MetricName": "StatusCheckFailed_System",
        "Statistic": "Minimum",
        "Period": "60",
        "EvaluationPeriods": "15",
        "ComparisonOperator": "GreaterThanThreshold",
        "Threshold": "0",
        "AlarmActions": [ {"Fn::Join" : ["", ["arn:aws:automate:", { "Ref" : "AWS::Region" }, ":ec2:recover" ]]} ],
        "Dimensions": [{"Name": "InstanceId","Value": {"Ref": "RecoveryInstance"}}]
      }
    }
  }
}
```

### YAML<a name="quickref-cloudwatch-example-3.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  RecoveryInstance:
    Description: The EC2 instance ID to associate this alarm with.
    Type: AWS::EC2::Instance::Id
Resources:
  RecoveryTestAlarm:
    Type: AWS::CloudWatch::Alarm
    Properties:
      AlarmDescription: Trigger a recovery when instance status check fails for 15
        consecutive minutes.
      Namespace: AWS/EC2
      MetricName: StatusCheckFailed_System
      Statistic: Minimum
      Period: '60'
      EvaluationPeriods: '15'
      ComparisonOperator: GreaterThanThreshold
      Threshold: '0'
      AlarmActions: [ !Sub "arn:aws:automate:${AWS::Region}:ec2:recover" ]
      Dimensions:
      - Name: InstanceId
        Value:
          Ref: RecoveryInstance
```

## Create a basic dashboard<a name="cloudwatch-sample-dashboard-basic"></a>

The following example creates a simple CloudWatch dashboard with one metric widget displaying CPU utilization, and one text widget displaying a message\.

### JSON<a name="quickref-cloudwatch-sample-dashboard-basic.json"></a>

```
{
    "BasicDashboard": {
        "Type": "AWS::CloudWatch::Dashboard",
        "Properties": {
            "DashboardName": "Dashboard1",
            "DashboardBody": "{\"widgets\":[{\"type\":\"metric\",\"x\":0,\"y\":0,\"width\":12,\"height\":6,\"properties\":{\"metrics\":[[\"AWS/EC2\",\"CPUUtilization\",\"InstanceId\",\"i-012345\"]],\"period\":300,\"stat\":\"Average\",\"region\":\"us-east-1\",\"title\":\"EC2 Instance CPU\"}},{\"type\":\"text\",\"x\":0,\"y\":7,\"width\":3,\"height\":3,\"properties\":{\"markdown\":\"Hello world\"}}]}"
        }
    }
}
```

### YAML<a name="quickref-cloudwatch-sample-dashboard-basic.yaml"></a>

```
BasicDashboard:
  Type: AWS::CloudWatch::Dashboard
  Properties:
    DashboardName: Dashboard1
    DashboardBody: '{"widgets":[{"type":"metric","x":0,"y":0,"width":12,"height":6,"properties":{"metrics":[["AWS/EC2","CPUUtilization","InstanceId","i-012345"]],"period":300,"stat":"Average","region":"us-east-1","title":"EC2 Instance CPU"}},{"type":"text","x":0,"y":7,"width":3,"height":3,"properties":{"markdown":"Hello world"}}]}'
```

## Create a dashboard with side\-by\-side widgets<a name="cloudwatch-sample-dashboard-sidebyside"></a>

The following example creates a dashboard with two metric widgets that appear side by side\.

### JSON<a name="quickref-cloudwatch-sample-dashboard-sidebyside.json"></a>

```
{
    "DashboardSideBySide": {
        "Type": "AWS::CloudWatch::Dashboard",
        "Properties": {
            "DashboardName": "Dashboard1",
            "DashboardBody": "{\"widgets\":[{\"type\":\"metric\",\"x\":0,\"y\":0,\"width\":12,\"height\":6,\"properties\":{\"metrics\":[[\"AWS/EC2\",\"CPUUtilization\",\"InstanceId\",\"i-012345\"]],\"period\":300,\"stat\":\"Average\",\"region\":\"us-east-1\",\"title\":\"EC2 Instance CPU\"}},{\"type\":\"metric\",\"x\":12,\"y\":0,\"width\":12,\"height\":6,\"properties\":{\"metrics\":[[\"AWS/S3\",\"BucketSizeBytes\",\"BucketName\",\"MyBucketName\"]],\"period\":86400,\"stat\":\"Maximum\",\"region\":\"us-east-1\",\"title\":\"MyBucketName bytes\"}}]}"
        }
    }
}
```

### YAML<a name="quickref-cloudwatch-sample-dashboard-sidebysidequickref-cloudwatch-sample-dashboard-sidebyside.yaml"></a>

```
DashboardSideBySide:
  Type: AWS::CloudWatch::Dashboard
  Properties:
    DashboardName: Dashboard1
    DashboardBody: '{"widgets":[{"type":"metric","x":0,"y":0,"width":12,"height":6,"properties":{"metrics":[["AWS/EC2","CPUUtilization","InstanceId","i-012345"]],"period":300,"stat":"Average","region":"us-east-1","title":"EC2 Instance CPU"}},{"type":"metric","x":12,"y":0,"width":12,"height":6,"properties":{"metrics":[["AWS/S3","BucketSizeBytes","BucketName","MyBucketName"]],"period":86400,"stat":"Maximum","region":"us-east-1","title":"MyBucketName bytes"}}]}'
```