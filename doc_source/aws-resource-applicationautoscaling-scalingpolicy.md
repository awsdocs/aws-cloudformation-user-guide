# AWS::ApplicationAutoScaling::ScalingPolicy<a name="aws-resource-applicationautoscaling-scalingpolicy"></a>

The `AWS::ApplicationAutoScaling::ScalingPolicy` resource defines a scaling policy that Application Auto Scaling uses to adjust your application resources\. 

For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\. For more information about scaling policies, see the [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html)\.

For introductory exercises for scaling specific resources, see [Getting Started](https://docs.aws.amazon.com/autoscaling/application/userguide/getting-started.html) in the *Application Auto Scaling User Guide*\.

## Syntax<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
  "Properties" : {
      "[PolicyName](#cfn-applicationautoscaling-scalingpolicy-policyname)" : String,
      "[PolicyType](#cfn-applicationautoscaling-scalingpolicy-policytype)" : String,
      "[ResourceId](#cfn-applicationautoscaling-scalingpolicy-resourceid)" : String,
      "[ScalableDimension](#cfn-applicationautoscaling-scalingpolicy-scalabledimension)" : String,
      "[ScalingTargetId](#cfn-applicationautoscaling-scalingpolicy-scalingtargetid)" : String,
      "[ServiceNamespace](#cfn-applicationautoscaling-scalingpolicy-servicenamespace)" : String,
      "[StepScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration)" : [StepScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.md),
      "[TargetTrackingScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration)" : [TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md)
    }
}
```

### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax.yaml"></a>

```
Type: AWS::ApplicationAutoScaling::ScalingPolicy
Properties: 
  [PolicyName](#cfn-applicationautoscaling-scalingpolicy-policyname): String
  [PolicyType](#cfn-applicationautoscaling-scalingpolicy-policytype): String
  [ResourceId](#cfn-applicationautoscaling-scalingpolicy-resourceid): String
  [ScalableDimension](#cfn-applicationautoscaling-scalingpolicy-scalabledimension): String
  [ScalingTargetId](#cfn-applicationautoscaling-scalingpolicy-scalingtargetid): String
  [ServiceNamespace](#cfn-applicationautoscaling-scalingpolicy-servicenamespace): String
  [StepScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration): 
    [StepScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.md)
  [TargetTrackingScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration): 
    [TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md)
```

## Properties<a name="aws-resource-applicationautoscaling-scalingpolicy-properties"></a>

`PolicyName`  <a name="cfn-applicationautoscaling-scalingpolicy-policyname"></a>
The name of the scaling policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `\p{Print}+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyType`  <a name="cfn-applicationautoscaling-scalingpolicy-policytype"></a>
The Application Auto Scaling policy type\.   
The following policy types are supported:   
`TargetTrackingScaling`—Not supported for Amazon EMR  
`StepScaling`—Not supported for DynamoDB, Comprehend, or Lambda  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-applicationautoscaling-scalingpolicy-resourceid"></a>
The unique resource identifier for the scalable target that this scaling policy applies to\. For valid values, see the `ResourceId` parameter for [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.  
You must specify either the `ResourceId`, `ScalableDimension`, and `ServiceNamespace` properties, or the `ScalingTargetId` property, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalableDimension`  <a name="cfn-applicationautoscaling-scalingpolicy-scalabledimension"></a>
The scalable dimension of the scalable target that this scaling policy applies to\. The scalable dimension contains the service namespace, resource type, and scaling property, such as `ecs:service:DesiredCount` for the desired task count of an Amazon ECS service\. For valid values, see the `ScalableDimension` parameter for [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.  
You must specify either the `ResourceId`, `ScalableDimension`, and `ServiceNamespace` properties, or the `ScalingTargetId` property, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingTargetId`  <a name="cfn-applicationautoscaling-scalingpolicy-scalingtargetid"></a>
The AWS CloudFormation\-generated ID of an Application Auto Scaling scalable target\. For more information about the ID, see the Return Value section of the `AWS::ApplicationAutoScaling::ScalableTarget` resource\.  
You must specify either the `ScalingTargetId` property, or the `ResourceId`, `ScalableDimension`, and `ServiceNamespace` properties, but not both\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceNamespace`  <a name="cfn-applicationautoscaling-scalingpolicy-servicenamespace"></a>
The namespace of the AWS service that provides the resource or `custom-resource` for a resource provided by your own application or service\. For valid values, see the `ServiceNamespace` parameter for [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.  
You must specify either the `ResourceId`, `ScalableDimension`, and `ServiceNamespace` properties, or the `ScalingTargetId` property, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StepScalingPolicyConfiguration`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration"></a>
A step scaling policy\.  
*Required*: No  
*Type*: [StepScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingScalingPolicyConfiguration`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>
A target tracking scaling policy\.  
*Required*: No  
*Type*: [TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-applicationautoscaling-scalingpolicy-return-values"></a>

### Ref<a name="aws-resource-applicationautoscaling-scalingpolicy-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the Application Auto Scaling scaling policy Amazon Resource Name \(ARN\)\. For example: `arn:aws:autoscaling:us-east-2:123456789012:scalingPolicy:12ab3c4d-56789-0ef1-2345-6ghi7jk8lm90:resource/ecs/service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH:policyName/MyStepPolicy`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-applicationautoscaling-scalingpolicy--examples"></a>

The following examples create scaling policies for a scalable target that is registered with Application Auto Scaling\. For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\.

### Target Tracking Scaling Policy with a Predefined Metric Specification for an Amazon DynamoDB Table<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_a_Predefined_Metric_Specification_for_an_Amazon_DynamoDB_Table"></a>

This example both registers a DynamoDB table \([AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)\) as a scalable target and creates a scaling policy with the `TargetTrackingScaling` policy type\. The scaling policy scales the table's write capacity throughput to maintain the target utilization at 50 percent based on the write capacity utilization metric\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_a_Predefined_Metric_Specification_for_an_Amazon_DynamoDB_Table--json"></a>

```
{
  "Resources":{
    "WriteCapacityScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":15,
        "MinCapacity":5,
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/dynamodb.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_DynamoDBTable"
        },
        "ServiceNamespace":"dynamodb",
        "ScalableDimension":"dynamodb:table:WriteCapacityUnits",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "table",
              {
                "Ref":"DDBTable"
              }
            ]
          ]
        }
      }
    },
    "WriteScalingPolicy":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"WriteAutoScalingPolicy",
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"WriteCapacityScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":50.0,
          "ScaleInCooldown":60,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"DynamoDBWriteCapacityUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_a_Predefined_Metric_Specification_for_an_Amazon_DynamoDB_Table--yaml"></a>

```
---
Resources:
  WriteCapacityScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 15
      MinCapacity: 5
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/dynamodb.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_DynamoDBTable'
      ServiceNamespace: dynamodb
      ScalableDimension: dynamodb:table:WriteCapacityUnits
      ResourceId: !Join
        - /
        - - table
          - !Ref DDBTable
  WriteScalingPolicy:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: WriteAutoScalingPolicy
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref WriteCapacityScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 50.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: DynamoDBWriteCapacityUtilization
```

### Target Tracking Scaling Policies for an ECS Service<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policies_for_an_ECS_Service"></a>

The following example both registers an ECS service \([AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)\) as a scalable target and creates two scaling policies with the `TargetTrackingScaling` policy type\. The policies are used to scale the ECS service based on the service's average CPU and memory usage\. 

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policies_for_an_ECS_Service--json"></a>

```
{
  "Resources":{
    "ECSScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":"2",
        "MinCapacity":"1",
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService"
        },
        "ServiceNamespace":"ecs",
        "ScalableDimension":"ecs:service:DesiredCount",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "service",
              {
                "Ref":"cluster"
              },
              {
                "Fn::GetAtt":[
                  "service",
                  "Name"
                ]
              }
            ]
          ]
        }
      }
    },
    "ServiceScalingPolicyCPU":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":{"Fn::Sub":"${AWS::StackName}-target-tracking-cpu70"},
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"ECSScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":70.0,
          "ScaleInCooldown":180,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ECSServiceAverageCPUUtilization"
          }
        }
      }
    },
    "ServiceScalingPolicyMem":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":{"Fn::Sub":"${AWS::StackName}-target-tracking-mem90"},
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"ECSScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":90.0,
          "ScaleInCooldown":180,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ECSServiceAverageMemoryUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policies_for_an_ECS_Service--yaml"></a>

```
---
Resources:
  ECSScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: '2'
      MinCapacity: '1'  
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService'
      ServiceNamespace: ecs
      ScalableDimension: 'ecs:service:DesiredCount'
      ResourceId: !Join 
        - /
        - - service
          - !Ref cluster
          - !GetAtt service.Name
  ServiceScalingPolicyCPU:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu70
      PolicyType: TargetTrackingScaling
      ScalingTargetId:
        Ref: ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 70.0
        ScaleInCooldown: 180
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageCPUUtilization
  ServiceScalingPolicyMem:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-mem90
      PolicyType: TargetTrackingScaling
      ScalingTargetId:
        Ref: ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 90.0
        ScaleInCooldown: 180
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageMemoryUtilization
```

### Target Tracking Scaling Policy for Scale Out Only for an ECS Service<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_for_Scale_Out_Only_for_an_ECS_Service"></a>

The following example applies a target tracking scaling policy with the `ALBRequestCountPerTarget` metric type to an ECS service called `web-app` in the default cluster\. The policy is used to add capacity to the ECS service when the request count per target exceeds the target value\. Because the value of `DisableScaleIn` is set to true, the target tracking policy won't remove capacity from the scalable target\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_for_Scale_Out_Only_for_an_ECS_Service--json"></a>

```
{
  "Resources":{
    "ServiceScalingPolicyALB":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"alb-scale-out-target-tracking-scaling-policy",
        "PolicyType":"TargetTrackingScaling",
        "ServiceNamespace":"ecs",
        "ScalableDimension":"ecs:service:DesiredCount",
        "ResourceId":"service/default/web-app",
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":1000.0,
          "ScaleInCooldown":60,
          "ScaleOutCooldown":60,
          "DisableScaleIn":true,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ALBRequestCountPerTarget",
            "ResourceLabel": "app/EC2Co-EcsEl-1TKLTMITMM0EO/f37c06a68c1748aa/targetgroup/EC2Co-Defau-LDNM7Q3ZH1ZN/6d4ea56ca2d6a18d"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_for_Scale_Out_Only_for_an_ECS_Service--yaml"></a>

```
---
Resources:
  ServiceScalingPolicyALB:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: alb-scale-out-target-tracking-scaling-policy
      PolicyType: TargetTrackingScaling
      ServiceNamespace: ecs
      ScalableDimension: ecs:service:DesiredCount
      ResourceId: service/default/web-app
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 1000.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        DisableScaleIn: true
        PredefinedMetricSpecification:
          PredefinedMetricType: ALBRequestCountPerTarget
          ResourceLabel: app/EC2Co-EcsEl-1TKLTMITMM0EO/f37c06a68c1748aa/targetgroup/EC2Co-Defau-LDNM7Q3ZH1ZN/6d4ea56ca2d6a18d
```

### Step Scaling Policy for Scale Out Only for a Spot Fleet<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out_Only_for_a_Spot_Fleet"></a>

The following example registers a Spot Fleet \([AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html)\) as a scalable target, creates a scheduled action, and creates a scaling policy\. It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property\. 

It creates a scaling policy with the `StepScaling` policy type and the `ChangeInCapacity` adjustment type\. When an associated alarm is triggered, the policy increases the capacity of the scalable target based on the following step adjustments \(assuming a CloudWatch alarm threshold of 70 percent\): 
+ Increase capacity by 1 when the value of the metric is greater than or equal to 70 percent but less than 85 percent 
+ Increase capacity by 2 when the value of the metric is greater than or equal to 85 percent but less than 95 percent 
+ Increase capacity by 3 when the value of the metric is greater than or equal to 95 percent 

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out_Only_for_a_Spot_Fleet--json"></a>

```
{
  "Resources":{
    "SpotFleetScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":2,
        "MinCapacity":1,
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest"
        },
        "ServiceNamespace":"ec2",
        "ScalableDimension":"ec2:spot-fleet-request:TargetCapacity",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "spot-fleet-request",
              {
                "Ref":"ECSSpotFleet"
              }
            ]
          ]
        },
        "ScheduledActions":[
          {
            "EndTime":"2019-12-31T12:00:00.000Z",
            "ScalableTargetAction":{
              "MaxCapacity":"20",
              "MinCapacity":"5"
            },
            "ScheduledActionName":"First",
            "StartTime":"2019-12-25T12:00:00.000Z",
            "Schedule":"cron(0 18 * * ? *)"
          }
        ]
      }
    },
    "SpotFleetPolicyHigh":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"SpotFleetPolicyHigh",
        "PolicyType":"StepScaling",
        "ScalingTargetId":{
          "Ref":"SpotFleetScalableTarget"
        },
        "StepScalingPolicyConfiguration":{
          "AdjustmentType":"ChangeInCapacity",
          "Cooldown":600,
          "MetricAggregationType":"Average",
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
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out_Only_for_a_Spot_Fleet--yaml"></a>

```
---
Resources:
  SpotFleetScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 2
      MinCapacity: 1
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest'
      ServiceNamespace: ec2
      ScalableDimension: 'ec2:spot-fleet-request:TargetCapacity'
      ResourceId: !Join 
        - /
        - - spot-fleet-request
          - !Ref ECSSpotFleet
      ScheduledActions:
        - EndTime: '2019-12-31T12:00:00.000Z'
          ScalableTargetAction:
            MaxCapacity: '20'
            MinCapacity: '5'
          ScheduledActionName: First
          StartTime: '2019-12-25T12:00:00.000Z'
          Schedule: 'cron(0 18 * * ? *)'
  SpotFleetPolicyHigh:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: SpotFleetPolicyHigh
      PolicyType: StepScaling
      ScalingTargetId:
        Ref: SpotFleetScalableTarget
      StepScalingPolicyConfiguration:
        AdjustmentType: ChangeInCapacity
        Cooldown: 600
        MetricAggregationType: Average
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

## See Also<a name="aws-resource-applicationautoscaling-scalingpolicy--seealso"></a>
+ [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html) 
+ [Examples](https://docs.aws.amazon.com/cli/latest/reference/application-autoscaling/put-scaling-policy.html#examples) of Application Auto Scaling scaling policies in the * AWS CLI Command Reference*