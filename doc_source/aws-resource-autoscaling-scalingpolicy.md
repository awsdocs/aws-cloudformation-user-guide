# AWS::AutoScaling::ScalingPolicy<a name="aws-resource-autoscaling-scalingpolicy"></a>

The `AWS::AutoScaling::ScalingPolicy` resource specifies an Amazon EC2 Auto Scaling scaling policy so that the Auto Scaling group can scale the number of instances available for your application\.

For more information about using scaling policies to scale your Auto Scaling group automatically, see [Dynamic scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scale-based-on-demand.html) and [Predictive scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-resource-autoscaling-scalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-scalingpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::ScalingPolicy",
  "Properties" : {
      "[AdjustmentType](#cfn-autoscaling-scalingpolicy-adjustmenttype)" : String,
      "[AutoScalingGroupName](#cfn-autoscaling-scalingpolicy-autoscalinggroupname)" : String,
      "[Cooldown](#cfn-autoscaling-scalingpolicy-cooldown)" : String,
      "[EstimatedInstanceWarmup](#cfn-autoscaling-scalingpolicy-estimatedinstancewarmup)" : Integer,
      "[MetricAggregationType](#cfn-autoscaling-scalingpolicy-metricaggregationtype)" : String,
      "[MinAdjustmentMagnitude](#cfn-autoscaling-scalingpolicy-minadjustmentmagnitude)" : Integer,
      "[PolicyType](#cfn-autoscaling-scalingpolicy-policytype)" : String,
      "[PredictiveScalingConfiguration](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration)" : PredictiveScalingConfiguration,
      "[ScalingAdjustment](#cfn-autoscaling-scalingpolicy-scalingadjustment)" : Integer,
      "[StepAdjustments](#cfn-autoscaling-scalingpolicy-stepadjustments)" : [ StepAdjustment, ... ],
      "[TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration)" : TargetTrackingConfiguration
    }
}
```

### YAML<a name="aws-resource-autoscaling-scalingpolicy-syntax.yaml"></a>

```
Type: AWS::AutoScaling::ScalingPolicy
Properties: 
  [AdjustmentType](#cfn-autoscaling-scalingpolicy-adjustmenttype): String
  [AutoScalingGroupName](#cfn-autoscaling-scalingpolicy-autoscalinggroupname): String
  [Cooldown](#cfn-autoscaling-scalingpolicy-cooldown): String
  [EstimatedInstanceWarmup](#cfn-autoscaling-scalingpolicy-estimatedinstancewarmup): Integer
  [MetricAggregationType](#cfn-autoscaling-scalingpolicy-metricaggregationtype): String
  [MinAdjustmentMagnitude](#cfn-autoscaling-scalingpolicy-minadjustmentmagnitude): Integer
  [PolicyType](#cfn-autoscaling-scalingpolicy-policytype): String
  [PredictiveScalingConfiguration](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration): 
    PredictiveScalingConfiguration
  [ScalingAdjustment](#cfn-autoscaling-scalingpolicy-scalingadjustment): Integer
  [StepAdjustments](#cfn-autoscaling-scalingpolicy-stepadjustments): 
    - StepAdjustment
  [TargetTrackingConfiguration](#cfn-autoscaling-scalingpolicy-targettrackingconfiguration): 
    TargetTrackingConfiguration
```

## Properties<a name="aws-resource-autoscaling-scalingpolicy-properties"></a>

`AdjustmentType`  <a name="cfn-autoscaling-scalingpolicy-adjustmenttype"></a>
Specifies how the scaling adjustment is interpreted \(for example, an absolute number or a percentage\)\. The valid values are `ChangeInCapacity`, `ExactCapacity`, and `PercentChangeInCapacity`\.  
Required if the policy type is `StepScaling` or `SimpleScaling`\. For more information, see [Scaling adjustment types](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-adjustment) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoScalingGroupName`  <a name="cfn-autoscaling-scalingpolicy-autoscalinggroupname"></a>
The name of the Auto Scaling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Cooldown`  <a name="cfn-autoscaling-scalingpolicy-cooldown"></a>
A cooldown period, in seconds, that applies to a specific simple scaling policy\. When a cooldown period is specified here, it overrides the default cooldown\.  
Valid only if the policy type is `SimpleScaling`\. For more information, see [Scaling cooldowns for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/Cooldown.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
Default: None  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EstimatedInstanceWarmup`  <a name="cfn-autoscaling-scalingpolicy-estimatedinstancewarmup"></a>
 *Not needed if the default instance warmup is defined for the group\.*   
The estimated time, in seconds, until a newly launched instance can contribute to the CloudWatch metrics\. This warm\-up period applies to instances launched due to a specific target tracking or step scaling policy\. When a warm\-up period is specified here, it overrides the default instance warmup\.  
Valid only if the policy type is `TargetTrackingScaling` or `StepScaling`\.  
The default is to use the value for the default instance warmup defined for the group\. If default instance warmup is null, then `EstimatedInstanceWarmup` falls back to the value of default cooldown\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricAggregationType`  <a name="cfn-autoscaling-scalingpolicy-metricaggregationtype"></a>
The aggregation type for the CloudWatch metrics\. The valid values are `Minimum`, `Maximum`, and `Average`\. If the aggregation type is null, the value is treated as `Average`\.  
Valid only if the policy type is `StepScaling`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinAdjustmentMagnitude`  <a name="cfn-autoscaling-scalingpolicy-minadjustmentmagnitude"></a>
The minimum value to scale by when the adjustment type is `PercentChangeInCapacity`\. For example, suppose that you create a step scaling policy to scale out an Auto Scaling group by 25 percent and you specify a `MinAdjustmentMagnitude` of 2\. If the group has 4 instances and the scaling policy is performed, 25 percent of 4 is 1\. However, because you specified a `MinAdjustmentMagnitude` of 2, Amazon EC2 Auto Scaling scales out the group by 2 instances\.  
Valid only if the policy type is `StepScaling` or `SimpleScaling`\. For more information, see [Scaling adjustment types](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html#as-scaling-adjustment) in the *Amazon EC2 Auto Scaling User Guide*\.  
Some Auto Scaling groups use instance weights\. In this case, set the `MinAdjustmentMagnitude` to a value that is at least as large as your largest instance weight\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-autoscaling-scalingpolicy-policytype"></a>
One of the following policy types:   
+  `TargetTrackingScaling` 
+  `StepScaling` 
+  `SimpleScaling` \(default\)
+  `PredictiveScaling` 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PredictiveScalingConfiguration`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration"></a>
A predictive scaling policy\. Provides support for predefined and custom metrics\.  
Predefined metrics include CPU utilization, network in/out, and the Application Load Balancer request count\.  
Required if the policy type is `PredictiveScaling`\.  
*Required*: Conditional  
*Type*: [PredictiveScalingConfiguration](aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingAdjustment`  <a name="cfn-autoscaling-scalingpolicy-scalingadjustment"></a>
The amount by which to scale, based on the specified adjustment type\. A positive value adds to the current capacity while a negative number removes from the current capacity\. For exact capacity, you must specify a positive value\.  
Required if the policy type is `SimpleScaling`\. \(Not used with any other policy type\.\)   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepAdjustments`  <a name="cfn-autoscaling-scalingpolicy-stepadjustments"></a>
A set of adjustments that enable you to scale based on the size of the alarm breach\.  
Required if the policy type is `StepScaling`\. \(Not used with any other policy type\.\)   
*Required*: Conditional  
*Type*: List of [StepAdjustment](aws-properties-autoscaling-scalingpolicy-stepadjustment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingConfiguration`  <a name="cfn-autoscaling-scalingpolicy-targettrackingconfiguration"></a>
A target tracking scaling policy\. Provides support for predefined or custom metrics\.  
The following predefined metrics are available:  
+  `ASGAverageCPUUtilization` 
+  `ASGAverageNetworkIn` 
+  `ASGAverageNetworkOut` 
+  `ALBRequestCountPerTarget` 
If you specify `ALBRequestCountPerTarget` for the metric, you must specify the `ResourceLabel` property with the `PredefinedMetricSpecification`\.  
Required if the policy type is `TargetTrackingScaling`\.  
*Required*: Conditional  
*Type*: [TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-autoscaling-scalingpolicy-return-values"></a>

### Ref<a name="aws-resource-autoscaling-scalingpolicy-return-values-ref"></a>

When you specify an `AWS::AutoScaling::ScalingPolicy` type as an argument to the `Ref` function, CloudFormation returns the policy Amazon Resource Name \(ARN\)\. For example: `arn:aws:autoscaling:us-east-2:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-autoscaling-scalingpolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-autoscaling-scalingpolicy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`PolicyName`  <a name="PolicyName-fn::getatt"></a>
Returns the name of a scaling policy\.

## Remarks<a name="aws-resource-autoscaling-scalingpolicy--remarks"></a>

When you create the [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html) resource for a step or simple scaling policy, specify the name of the scaling policy in the `AlarmActions` property\. For an example snippet, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

## Examples<a name="aws-resource-autoscaling-scalingpolicy--examples"></a>

The following examples specify scaling policies for an Auto Scaling group\.

For more template snippets, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

### Predictive scaling policy<a name="aws-resource-autoscaling-scalingpolicy--examples--Predictive_scaling_policy"></a>

The following template snippet shows a predictive scaling policy configuration that uses CPU utilization metrics with a target utilization of 70\. Because `ForecastOnly` mode is specified, Amazon EC2 Auto Scaling generates forecasts with traffic predictions for the two days ahead, but does not actively scale the group\. 

#### JSON<a name="aws-resource-autoscaling-scalingpolicy--examples--Predictive_scaling_policy--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Resources":{
    "myPredictiveScalingPolicy":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"PredictiveScaling",
        "PredictiveScalingConfiguration":{
          "MetricSpecifications":[
            {
              "TargetValue":70,
              "PredefinedMetricPairSpecification":{
                "PredefinedMetricType":"ASGCPUUtilization"
              }
            }
          ],
          "Mode":"ForecastOnly"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scalingpolicy--examples--Predictive_scaling_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myPredictiveScalingPolicy:
    Type: 'AWS::AutoScaling::ScalingPolicy'
    Properties:
      AutoScalingGroupName: !Ref myASG
      PolicyType: PredictiveScaling
      PredictiveScalingConfiguration:
        MetricSpecifications:
          - TargetValue: '70'
            PredefinedMetricPairSpecification:
              PredefinedMetricType: ASGCPUUtilization
        Mode: ForecastOnly
```

### Target tracking scaling policy<a name="aws-resource-autoscaling-scalingpolicy--examples--Target_tracking_scaling_policy"></a>

The following example creates an Auto Scaling group with two target tracking scaling policies based on the `ASGAverageCPUUtilization` and `ALBRequestCountPerTarget` metrics\. The properties of each of these policies include a `TargetValue` property that references a [parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) value from the same template\.

Because `Monitoring` is enabled in the launch template, EC2 metric data will be available at 1\-minute intervals \(known as detailed monitoring\) through CloudWatch\.

The `DefaultInstanceWarmup` property is set to 30 seconds, to represent the amount of time that it takes for resource consumption to become stable after an instance reaches the `InService` state\. For more information, see [Set the default instance warmup for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-default-instance-warmup.html) in the *Amazon EC2 Auto Scaling User Guide*\.

To create a scaling policy for the `ALBRequestCountPerTarget` metric and the load balancer in the same stack template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the `AWS::ElasticLoadBalancingV2::Listener` resource\. 

#### JSON<a name="aws-resource-autoscaling-scalingpolicy--examples--Target_tracking_scaling_policy--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "AmiId":{
      "Type":"String"
    },
    "Subnets":{
      "Type": "List<AWS::EC2::Subnet::Id>",
      "Description": "At least two public subnets in different Availability Zones in the selected VPC"
    },
    "VPC":{
      "Type": "AWS::EC2::VPC::Id",
      "Description": "A VPC that allows the load balancer access to the Internet"
    },
    "InstanceSecurityGroup":{
      "Type": "List<AWS::EC2::SecurityGroup::Id>",
      "Description": "A security group in the selected VPC that allows HTTP access on the inbound port"
    },
    "CPUPolicyTargetValue":{
      "Type":"String",
      "Description": "The target utilization for the CPU metric"
    },
    "ALBRequestCountTargetValue":{
      "Type":"String",
      "Description": "The optimal average request count per instance during any one-minute interval"
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
    "myLaunchTemplate": {
      "Type": "AWS::EC2::LaunchTemplate",
      "Properties": {
        "LaunchTemplateName": { "Fn::Sub": "${AWS::StackName}-launch-template" },
        "LaunchTemplateData": {
          "ImageId": { "Ref": "AmiId" },
          "InstanceType": "t3.micro",
          "SecurityGroupIds": [ { "Ref":"InstanceSecurityGroup" } ],
          "Monitoring": { "Enabled": true }
        }
      }
    },
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "LaunchTemplate": {
          "LaunchTemplateId": { "Ref": "myLaunchTemplate" },
          "Version": { "Fn::GetAtt": [ "myLaunchTemplate", "LatestVersionNumber" ] }
        },      
        "MaxSize":"2",
        "MinSize":"1",
        "DefaultInstanceWarmup": 30,
        "VPCZoneIdentifier": { "Ref":"Subnets" },
        "TargetGroupARNs":[ { "Ref":"myTargetGroup" } ]
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
      "DependsOn" : "myLoadBalancerListener",
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

#### YAML<a name="aws-resource-autoscaling-scalingpolicy--examples--Target_tracking_scaling_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AmiId:
    Type: String
  Subnets:
    Type: 'List<AWS::EC2::Subnet::Id>'
    Description: At least two public subnets in different Availability Zones in the selected VPC
  VPC:
    Type: 'AWS::EC2::VPC::Id'
    Description: A VPC that allows the load balancer access to the Internet
  InstanceSecurityGroup:
    Type: 'List<AWS::EC2::SecurityGroup::Id>'
    Description: A security group in the selected VPC that allows HTTP access on the inbound port
  CPUPolicyTargetValue:
    Type: String
    Description: The target utilization for the CPU metric
  ALBRequestCountTargetValue:
    Type: String
    Description: The optimal average request count per instance during any one-minute interval
Resources:
  myLoadBalancer:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Subnets: !Ref Subnets
  myLoadBalancerListener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions:
        - TargetGroupArn: !Ref myTargetGroup
          Type: forward
      LoadBalancerArn: !Ref myLoadBalancer
      Port: 80
      Protocol: HTTP
  myTargetGroup:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      Name: myTargetGroup
      Port: 80
      Protocol: HTTP
      VpcId: !Ref VPC
  myLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
      LaunchTemplateData:
        ImageId: !Ref AmiId
        InstanceType: t3.micro
        SecurityGroupIds: 
          - !Ref InstanceSecurityGroup
        Monitoring: 
          Enabled: true
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !GetAtt myLaunchTemplate.LatestVersionNumber
      MaxSize: '2'
      MinSize: '1'
      DefaultInstanceWarmup: 30
      VPCZoneIdentifier: !Ref Subnets
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
    DependsOn: myLoadBalancerListener
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

### Step scaling policy<a name="aws-resource-autoscaling-scalingpolicy--examples--Step_scaling_policy"></a>

The following example creates a scaling policy with the `StepScaling` policy type and the `ChangeInCapacity` adjustment type\. You must also create a CloudWatch alarm that monitors a CloudWatch metric for your Auto Scaling group\. You can associate a CloudWatch alarm with only one scaling policy\. 

When the associated alarm is triggered, the policy increases the capacity of the Auto Scaling group based on the following step adjustments \(assuming a CloudWatch alarm threshold of 70 percent\): 
+ Increase capacity by 1 when the value of the metric is greater than or equal to 70 percent but less than 85 percent 
+ Increase capacity by 2 when the value of the metric is greater than or equal to 85 percent but less than 95 percent 
+ Increase capacity by 3 when the value of the metric is greater than or equal to 95 percent 

#### JSON<a name="aws-resource-autoscaling-scalingpolicy--examples--Step_scaling_policy--json"></a>

```
{
  "Resources":{
    "ASGScalingPolicyHigh":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"StepScaling",
        "AdjustmentType":"ChangeInCapacity",
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

#### YAML<a name="aws-resource-autoscaling-scalingpolicy--examples--Step_scaling_policy--yaml"></a>

```
---
Resources:
  ASGScalingPolicyHigh: 
    Type: AWS::AutoScaling::ScalingPolicy
    Properties: 
      AutoScalingGroupName: !Ref myASG
      PolicyType: StepScaling
      AdjustmentType: ChangeInCapacity
      MetricAggregationType: Average
      EstimatedInstanceWarmup: '60'
      StepAdjustments: 
        - MetricIntervalLowerBound: '0'
          MetricIntervalUpperBound: '15'
          ScalingAdjustment: '1'
        - MetricIntervalLowerBound: '15'
          MetricIntervalUpperBound: '25'
          ScalingAdjustment: '2'
        - MetricIntervalLowerBound: '25'
          ScalingAdjustment: '3'
```

### Simple scaling policy<a name="aws-resource-autoscaling-scalingpolicy--examples--Simple_scaling_policy"></a>

The following example creates a scaling policy with the `SimpleScaling` policy type and the `ChangeInCapacity` adjustment type\. The policy increases capacity by one when it is triggered\. You must also create a CloudWatch alarm that monitors a CloudWatch metric for your Auto Scaling group\. You can associate a CloudWatch alarm with only one scaling policy\. 

#### JSON<a name="aws-resource-autoscaling-scalingpolicy--examples--Simple_scaling_policy--json"></a>

```
{
  "Resources":{
    "ASGScalingPolicyHigh":{
      "Type":"AWS::AutoScaling::ScalingPolicy",
      "Properties":{
        "AutoScalingGroupName":{
          "Ref":"myASG"
        },
        "PolicyType":"SimpleScaling",
        "AdjustmentType":"ChangeInCapacity",
        "ScalingAdjustment":1
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscaling-scalingpolicy--examples--Simple_scaling_policy--yaml"></a>

```
---
Resources:
  ASGScalingPolicyHigh: 
    Type: AWS::AutoScaling::ScalingPolicy
    Properties: 
      AutoScalingGroupName: !Ref myASG
      PolicyType: SimpleScaling
      AdjustmentType: ChangeInCapacity
      ScalingAdjustment: '1'
```

## See also<a name="aws-resource-autoscaling-scalingpolicy--seealso"></a>
+ [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)
+ [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutScalingPolicy.html) in the *Amazon EC2 Auto Scaling API Reference*

