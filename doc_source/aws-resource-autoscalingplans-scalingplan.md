# AWS::AutoScalingPlans::ScalingPlan<a name="aws-resource-autoscalingplans-scalingplan"></a>

The `AWS::AutoScalingPlans::ScalingPlan` resource defines a scaling plan that AWS Auto Scaling uses to scale the following application resources:
+ Amazon EC2 Auto Scaling groups
+ Amazon EC2 Spot Fleet requests 
+ Amazon ECS services
+ Amazon DynamoDB tables and global secondary indexes 
+ Amazon Aurora Replicas 

For more information, see the [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)\. 

## Syntax<a name="aws-resource-autoscalingplans-scalingplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscalingplans-scalingplan-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScalingPlans::ScalingPlan",
  "Properties" : {
      "[ApplicationSource](#cfn-autoscalingplans-scalingplan-applicationsource)" : ApplicationSource,
      "[ScalingInstructions](#cfn-autoscalingplans-scalingplan-scalinginstructions)" : [ ScalingInstruction, ... ]
    }
}
```

### YAML<a name="aws-resource-autoscalingplans-scalingplan-syntax.yaml"></a>

```
Type: AWS::AutoScalingPlans::ScalingPlan
Properties: 
  [ApplicationSource](#cfn-autoscalingplans-scalingplan-applicationsource): 
    ApplicationSource
  [ScalingInstructions](#cfn-autoscalingplans-scalingplan-scalinginstructions): 
    - ScalingInstruction
```

## Properties<a name="aws-resource-autoscalingplans-scalingplan-properties"></a>

`ApplicationSource`  <a name="cfn-autoscalingplans-scalingplan-applicationsource"></a>
A CloudFormation stack or a set of tags\. You can create one scaling plan per application source\. The `ApplicationSource` property must be present to ensure interoperability with the AWS Auto Scaling console\.  
*Required*: Yes  
*Type*: [ApplicationSource](aws-properties-autoscalingplans-scalingplan-applicationsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalingInstructions`  <a name="cfn-autoscalingplans-scalingplan-scalinginstructions"></a>
The scaling instructions\.  
*Required*: Yes  
*Type*: List of [ScalingInstruction](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-autoscalingplans-scalingplan-return-values"></a>

### Ref<a name="aws-resource-autoscalingplans-scalingplan-return-values-ref"></a>

When you pass the logical ID of an `AWS::AutoScalingPlans::ScalingPlan` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the scaling plan\. The format of the ARN is as follows:

`arn:aws:autoscaling:region:123456789012:scalingPlan:scalingPlanName/plan-name:scalingPlanVersion/plan-version `

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-autoscalingplans-scalingplan--examples"></a>

### Scaling plan<a name="aws-resource-autoscalingplans-scalingplan--examples--Scaling_plan"></a>

The following example creates a scaling plan named `myScalingPlan` for an existing Auto Scaling group \([AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\) whose name you specify when launching the stack using this template\. It specifies the `TagFilters` property as the application source\. You can specify any tag key and tag value you want without affecting the stack, as long as the key\-pair is unique for each scaling plan\. This can be any value you choose that helps you identify your scaling plan configuration\. However, if you also want to use the AWS Auto Scaling console to edit the scaling plan, then the tag must match the tag you chose for the Auto Scaling group\.

The [ScalingInstructions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-scalinginstruction.html) property includes information that's required to enable predictive scaling and dynamic scaling\. In this example, the predictive scaling mode specifies `ForecastOnly`\. In which case, AWS Auto Scaling generates forecasts with traffic predictions for the two days ahead, but does not schedule scaling actions to match the forecast\. 

#### JSON<a name="aws-resource-autoscalingplans-scalingplan--examples--Scaling_plan--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "myTagKey":{
      "Type":"String"
    },
    "myTagValue":{
      "Type":"String"
    },
    "myASGroup":{
      "Type":"String",
      "Description":"Name of the Auto Scaling group"
    },
    "ASGMinCapacity":{
      "Type":"Number"
    },
    "ASGMaxCapacity":{
      "Type":"Number"
    },
    "ASGTargetUtilization":{
      "Type":"Number",
      "Default":"50.0"
    },
    "ASGEstimatedInstanceWarmup":{
      "Type":"Number",
      "Default":"600"
    }
  },
  "Resources":{
    "myScalingPlan":{
      "Type":"AWS::AutoScalingPlans::ScalingPlan",
      "Properties":{
        "ApplicationSource":{
          "TagFilters":[
            {
              "Key":{
                "Ref":"myTagKey"
              },
              "Values":[{
                "Ref":"myTagValue"
              }]
            }
          ]
        },
        "ScalingInstructions":[
          {
            "MinCapacity":{
              "Ref":"ASGMinCapacity"
            }, 
            "MaxCapacity":{
              "Ref":"ASGMaxCapacity"
            }, 
            "ServiceNamespace":"autoscaling",
            "ScalableDimension":"autoscaling:autoScalingGroup:DesiredCapacity",
            "ResourceId":{
              "Fn::Join":[
                "/",
                [
                  "autoScalingGroup",
                  {
                    "Ref":"myASGroup"
                  }
                ]
              ]
            },
            "TargetTrackingConfigurations":[
              {
                "PredefinedScalingMetricSpecification":{
                  "PredefinedScalingMetricType":"ASGAverageCPUUtilization"
                },
                "TargetValue":{
                  "Ref":"ASGTargetUtilization"
                }, 
                "EstimatedInstanceWarmup":{
                  "Ref":"ASGEstimatedInstanceWarmup"
                }
              }
            ],
            "PredefinedLoadMetricSpecification":{
              "PredefinedLoadMetricType":"ASGTotalCPUUtilization"
            },
            "PredictiveScalingMode":"ForecastOnly",
            "PredictiveScalingMaxCapacityBehavior":"SetMaxCapacityAboveForecastCapacity",
            "PredictiveScalingMaxCapacityBuffer":25,
            "ScheduledActionBufferTime":600
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-autoscalingplans-scalingplan--examples--Scaling_plan--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  myTagKey:
    Type: String
  myTagValue:
    Type: String
  myASGroup:
    Type: String
    Description: Name of the Auto Scaling group
  ASGMinCapacity:
    Type: Number
  ASGMaxCapacity:
    Type: Number
  ASGTargetUtilization:
    Type: Number
    Default: 50.0
  ASGEstimatedInstanceWarmup:
    Type: Number
    Default: 600
Resources:
  myScalingPlan:
    Type: AWS::AutoScalingPlans::ScalingPlan
    Properties:
      ApplicationSource:
        TagFilters:
          - Key: !Ref myTagKey
            Values:
              - !Ref myTagValue
      ScalingInstructions:
        - MinCapacity: !Ref ASGMinCapacity
          MaxCapacity: !Ref ASGMaxCapacity
          ServiceNamespace: autoscaling
          ScalableDimension: autoscaling:autoScalingGroup:DesiredCapacity
          ResourceId: !Join
            - /
            - - autoScalingGroup
              - !Ref myASGroup
          TargetTrackingConfigurations:
            - PredefinedScalingMetricSpecification:
                PredefinedScalingMetricType: "ASGAverageCPUUtilization"
              TargetValue: !Ref ASGTargetUtilization
              EstimatedInstanceWarmup: !Ref ASGEstimatedInstanceWarmup
          PredefinedLoadMetricSpecification:
            PredefinedLoadMetricType: "ASGTotalCPUUtilization"
          PredictiveScalingMode: "ForecastOnly"
          PredictiveScalingMaxCapacityBehavior: "SetMaxCapacityAboveForecastCapacity"
          PredictiveScalingMaxCapacityBuffer: 25
          ScheduledActionBufferTime: 600
```