# AWS::CloudWatch::CompositeAlarm<a name="aws-resource-cloudwatch-compositealarm"></a>

The `AWS::CloudWatch::CompositeAlarm` type creates or updates a composite alarm\. When you create a composite alarm, you specify a rule expression for the alarm that takes into account the alarm states of other alarms that you have created\. The composite alarm goes into ALARM state only if all conditions of the rule are met\.

The alarms specified in a composite alarm's rule expression can include metric alarms and other composite alarms\.

Using composite alarms can reduce alarm noise\. You can create multiple metric alarms, and also create a composite alarm and set up alerts only for the composite alarm\. For example, you could create a composite alarm that goes into ALARM state only when more than one of the underlying metric alarms are in ALARM state\.

Currently, the only alarm actions that can be taken by composite alarms are notifying SNS topics\.

When this operation creates an alarm, the alarm state is immediately set to INSUFFICIENT\_DATA\. The alarm is then evaluated and its state is set appropriately\. Any actions associated with the new state are then executed\. For a composite alarm, this initial time after creation is the only time that the alarm can be in INSUFFICIENT\_DATA state\.

When you update an existing alarm, its state is left unchanged, but the update completely overwrites the previous configuration of the alarm\.

## Syntax<a name="aws-resource-cloudwatch-compositealarm-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudwatch-compositealarm-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::CompositeAlarm",
  "Properties" : {
      "[ActionsEnabled](#cfn-cloudwatch-compositealarm-actionsenabled)" : Boolean,
      "[AlarmActions](#cfn-cloudwatch-compositealarm-alarmactions)" : [ String, ... ],
      "[AlarmDescription](#cfn-cloudwatch-compositealarm-alarmdescription)" : String,
      "[AlarmName](#cfn-cloudwatch-compositealarm-alarmname)" : String,
      "[AlarmRule](#cfn-cloudwatch-compositealarm-alarmrule)" : String,
      "[InsufficientDataActions](#cfn-cloudwatch-compositealarm-insufficientdataactions)" : [ String, ... ],
      "[OKActions](#cfn-cloudwatch-compositealarm-okactions)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-cloudwatch-compositealarm-syntax.yaml"></a>

```
Type: AWS::CloudWatch::CompositeAlarm
Properties: 
  [ActionsEnabled](#cfn-cloudwatch-compositealarm-actionsenabled): Boolean
  [AlarmActions](#cfn-cloudwatch-compositealarm-alarmactions): 
    - String
  [AlarmDescription](#cfn-cloudwatch-compositealarm-alarmdescription): String
  [AlarmName](#cfn-cloudwatch-compositealarm-alarmname): String
  [AlarmRule](#cfn-cloudwatch-compositealarm-alarmrule): String
  [InsufficientDataActions](#cfn-cloudwatch-compositealarm-insufficientdataactions): 
    - String
  [OKActions](#cfn-cloudwatch-compositealarm-okactions): 
    - String
```

## Properties<a name="aws-resource-cloudwatch-compositealarm-properties"></a>

`ActionsEnabled`  <a name="cfn-cloudwatch-compositealarm-actionsenabled"></a>
Indicates whether actions should be executed during any changes to the alarm state of the composite alarm\. The default is TRUE\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmActions`  <a name="cfn-cloudwatch-compositealarm-alarmactions"></a>
The actions to execute when this alarm transitions to the ALARM state from any other state\. Each action is specified as an Amazon Resource Name \(ARN\)\. For more information about creating alarms and the actions that you can specify, see [PutCompositeAlarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutCompositeAlarm.html) in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmDescription`  <a name="cfn-cloudwatch-compositealarm-alarmdescription"></a>
The description for the composite alarm\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmName`  <a name="cfn-cloudwatch-compositealarm-alarmname"></a>
The name for the composite alarm\. This name must be unique within your AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AlarmRule`  <a name="cfn-cloudwatch-compositealarm-alarmrule"></a>
An expression that specifies which other alarms are to be evaluated to determine this composite alarm's state\. For each alarm that you reference, you designate a function that specifies whether that alarm needs to be in ALARM state, OK state, or INSUFFICIENT\_DATA state\. You can use operators \(AND, OR and NOT\) to combine multiple functions in a single expression\. You can use parenthesis to logically group the functions in your expression\.  
You can use either alarm names or ARNs to reference the other alarms that are to be evaluated\.  
Functions can include the following:  
+  ALARM\("alarm\-name or alarm\-ARN"\) is TRUE if the named alarm is in ALARM state\. 
+  OK\("alarm\-name or alarm\-ARN"\) is TRUE if the named alarm is in OK state\. 
+  INSUFFICIENT\_DATA\("alarm\-name or alarm\-ARN"\) is TRUE if the named alarm is in INSUFFICIENT\_DATA state\. 
+ TRUE always evaluates to TRUE\.
+ FALSE always evaluates to FALSE\.
 TRUE and FALSE are useful for testing a complex AlarmRule structure, and for testing your alarm actions\.  
For more information about `AlarmRule` syntax, see [PutCompositeAlarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutCompositeAlarm.html) in the *Amazon CloudWatch API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsufficientDataActions`  <a name="cfn-cloudwatch-compositealarm-insufficientdataactions"></a>
The actions to execute when this alarm transitions to the INSUFFICIENT\_DATA state from any other state\. Each action is specified as an Amazon Resource Name \(ARN\)\. For more information about creating alarms and the actions that you can specify, see [PutCompositeAlarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutCompositeAlarm.html) in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OKActions`  <a name="cfn-cloudwatch-compositealarm-okactions"></a>
The actions to execute when this alarm transitions to the OK state from any other state\. Each action is specified as an Amazon Resource Name \(ARN\)\. For more information about creating alarms and the actions that you can specify, see [PutCompositeAlarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutCompositeAlarm.html) in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudwatch-compositealarm-return-values"></a>

### Ref<a name="aws-resource-cloudwatch-compositealarm-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alarm name, such as `MyCompositeAlarm`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudwatch-compositealarm-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudwatch-compositealarm-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the composite alarm, such as `arn:aws:cloudwatch:us-west-2:123456789012:alarm/CompositeAlarmName`\.

## Examples<a name="aws-resource-cloudwatch-compositealarm--examples"></a>



### Composite alarm based on two metric alarms and another composite alarm<a name="aws-resource-cloudwatch-compositealarm--examples--Composite_alarm_based_on_two_metric_alarms_and_another_composite_alarm"></a>

This example creates composite alarms named "HighResourceUsage" and "DeploymentInProgress", and also creates metrics alarms named "HighCPUUsage" and "HighMemoryUsage"\. "DeploymentInProgress" is an alarm that must be manually set to TRUE or FALSE\. The "HighResourceUsage" alarm goes into ALARM state only if both "HighCPUUsage" and "HighMemoryUsage" are in ALARM state, and if "DeploymentInProgress" is FALSE\. Only "HighResourceUsage" has the alarm action of notifying SNS\. This reduces alarm noise, so that you are alerted only if both CPU usage and memory usage are high, and a deployment is not currently in progress\.

#### JSON<a name="aws-resource-cloudwatch-compositealarm--examples--Composite_alarm_based_on_two_metric_alarms_and_another_composite_alarm--json"></a>

```
"Resources": {
    "HighResourceUsage": {
        "Type": "AWS::CloudWatch::CompositeAlarm",
        "Properties": {
            "AlarmName": "HighResourceUsage",
            "AlarmRule": "(ALARM(HighCPUUsage) OR ALARM(HighMemoryUsage)) AND NOT ALARM(DeploymentInProgress)",
            "AlarmActions": "arn:aws:sns:us-west-2:123456789012:my-sns-topic",
            "AlarmDescription": "Indicates that the system resource usage is high while no known 
            deployment is in progress"
        },
        "DependsOn": [
            "DeploymentInProgress",
            "HighCPUUsage",
            "HighMemoryUsage"
        ]
    },
    "DeploymentInProgress": {
        "Type": "AWS::CloudWatch::CompositeAlarm",
        "Properties": {
            "AlarmName": "DeploymentInProgress",
            "AlarmRule": "FALSE",
            "AlarmDescription": "Manually updated to TRUE/FALSE to disable other alarms"
        }
    },
    "HighCPUUsage": {
        "Type": "AWS::CloudWatch::Alarm",
        "Properties": {
            "AlarmDescription": "CPUusageishigh",
            "AlarmName": "HighCPUUsage",
            "ComparisonOperator": "GreaterThanThreshold",
            "EvaluationPeriods": 1,
            "MetricName": "CPUUsage",
            "Namespace": "CustomNamespace",
            "Period": 60,
            "Statistic": "Average",
            "Threshold": 70,
            "TreatMissingData": "notBreaching"
        }
    },
    "HighMemoryUsage": {
        "Type": "AWS::CloudWatch::Alarm",
        "Properties": {
            "AlarmDescription": "Memoryusageishigh",
            "AlarmName": "HighMemoryUsage",
            "ComparisonOperator": "GreaterThanThreshold",
            "EvaluationPeriods": 1,
            "MetricName": "MemoryUsage",
            "Namespace": "CustomNamespace",
            "Period": 60,
            "Statistic": "Average",
            "Threshold": 65,
            "TreatMissingData": "breaching"
        }
    }
}
```

#### YAML<a name="aws-resource-cloudwatch-compositealarm--examples--Composite_alarm_based_on_two_metric_alarms_and_another_composite_alarm--yaml"></a>

```
Resources:
  HighResourceUsage:
    Type: AWS::CloudWatch::CompositeAlarm
    Properties:
      AlarmName: HighResourceUsage
      AlarmRule: (ALARM(HighCPUUsage) OR ALARM(HighMemoryUsage)) AND NOT ALARM(DeploymentInProgress)
      AlarmActions: arn:aws:sns:us-west-2:123456789012:my-sns-topic
      AlarmDescription: Indicates that the system resource usage is high while no known deployment is in progress
    DependsOn:
    - DeploymentInProgress
    - HighCPUUsage
    - HighMemoryUsage
  DeploymentInProgress:
    Type: AWS::CloudWatch::CompositeAlarm
    Properties:
      AlarmName: DeploymentInProgress
      AlarmRule: 
      AlarmDescription: Manually updated to TRUE/FALSE to disable other alarms
  HighCPUUsage: 
    Type: AWS::CloudWatch::Alarm
    Properties: 
      AlarmDescription: CPU usage is high
      AlarmName: HighCPUUsage
      ComparisonOperator: GreaterThanThreshold
      EvaluationPeriods: 1
      MetricName: CPUUsage
      Namespace: CustomNamespace
      Period: 60
      Statistic: Average
      Threshold: 70
      TreatMissingData: notBreaching
  HighMemoryUsage: 
    Type: AWS::CloudWatch::Alarm
    Properties: 
      AlarmDescription: Memory usage is high
      AlarmName: HighMemoryUsage
      ComparisonOperator: GreaterThanThreshold
      EvaluationPeriods: 1
      MetricName: MemoryUsage
      Namespace: CustomNamespace
      Period: 60
      Statistic: Average
      Threshold: 65
      TreatMissingData: breaching
```