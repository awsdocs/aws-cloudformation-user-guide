# AWS::AutoScaling::ScalingPolicy<a name="aws-properties-as-policy"></a>

Specifies a scaling policy for an Amazon EC2 Auto Scaling group\.

To update an existing scaling policy, use the existing policy name and set the property to change\. If you leave a property unspecified when updating a scaling policy, the corresponding value remains unchanged\.

If you create either a step scaling policy or a simple scaling policy, you must also create a CloudWatch alarm that monitors a CloudWatch metric for your Auto Scaling group\. Note that you can associate a CloudWatch alarm with only one scaling policy\.

For more information about using scaling policies to scale your Auto Scaling group automatically, see [Dynamic Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-as-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-policy-syntax.json"></a>

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
      "[StepAdjustments](#cfn-as-scalingpolicy-stepadjustments)" : [ [StepAdjustment](aws-properties-autoscaling-scalingpolicy-stepadjustments.md), ... ],
      "[TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration)" : [TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)
    }
}
```

### YAML<a name="aws-properties-as-policy-syntax.yaml"></a>

```
Type: AWS::AutoScaling::ScalingPolicy
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
    - [StepAdjustment](aws-properties-autoscaling-scalingpolicy-stepadjustments.md)
  [TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration):
    [TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)
```

## Properties<a name="aws-properties-as-policy-properties"></a>

`AdjustmentType`  <a name="cfn-as-scalingpolicy-adjustmenttype"></a>
Specifies whether the `ScalingAdjustment` property is an absolute number or a percentage of the current capacity\. The valid values are `ChangeInCapacity`, `ExactCapacity`, and `PercentChangeInCapacity`\.
Valid only if the policy type is `StepScaling` or `SimpleScaling`\. For more information, see [Scaling Adjustment Types](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-adjustment) in the *Amazon EC2 Auto Scaling User Guide*\.
*Required*: No
*Type*: String
*Minimum*: `1`
*Maximum*: `255`
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoScalingGroupName`  <a name="cfn-as-scalingpolicy-autoscalinggroupname"></a>
The name or Amazon Resource Name \(ARN\) of the Auto Scaling group that you want to attach the policy to\.
*Required*: Yes
*Type*: String
*Minimum*: `1`
*Maximum*: `255`
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-as-scalingpolicy-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before any further dynamic scaling activities can start\. If this property is not specified, the default cooldown period for the group applies\.
Valid only if the policy type is `SimpleScaling`\. For more information, see [Scaling Cooldowns](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EstimatedInstanceWarmup`  <a name="cfn-as-scalingpolicy-estimatedinstancewarmup"></a>
The estimated time, in seconds, until a newly launched instance can contribute to the CloudWatch metrics\. The default is to use the value specified for the default cooldown period for the group\.
Valid only if the policy type is `StepScaling` or `TargetTrackingScaling`\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricAggregationType`  <a name="cfn-as-scalingpolicy-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. The valid values are `Minimum`, `Maximum`, and `Average`\. By default, AWS CloudFormation specifies `Average`\.
Valid only if the policy type is `StepScaling`\.
*Required*: No
*Type*: String
*Minimum*: `1`
*Maximum*: `32`
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinAdjustmentMagnitude`  <a name="cfn-as-scalingpolicy-minadjustmentmagnitude"></a>
The minimum number of instances to scale\. If the value of `AdjustmentType` is `PercentChangeInCapacity`, the scaling policy changes the `DesiredCapacity` of the Auto Scaling group by at least this many instances\. This property replaces the `MinAdjustmentStep` property\.
For example, suppose that you create a step scaling policy to scale out an Auto Scaling group by 25 percent and you specify a `MinAdjustmentMagnitude` of 2\. If the group has 4 instances and the scaling policy is performed, 25 percent of 4 is 1\. However, because you specified a `MinAdjustmentMagnitude` of 2, Amazon EC2 Auto Scaling scales out the group by 2 instances\.
Valid only if the policy type is `StepScaling` or `SimpleScaling`\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-as-scalingpolicy-policytype"></a>
The policy type\. The valid values are `SimpleScaling`, `StepScaling`, and `TargetTrackingScaling`\. By default, AWS CloudFormation specifies `SimpleScaling`\.
*Required*: No
*Type*: String
*Minimum*: `1`
*Maximum*: `64`
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-as-scalingpolicy-scalingadjustment"></a>
The amount by which a simple scaling policy scales the Auto Scaling group in response to an alarm breach\. The adjustment is based on the value that you specified in the `AdjustmentType` property \(either an absolute number or a percentage\)\. A positive value adds to the current capacity and a negative value subtracts from the current capacity\. For exact capacity, you must specify a positive value\.
If you specify `SimpleScaling` for the policy type, you must specify this property\. \(Not used with any other policy type\.\)
*Required*: Conditional
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepAdjustments`  <a name="cfn-as-scalingpolicy-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.
If you specify `StepScaling` for the policy type, you must specify this property\. \(Not used with any other policy type\.\)
*Required*: Conditional
*Type*: List of [StepAdjustment](aws-properties-autoscaling-scalingpolicy-stepadjustments.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingConfiguration`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration"></a>
Configures a target tracking scaling policy\.
If you specify `TargetTrackingScaling` for the policy type, you must specify this property\. \(Not used with any other policy type\.\)
*Required*: Conditional
*Type*: [TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-as-policy-return-values"></a>

### Ref<a name="aws-properties-as-policy-return-values-ref"></a>

When you specify an `AWS::AutoScaling::ScalingPolicy` type as an argument to the `Ref` function, AWS CloudFormation returns the policy Amazon Resource Name \(ARN\)\. For example: `arn:aws:autoscaling:us-east-2:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-as-policy--examples"></a>

The following examples specify scaling policies for an Auto Scaling group\.

### Target Tracking Scaling Policy<a name="aws-properties-as-policy--examples--Target_Tracking_Scaling_Policy"></a>

The following example is a target tracking scaling policy based on the `ASGAverageCPUUtilization` metric\. The `TargetValue` property of the scaling policy references a `PolicyTargetValue` [parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) value from the same template\.

#### JSON<a name="aws-properties-as-policy--examples--Target_Tracking_Scaling_Policy--json"></a>

```
{
  "AWSTemplateFormatVersion":"2018-09-09",
  "Parameters":{
    "AMI":{
      "Type":"String"
    },
    "Subnets":{
      "Type":"CommaDelimitedList"
    },
    "AZs":{
      "Type":"CommaDelimitedList"
    },
    "PolicyTargetValue":{
      "Type":"String"
    }
  },
  "Resources":{
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":{
          "Ref":"AMI"
        },
        "InstanceType":"t2.large"
      }
    },
    "myCPUPolicy":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASGroup"
        },
        "PolicyType":"TargetTrackingScaling",
        "TargetTrackingConfiguration":{
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ASGAverageCPUUtilization"
          },
          "TargetValue":{
            "Ref":"PolicyTargetValue"
          }
        }
      }
    },
    "myASGroup":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "MaxSize":"2",
        "AvailabilityZones":{
          "Ref":"AZs"
        },
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        },
        "MinSize":"1",
        "LaunchConfigurationName":{
          "Ref":"myLaunchConfig"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Target_Tracking_Scaling_Policy--yaml"></a>

```
AWSTemplateFormatVersion: 2018-09-09
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
  myLaunchConfig:
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties:
      ImageId: !Ref AMI
      InstanceType: t2.large
  myCPUPolicy:
    Type: AWS::AutoScaling::ScalingPolicy
    Properties:
      AutoScalingGroupName: !Ref myASGroup
      PolicyType: TargetTrackingScaling
      TargetTrackingConfiguration:
        PredefinedMetricSpecification:
          PredefinedMetricType: ASGAverageCPUUtilization
        TargetValue: !Ref PolicyTargetValue
  myASGroup:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      MaxSize: '2'
      AvailabilityZones: !Ref AZs
      VPCZoneIdentifier: !Ref Subnets
      MinSize: '1'
      LaunchConfigurationName: !Ref myLaunchConfig
```

### Step Scaling Policy<a name="aws-properties-as-policy--examples--Step_Scaling_Policy"></a>

The following example is a step scaling policy that increases the number instances by one or two, depending on the size of the alarm breach\. For a breach that is less than 50 units than the threshold value, the policy increases the number of instances by one\. For a breach that is 50 units or more higher than the threshold, the policy increases the number of instances by two\.

#### JSON<a name="aws-properties-as-policy--examples--Step_Scaling_Policy--json"></a>

```
{
  "ASGScaleOutPolicy":{
    "Type":"AWS::AutoScaling::ScalingPolicy",
    "Properties":{
      "AdjustmentType":"ChangeInCapacity",
      "AutoScalingGroupName":{
        "Ref":"myASGroup"
      },
      "PolicyType":"StepScaling",
      "MetricAggregationType":"Average",
      "EstimatedInstanceWarmup":"60",
      "StepAdjustments":[
        {
          "MetricIntervalLowerBound":"0",
          "MetricIntervalUpperBound":"50",
          "ScalingAdjustment":"1"
        },
        {
          "MetricIntervalLowerBound":"50",
          "ScalingAdjustment":"2"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Step_Scaling_Policy--yaml"></a>

```
ASGScaleOutPolicy:
  Type: AWS::AutoScaling::ScalingPolicy
  Properties:
    AdjustmentType: "ChangeInCapacity"
    AutoScalingGroupName:
      Ref: "myASGroup"
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

### Simple Scaling Policy<a name="aws-properties-as-policy--examples--Simple_Scaling_Policy"></a>

The following example is a simple scaling policy that increases the number instances by one when it is triggered\.

#### JSON<a name="aws-properties-as-policy--examples--Simple_Scaling_Policy--json"></a>

```
{
  "ASGScaleOutPolicy":{
    "Type":"AWS::AutoScaling::ScalingPolicy",
    "Properties":{
      "AdjustmentType":"ChangeInCapacity",
      "PolicyType":"SimpleScaling",
      "Cooldown":"60",
      "AutoScalingGroupName":{
        "Ref":"myASGroup"
      },
      "ScalingAdjustment":1
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Simple_Scaling_Policy--yaml"></a>

```
ASGScaleOutPolicy:
  Type: AWS::AutoScaling::ScalingPolicy
  Properties:
    AdjustmentType: "ChangeInCapacity"
    PolicyType: "SimpleScaling"
    Cooldown: "60"
    AutoScalingGroupName:
      Ref: "myASGroup"
    ScalingAdjustment: 1
```
