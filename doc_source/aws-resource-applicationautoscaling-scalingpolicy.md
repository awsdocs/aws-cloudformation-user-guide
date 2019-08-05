# AWS::ApplicationAutoScaling::ScalingPolicy<a name="aws-resource-applicationautoscaling-scalingpolicy"></a>

The `AWS::ApplicationAutoScaling::ScalingPolicy` resource defines a scaling policy that Application Auto Scaling uses to adjust your application resources\.

For more information, see [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*\. For more information about scaling policies, see the [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html)\.

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
The Application Auto Scaling policy type\. Valid values are `StepScaling` and `TargetTrackingScaling`\.
For DynamoDB, only `TargetTrackingScaling` is supported\. For Amazon ECS, Spot Fleet, and Amazon RDS, both `StepScaling` and `TargetTrackingScaling` are supported\. For any other service, only `StepScaling` is supported\.
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

### Target Tracking Scaling Policy with an Amazon DynamoDB Table<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_an_Amazon_DynamoDB_Table"></a>

This example both registers a [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) as a scalable target and defines a `TargetTrackingScaling` scaling policy that scales the `WriteCapacityUnits` throughput for the table\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_an_Amazon_DynamoDB_Table--json"></a>

```
{
  "Resources":{
    "DDBTable":{
      "Type":"AWS::DynamoDB::Table",
      "Properties":{
        "AttributeDefinitions":[
          {
            "AttributeName":"ArtistId",
            "AttributeType":"S"
          },
          {
            "AttributeName":"Concert",
            "AttributeType":"S"
          },
          {
            "AttributeName":"TicketSales",
            "AttributeType":"S"
          }
        ],
        "KeySchema":[
          {
            "AttributeName":"ArtistId",
            "KeyType":"HASH"
          },
          {
            "AttributeName":"Concert",
            "KeyType":"RANGE"
          }
        ],
        "GlobalSecondaryIndexes":[
          {
            "IndexName":"GSI",
            "KeySchema":[
              {
                "AttributeName":"TicketSales",
                "KeyType":"HASH"
              }
            ],
            "Projection":{
              "ProjectionType":"KEYS_ONLY"
            },
            "ProvisionedThroughput":{
              "ReadCapacityUnits":5,
              "WriteCapacityUnits":5
            }
          }
        ],
        "ProvisionedThroughput":{
          "ReadCapacityUnits":5,
          "WriteCapacityUnits":5
        }
      }
    },
    "WriteCapacityScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":15,
        "MinCapacity":5,
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
        },
        "RoleARN":{
          "Fn::GetAtt":[
            "ScalingRole",
            "Arn"
          ]
        },
        "ScalableDimension":"dynamodb:table:WriteCapacityUnits",
        "ServiceNamespace":"dynamodb"
      }
    },
    "ScalingRole":{
      "Type":"AWS::IAM::Role",
      "Properties":{
        "AssumeRolePolicyDocument":{
          "Version":"2012-10-17",
          "Statement":[
            {
              "Effect":"Allow",
              "Principal":{
                "Service":[
                  "application-autoscaling.amazonaws.com"
                ]
              },
              "Action":[
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Path":"/",
        "Policies":[
          {
            "PolicyName":"root",
            "PolicyDocument":{
              "Version":"2012-10-17",
              "Statement":[
                {
                  "Effect":"Allow",
                  "Action":[
                    "dynamodb:DescribeTable",
                    "dynamodb:UpdateTable",
                    "cloudwatch:PutMetricAlarm",
                    "cloudwatch:DescribeAlarms",
                    "cloudwatch:GetMetricStatistics",
                    "cloudwatch:SetAlarmState",
                    "cloudwatch:DeleteAlarms"
                  ],
                  "Resource":"*"
                }
              ]
            }
          }
        ]
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

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_Tracking_Scaling_Policy_with_an_Amazon_DynamoDB_Table--yaml"></a>

```
Resources:
  DDBTable:
    Type: AWS::DynamoDB::Table
    Properties:
      AttributeDefinitions:
        -
          AttributeName: "ArtistId"

          AttributeType: "S"
        -
          AttributeName: "Concert"

          AttributeType: "S"
        -
          AttributeName: "TicketSales"
          AttributeType: "S"
      KeySchema:
        -
          AttributeName: "ArtistId"
          KeyType: "HASH"
        -
          AttributeName: "Concert"
          KeyType: "RANGE"
      GlobalSecondaryIndexes:
        -
          IndexName: "GSI"
          KeySchema:
            -
              AttributeName: "TicketSales"
              KeyType: "HASH"
          Projection:
            ProjectionType: "KEYS_ONLY"
          ProvisionedThroughput:
            ReadCapacityUnits: 5
            WriteCapacityUnits: 5
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 5
  WriteCapacityScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 15
      MinCapacity: 5
      ResourceId: !Join
        - /
        - - table
          - !Ref DDBTable
      RoleARN: !GetAtt ScalingRole.Arn
      ScalableDimension: dynamodb:table:WriteCapacityUnits
      ServiceNamespace: dynamodb
  ScalingRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          -
            Effect: "Allow"
            Principal:
              Service:
                - application-autoscaling.amazonaws.com
            Action:
              - "sts:AssumeRole"
      Path: "/"
      Policies:
        -
          PolicyName: "root"
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              -
                Effect: "Allow"
                Action:
                  - "dynamodb:DescribeTable"
                  - "dynamodb:UpdateTable"
                  - "cloudwatch:PutMetricAlarm"
                  - "cloudwatch:DescribeAlarms"
                  - "cloudwatch:GetMetricStatistics"
                  - "cloudwatch:SetAlarmState"
                  - "cloudwatch:DeleteAlarms"
                Resource: "*"
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

### Step Scaling Policy for Scale Out<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out"></a>

The following example creates a step scaling policy for a specified scalable target\. When an associated alarm is triggered, the policy increases the capacity of the scalable target by 200%, with a cooldown period of 60 seconds\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out--json"></a>

```
{
  "scalingPolicy":{
    "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
    "Properties":{
      "PolicyName":"MyStepPolicy",
      "PolicyType":"StepScaling",
      "ScalingTargetId":{
        "Ref":"scalableTarget"
      },
      "StepScalingPolicyConfiguration":{
        "AdjustmentType":"PercentChangeInCapacity",
        "Cooldown":60,
        "MetricAggregationType":"Average",
        "StepAdjustments":[
          {
            "MetricIntervalLowerBound":0,
            "ScalingAdjustment":200
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_Scaling_Policy_for_Scale_Out--yaml"></a>

```
scalingPolicy:
  Type: AWS::ApplicationAutoScaling::ScalingPolicy
  Properties:
    PolicyName: MyStepPolicy
    PolicyType: StepScaling
    ScalingTargetId:
      Ref: scalableTarget
    StepScalingPolicyConfiguration:
      AdjustmentType: PercentChangeInCapacity
      Cooldown: 60
      MetricAggregationType: Average
      StepAdjustments:
      - MetricIntervalLowerBound: 0
        ScalingAdjustment: 200
```
