# AWS::AutoScaling::ScalingPolicy<a name="aws-properties-as-policy"></a>

The AWS::AutoScaling::ScalingPolicy resource specifies an Amazon EC2 Auto Scaling scaling policy so that the Auto Scaling group can change the number of instances available for your application in response to changing demand\.

For more information about using scaling policies to scale your Auto Scaling group automatically, see [Dynamic scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) in the *Amazon EC2 Auto Scaling User Guide*\. 

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
      "[StepAdjustments](#cfn-as-scalingpolicy-stepadjustments)" : [ StepAdjustment, ... ],
      "[TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration)" : TargetTrackingConfiguration
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
    - StepAdjustment
  [TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration): 
    TargetTrackingConfiguration
```

## Properties<a name="aws-properties-as-policy-properties"></a>

`AdjustmentType`  <a name="cfn-as-scalingpolicy-adjustmenttype"></a>
Specifies how the scaling adjustment is interpreted\. The valid values are `ChangeInCapacity`, `ExactCapacity`, and `PercentChangeInCapacity`\.   
Required if the policy type is `StepScaling` or `SimpleScaling`\. For more information, see [Scaling adjustment types](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-adjustment) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoScalingGroupName`  <a name="cfn-as-scalingpolicy-autoscalinggroupname"></a>
The name or Amazon Resource Name \(ARN\) of the Auto Scaling group that you want to attach the policy to\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cooldown`  <a name="cfn-as-scalingpolicy-cooldown"></a>
The duration of the policy's cooldown period, in seconds\. When a cooldown period is specified here, it overrides the default cooldown period defined for the Auto Scaling group\.  
Valid only if the policy type is `SimpleScaling`\. For more information, see [Scaling cooldowns for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EstimatedInstanceWarmup`  <a name="cfn-as-scalingpolicy-estimatedinstancewarmup"></a>
The estimated time, in seconds, until a newly launched instance can contribute to the CloudWatch metrics\. If not provided, the default is to use the value from the default cooldown period for the Auto Scaling group\.   
Valid only if the policy type is `TargetTrackingScaling` or `StepScaling`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricAggregationType`  <a name="cfn-as-scalingpolicy-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. The valid values are `Minimum`, `Maximum`, and `Average`\. If the aggregation type is null, the value is treated as `Average`\.   
Valid only if the policy type is `StepScaling`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinAdjustmentMagnitude`  <a name="cfn-as-scalingpolicy-minadjustmentmagnitude"></a>
The minimum value to scale by when the adjustment type is `PercentChangeInCapacity`\. For example, suppose that you create a step scaling policy to scale out an Auto Scaling group by 25 percent and you specify a `MinAdjustmentMagnitude` of 2\. If the group has 4 instances and the scaling policy is performed, 25 percent of 4 is 1\. However, because you specified a `MinAdjustmentMagnitude` of 2, Amazon EC2 Auto Scaling scales out the group by 2 instances\.   
Valid only if the policy type is `StepScaling` or `SimpleScaling`\. For more information, see [Scaling adjustment types](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-adjustment) in the *Amazon EC2 Auto Scaling User Guide*\.  
Some Auto Scaling groups use instance weights\. In this case, set the `MinAdjustmentMagnitude` to a value that is at least as large as your largest instance weight\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-as-scalingpolicy-policytype"></a>
One of the following policy types:   
+  `TargetTrackingScaling` 
+  `StepScaling` 
+  `SimpleScaling` \(default\)
For more information, see [Target tracking scaling policies](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html) and [Step and simple scaling policies](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-as-scalingpolicy-scalingadjustment"></a>
The amount by which to scale, based on the specified adjustment type\. A positive value adds to the current capacity while a negative number removes from the current capacity\. For exact capacity, you must specify a positive value\.   
Required if the policy type is `SimpleScaling`\. \(Not used with any other policy type\.\)   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepAdjustments`  <a name="cfn-as-scalingpolicy-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.   
Required if the policy type is `StepScaling`\. \(Not used with any other policy type\.\)   
*Required*: Conditional  
*Type*: List of [StepAdjustment](aws-properties-autoscaling-scalingpolicy-stepadjustments.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingConfiguration`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration"></a>
A target tracking scaling policy\. Includes support for predefined or customized metrics\.  
The following predefined metrics are available:  
+ `ASGAverageCPUUtilization`
+ `ASGAverageNetworkIn`
+ `ASGAverageNetworkOut`
+ `ALBRequestCountPerTarget` 
If you specify `ALBRequestCountPerTarget` for the metric, you must specify the `ResourceLabel` property with the `PredefinedMetricSpecification`\.  
*Required*: Conditional  
*Type*: [TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-as-policy-return-values"></a>

### Ref<a name="aws-properties-as-policy-return-values-ref"></a>

When you specify an `AWS::AutoScaling::ScalingPolicy` type as an argument to the `Ref` function, AWS CloudFormation returns the policy Amazon Resource Name \(ARN\)\. For example: `arn:aws:autoscaling:us-east-2:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-properties-as-policy--examples"></a>

The following examples specify scaling policies for an Auto Scaling group\.

For more template snippets, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

### Target tracking scaling policy<a name="aws-properties-as-policy--examples--Target_tracking_scaling_policy"></a>

The following example creates an Auto Scaling group with two target tracking scaling policies based on the `ASGAverageCPUUtilization` and `ALBRequestCountPerTarget` metrics\. The properties of each of these policies include a `TargetValue` property that references a [parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) value from the same template\.

#### JSON<a name="aws-properties-as-policy--examples--Target_tracking_scaling_policy--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "AMI":{
      "Type":"String"
    },
    "Subnets":{
      "Type":"CommaDelimitedList"
    },
    "VPC":{
      "Type":"String"
    },
    "CPUPolicyTargetValue":{
      "Type":"String"
    },
    "ALBRequestCountTargetValue":{
      "Type":"String"
    }
  },
  "Resources":{
    "myLoadBalancer":{
      "Type":"AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties":{
        "Subnets":{
          "Ref":"Subnets"
        }
      }
    },
    "myLoadBalancerListener":{
      "Type":"AWS::ElasticLoadBalancingV2::Listener",
      "Properties":{
        "DefaultActions":[
          {
            "TargetGroupArn":{
              "Ref":"myTargetGroup"
            },
            "Type":"forward"
          }
        ],
        "LoadBalancerArn":{
          "Ref":"myLoadBalancer"
        },
        "Port":80,
        "Protocol":"HTTP"
      }
    },
    "myTargetGroup":{
      "Type":"AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties":{
        "Name":"myTargetGroup",
        "Port":80,
        "Protocol":"HTTP",
        "VpcId":{
          "Ref":"VPC"
        }
      }
    },
    "myLaunchConfig":{
      "Type":"AWS::AutoScaling::LaunchConfiguration",
      "Properties":{
        "ImageId":{
          "Ref":"AMI"
        },
        "InstanceType":"t2.large"
      }
    },
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "MaxSize":"2",
        "MinSize":"1",
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        },
        "LaunchConfigurationName":{
          "Ref":"myLaunchConfig"
        },
        "TargetGroupARNs":[
          {
            "Ref":"myTargetGroup"
          }
        ]
      }
    },
    "myCPUPolicy":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"TargetTrackingScaling",
        "TargetTrackingConfiguration":{
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ASGAverageCPUUtilization"
          },
          "TargetValue":{
            "Ref":"CPUPolicyTargetValue"
          }
        }
      }
    },
    "myALBRequestCountPolicy":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"TargetTrackingScaling",
        "TargetTrackingConfiguration":{
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ALBRequestCountPerTarget",
            "ResourceLabel":{
              "Fn::Join":[
                "/",
                [
                  {
                    "Fn::GetAtt":[
                      "myLoadBalancer",
                      "LoadBalancerFullName"
                    ]
                  },
                  {
                    "Fn::GetAtt":[
                      "myTargetGroup",
                      "TargetGroupFullName"
                    ]
                  }
                ]
              ]
            }
          },
          "TargetValue":{
            "Ref":"ALBRequestCountTargetValue"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Target_tracking_scaling_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AMI:
    Type: String
  Subnets:
    Type: CommaDelimitedList
  VPC:
    Type: String
  CPUPolicyTargetValue:
    Type: String
  ALBRequestCountTargetValue:
    Type: String
Resources:
  myLoadBalancer:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Subnets: !Ref Subnets
  myLoadBalancerListener:
    Type: "AWS::ElasticLoadBalancingV2::Listener"
    Properties:
      DefaultActions:
        - TargetGroupArn: !Ref myTargetGroup
          Type: forward
      LoadBalancerArn: !Ref myLoadBalancer
      Port: 80
      Protocol: HTTP
  myTargetGroup:
    Type: "AWS::ElasticLoadBalancingV2::TargetGroup"
    Properties:
      Name: myTargetGroup
      Port: 80
      Protocol: HTTP
      VpcId: !Ref VPC
  myLaunchConfig:
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties:
      ImageId: !Ref AMI
      InstanceType: t2.large
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      MaxSize: '2'
      MinSize: '1'
      VPCZoneIdentifier: !Ref Subnets
      LaunchConfigurationName: !Ref myLaunchConfig
      TargetGroupARNs:
        - !Ref myTargetGroup
  myCPUPolicy:
    Type: AWS::AutoScaling::ScalingPolicy
    Properties:
      AutoScalingGroupName: !Ref myASG
      PolicyType: TargetTrackingScaling
      TargetTrackingConfiguration:
        PredefinedMetricSpecification:
          PredefinedMetricType: ASGAverageCPUUtilization
        TargetValue: !Ref CPUPolicyTargetValue
  myALBRequestCountPolicy:
    Type: AWS::AutoScaling::ScalingPolicy
    Properties:
      AutoScalingGroupName: !Ref myASG
      PolicyType: TargetTrackingScaling
      TargetTrackingConfiguration:
        PredefinedMetricSpecification:
          PredefinedMetricType: ALBRequestCountPerTarget
          ResourceLabel: !Join 
            - '/' 
            - - !GetAtt myLoadBalancer.LoadBalancerFullName
              - !GetAtt myTargetGroup.TargetGroupFullName
        TargetValue: !Ref ALBRequestCountTargetValue
```

### Step scaling policy<a name="aws-properties-as-policy--examples--Step_scaling_policy"></a>

The following example creates a scaling policy with the `StepScaling` policy type and the `ChangeInCapacity` adjustment type\. You must also create a CloudWatch alarm that monitors a CloudWatch metric for your Auto Scaling group\. You can associate a CloudWatch alarm with only one scaling policy\. 

When the associated alarm is triggered, the policy increases the capacity of the Auto Scaling group based on the following step adjustments \(assuming a CloudWatch alarm threshold of 70 percent\): 
+ Increase capacity by 1 when the value of the metric is greater than or equal to 70 percent but less than 85 percent 
+ Increase capacity by 2 when the value of the metric is greater than or equal to 85 percent but less than 95 percent 
+ Increase capacity by 3 when the value of the metric is greater than or equal to 95 percent 

#### JSON<a name="aws-properties-as-policy--examples--Step_scaling_policy--json"></a>

```
{
  "Resources":{
    "ASGScalingPolicyHigh":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AdjustmentType":"ChangeInCapacity",
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"StepScaling",
        "MetricAggregationType":"Average",
        "EstimatedInstanceWarmup":60,
        "StepAdjustments":[
          {
            "MetricIntervalLowerBound":0,
            "MetricIntervalUpperBound":15,
            "ScalingAdjustment":1
          },
          {
            "MetricIntervalLowerBound":15,
            "MetricIntervalUpperBound":25,
            "ScalingAdjustment":2
          },
          {
            "MetricIntervalLowerBound":25,
            "ScalingAdjustment":3
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Step_scaling_policy--yaml"></a>

```
---
Resources:
  ASGScalingPolicyHigh: 
    Type: AWS::AutoScaling::ScalingPolicy
    Properties: 
      AdjustmentType: "ChangeInCapacity"
      AutoScalingGroupName: 
        Ref: "myASG"
      PolicyType: "StepScaling"
      MetricAggregationType: "Average"
      EstimatedInstanceWarmup: 60
      StepAdjustments: 
        - MetricIntervalLowerBound: 0
          MetricIntervalUpperBound: 15
          ScalingAdjustment: 1
        - MetricIntervalLowerBound: 15
          MetricIntervalUpperBound: 25
          ScalingAdjustment: 2
        - MetricIntervalLowerBound: 25
          ScalingAdjustment: 3
```

### Simple scaling policy<a name="aws-properties-as-policy--examples--Simple_scaling_policy"></a>

The following example creates a scaling policy with the `SimpleScaling` policy type and the `ChangeInCapacity` adjustment type\. The policy increases capacity by one when it is triggered\. You must also create a CloudWatch alarm that monitors a CloudWatch metric for your Auto Scaling group\. You can associate a CloudWatch alarm with only one scaling policy\. 

#### JSON<a name="aws-properties-as-policy--examples--Simple_scaling_policy--json"></a>

```
{
  "Resources":{
    "ASGScalingPolicyHigh":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AdjustmentType":"ChangeInCapacity",
        "PolicyType":"SimpleScaling",
        "Cooldown":"300",
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "ScalingAdjustment":1
      }
    }
  }
}
```

#### YAML<a name="aws-properties-as-policy--examples--Simple_scaling_policy--yaml"></a>

```
---
Resources:
  ASGScalingPolicyHigh: 
    Type: AWS::AutoScaling::ScalingPolicy
    Properties: 
      AdjustmentType: "ChangeInCapacity"
      PolicyType: "SimpleScaling"
      Cooldown: "300"
      AutoScalingGroupName: 
        Ref: "myASG"
      ScalingAdjustment: 1
```