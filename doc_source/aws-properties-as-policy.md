# AWS::AutoScaling::ScalingPolicy<a name="aws-properties-as-policy"></a>

Adds a scaling policy to an Auto Scaling group\. A scaling policy specifies whether to scale the Auto Scaling group up or down, and by how much\. For more information, see [Dynamic Scaling](http://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the *Amazon EC2 Auto Scaling User Guide*\.

You can use a scaling policy together with a CloudWatch alarm\. A CloudWatch alarm can automatically initiate actions on your behalf, based on parameters you specify\. A scaling policy is one type of action that an alarm can initiate\. For a snippet showing how to create an Auto Scaling policy that is triggered by a CloudWatch alarm, see [Auto Scaling Policy Triggered by CloudWatch Alarm](quickref-autoscaling.md#scenario-as-policy)\. Note that you can only associate one scaling policy with an alarm\.

This type supports updates\. For more information about updating this resource, see [PutScalingPolicy](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutScalingPolicy.html) in the *Amazon EC2 Auto Scaling API Reference*\.

**Topics**
+ [Syntax](#aws-resource-autoscaling-scalingpolicy-syntax)
+ [Properties](#w3ab2c21c10d144c13)
+ [Return Value](#w3ab2c21c10d144c15)
+ [Examples](#w3ab2c21c10d144c17)

## Syntax<a name="aws-resource-autoscaling-scalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-scalingpolicy-syntax.json"></a>

```
{
   "Type" : "AWS::AutoScaling::ScalingPolicy",
   "Properties" : {
      "[AdjustmentType](#cfn-as-scalingpolicy-adjustmenttype)" : String,
      "[AutoScalingGroupName](#cfn-as-scalingpolicy-autoscalinggroupname)" : String,
      "[Cooldown](#cfn-as-scalingpolicy-cooldown)" : String,
      "[EstimatedInstanceWarmup](#cfn-as-scalingpolicy-estimatedinstancewarmup)" : Integer,
      "[MetricAggregationType](#cfn-as-scalingpolicy-metricaggregationtype)" : String,
      "[MinAdjustmentMagnitude](#cfn-as-scalingpolicy-minadjustmentmagnitude)" : Integer,
      "[PolicyType](#cfn-as-scalingpolicy-policytype)" : String,
      "[ScalingAdjustment](#cfn-as-scalingpolicy-scalingadjustment)" : Integer,
      "[StepAdjustments](#cfn-as-scalingpolicy-stepadjustments)" : [ [*StepAdjustments*](aws-properties-autoscaling-scalingpolicy-stepadjustments.md), ... ]
      "[TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration)" : [*TargetTrackingConfiguration*](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)
   }
}
```

### YAML<a name="aws-resource-autoscaling-scalingpolicy-syntax.yaml"></a>

```
Type: "AWS::AutoScaling::ScalingPolicy"
Properties:
  [AdjustmentType](#cfn-as-scalingpolicy-adjustmenttype): String
  [AutoScalingGroupName](#cfn-as-scalingpolicy-autoscalinggroupname): String
  [Cooldown](#cfn-as-scalingpolicy-cooldown): String
  [EstimatedInstanceWarmup](#cfn-as-scalingpolicy-estimatedinstancewarmup): Integer
  [MetricAggregationType](#cfn-as-scalingpolicy-metricaggregationtype): String
  [MinAdjustmentMagnitude](#cfn-as-scalingpolicy-minadjustmentmagnitude): Integer
  [PolicyType](#cfn-as-scalingpolicy-policytype): String
  [ScalingAdjustment](#cfn-as-scalingpolicy-scalingadjustment): Integer
  [StepAdjustments](#cfn-as-scalingpolicy-stepadjustments):
    - [*StepAdjustments*](aws-properties-autoscaling-scalingpolicy-stepadjustments.md)
  [TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration):
    [*TargetTrackingConfiguration*](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)
```

## Properties<a name="w3ab2c21c10d144c13"></a>

`AdjustmentType`  <a name="cfn-as-scalingpolicy-adjustmenttype"></a>
Specifies whether the `ScalingAdjustment` is an absolute number or a percentage of the current capacity\. Valid values are `ChangeInCapacity`, `ExactCapacity`, and `PercentChangeInCapacity`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoScalingGroupName`  <a name="cfn-as-scalingpolicy-autoscalinggroupname"></a>
The name or Amazon Resource Name \(ARN\) of the Auto Scaling Group that you want to attach the policy to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Cooldown`  <a name="cfn-as-scalingpolicy-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before any further trigger\-related scaling activities can start\.  
Do not specify this property if you are using the `StepScaling` policy type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EstimatedInstanceWarmup`  <a name="cfn-as-scalingpolicy-estimatedinstancewarmup"></a>
The estimated time, in seconds, until a newly launched instance can send metrics to CloudWatch\. By default, Auto Scaling uses the cooldown period, as specified in the `Cooldown` property\.  
Do not specify this property if you are using the `SimpleScaling` policy type\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricAggregationType`  <a name="cfn-as-scalingpolicy-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. You can specify `Minimum`, `Maximum`, or `Average`\. By default, AWS CloudFormation specifies `Average`\.  
Do not specify this property if you are using the `SimpleScaling` policy type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinAdjustmentMagnitude`  <a name="cfn-as-scalingpolicy-minadjustmentmagnitude"></a>
For the `PercentChangeInCapacity` adjustment type, the minimum number of instances to scale\. The scaling policy changes the desired capacity of the Auto Scaling group by a minimum of this many instances\. This property replaces the `MinAdjustmentStep` property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PolicyType`  <a name="cfn-as-scalingpolicy-policytype"></a>
An Auto Scaling policy type\. You can specify `SimpleScaling`, `StepScaling`, or `TargetTrackingScaling`\. By default, AWS CloudFormation specifies `SimpleScaling`\. For more information, see [Dynamic Scaling](http://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-as-scalingpolicy-scalingadjustment"></a>
The number of instances by which to scale\. The `AdjustmentType` property determines if AWS CloudFormation interprets this number as an absolute number \(when the `ExactCapacity` value is specified\), increase or decrease capacity by a specified number \(when the `ChangeInCapacity` value is specified\), or increase or decrease capacity as a percentage of the existing Auto Scaling group size \(when the `PercentChangeInCapacity` value is specified\)\. A positive value adds to the current capacity and a negative value subtracts from the current capacity\. For exact capacity, you must specify a positive value\.  
*Required*: Conditional\. This property is required if the policy type is `SimpleScaling`\. This property is not supported with any other policy type\.   
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StepAdjustments`  <a name="cfn-as-scalingpolicy-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.  
*Required*: Conditional\. This property is required if the policy type is `StepScaling`\. This property is not supported with any other policy type\.   
*Type*: List of [Amazon EC2 Auto Scaling ScalingPolicy StepAdjustments](aws-properties-autoscaling-scalingpolicy-stepadjustments.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetTrackingConfiguration`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration"></a>
Configures a target tracking scaling policy\.  
*Required*: Conditional\. This property is required if the policy type is `TargetTrackingScaling`\. This property is not supported with any other policy type\.  
*Type*: [Amazon EC2 Auto Scaling ScalingPolicy TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d144c15"></a>

When you specify an `AWS::AutoScaling::ScalingPolicy` type as an argument to the `Ref` function, AWS CloudFormation returns the policy Amazon Resource Name \(ARN\), such as `arn:aws:autoscaling:``us-east-2``:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d144c17"></a>

### Simple policy type<a name="w3ab2c21c10d144c17b3"></a>

The following example is a simple scaling policy that increases the number instances by one when it is triggered\.

#### JSON<a name="aws-resource-autoscaling-scalingpolicy-example1.json"></a>

```
"SimpleScaling" : {
  "Type" : "AWS::AutoScaling::ScalingPolicy",
  "Properties" : {
    "AdjustmentType" : "ChangeInCapacity",
    "PolicyType" : "SimpleScaling",	
    "Cooldown" : "60",
    "AutoScalingGroupName" : { "Ref" : "ASG" },
    "ScalingAdjustment" : 1
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scalingpolicy-example1.yaml"></a>

```
SimpleScaling: 
  Type: "AWS::AutoScaling::ScalingPolicy"
  Properties: 
    AdjustmentType: "ChangeInCapacity"
    PolicyType: "SimpleScaling"
    Cooldown: "60"
    AutoScalingGroupName: 
      Ref: "ASG"
    ScalingAdjustment: 1
```

### Step policy type<a name="w3ab2c21c10d144c17b5"></a>

The following example is a step scaling policy that increases the number instances by one or two, depending on the size of the alarm breach\. For a breach that is less than 50 units than the threshold value, the policy increases the number of instances by one\. For a breach that is 50 units or more higher than the threshold, the policy increases the number of instances by two\.

#### JSON<a name="aws-resource-autoscaling-scalingpolicy-example2.json"></a>

```
"StepScaling" : {
  "Type" : "AWS::AutoScaling::ScalingPolicy",
  "Properties" : {
    "AdjustmentType" : "ChangeInCapacity",
    "AutoScalingGroupName" : { "Ref" : "ASG" },
    "PolicyType" : "StepScaling",
    "MetricAggregationType" : "Average",
    "EstimatedInstanceWarmup" : "60",
    "StepAdjustments": [
      {
        "MetricIntervalLowerBound": "0",
        "MetricIntervalUpperBound" : "50",
        "ScalingAdjustment": "1"
      },
      {
        "MetricIntervalLowerBound": "50",
        "ScalingAdjustment": "2"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scalingpolicy-example2.yaml"></a>

```
StepScaling: 
  Type: "AWS::AutoScaling::ScalingPolicy"
  Properties: 
    AdjustmentType: "ChangeInCapacity"
    AutoScalingGroupName: 
      Ref: "ASG"
    PolicyType: "StepScaling"
    MetricAggregationType: "Average"
    EstimatedInstanceWarmup: "60"
    StepAdjustments: 
      - 
        MetricIntervalLowerBound: "0"
        MetricIntervalUpperBound: "50"
        ScalingAdjustment: "1"
      - 
        MetricIntervalLowerBound: "50"
        ScalingAdjustment: "2"
```

### Target tracking scaling policy type<a name="aws-resource-autoscaling-scalingpolicy-example3"></a>

The following example is a target tracking scaling policy based on the `ASGAverageCPUUtilization` metric\.

#### JSON<a name="aws-resource-autoscaling-scalingpolicy-example3.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Parameters" : {
    "AMI" : {
      "Type" : "String"
    },
    "Subnets": {
      "Type" : "CommaDelimitedList"
    },
    "AZs": {
      "Type" : "CommaDelimitedList"
    },
    "PolicyTargetValue": {
      "Type" : "String"
    }
  },
  "Resources" : {
    "LC" : {
      "Type" : "AWS::AutoScaling::LaunchConfiguration",
      "Properties" : {
        "ImageId" : { "Ref" : "AMI" },
        "InstanceType" : "t2.large"
      }
    },
    "POL" : {
      "Type" : "AWS::AutoScaling::ScalingPolicy",
      "Properties" : {
        "AutoScalingGroupName" : {
          "Ref" : "ASG"
        },
        "PolicyType" : "TargetTrackingScaling",
        "TargetTrackingConfiguration": {
          "PredefinedMetricSpecification": {
            "PredefinedMetricType": "ASGAverageCPUUtilization"
          },
          "TargetValue": {"Ref": "PolicyTargetValue"}
        }
      }
    },
    "ASG" : {
      "Type" : "AWS::AutoScaling::AutoScalingGroup",
      "Properties" : {
        "MaxSize" : "1",
        "AvailabilityZones": {
          "Ref": "AZs"
        },
        "VPCZoneIdentifier": {
          "Ref" : "Subnets"
        },
        "MinSize" : "0",
        "DesiredCapacity" : "0",
        "LaunchConfigurationName" : {
          "Ref" : "LC"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scalingpolicy-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AMI:
    Type: String
  Subnets:
    Type: CommaDelimitedList
  AZs:
    Type: CommaDelimitedList
  PolicyTargetValue:
    Type: String
Resources:
  LC:
    Type: 'AWS::AutoScaling::LaunchConfiguration'
    Properties:
      ImageId: !Ref AMI
      InstanceType: t2.large
  POL:
    Type: 'AWS::AutoScaling::ScalingPolicy'
    Properties:
      AutoScalingGroupName: !Ref ASG
      PolicyType: TargetTrackingScaling
      TargetTrackingConfiguration:
        PredefinedMetricSpecification:
          PredefinedMetricType: ASGAverageCPUUtilization
        TargetValue: !Ref PolicyTargetValue
  ASG:
    Type: 'AWS::AutoScaling::AutoScalingGroup'
    Properties:
      MaxSize: '1'
      AvailabilityZones: !Ref AZs
      VPCZoneIdentifier: !Ref Subnets
      MinSize: '0'
      DesiredCapacity: '0'
      LaunchConfigurationName: !Ref LC
```