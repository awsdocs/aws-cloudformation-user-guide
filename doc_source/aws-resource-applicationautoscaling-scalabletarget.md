# AWS::ApplicationAutoScaling::ScalableTarget<a name="aws-resource-applicationautoscaling-scalabletarget"></a>

The `AWS::ApplicationAutoScaling::ScalableTarget` resource specifies a resource that Application Auto Scaling can scale\. 

For more information, see [RegisterScalableTarget](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-resource-applicationautoscaling-scalabletarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-applicationautoscaling-scalabletarget-syntax.json"></a>

```
{
  "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
  "Properties" : {
      "[MaxCapacity](#cfn-applicationautoscaling-scalabletarget-maxcapacity)" : Integer,
      "[MinCapacity](#cfn-applicationautoscaling-scalabletarget-mincapacity)" : Integer,
      "[ResourceId](#cfn-applicationautoscaling-scalabletarget-resourceid)" : String,
      "[RoleARN](#cfn-applicationautoscaling-scalabletarget-rolearn)" : String,
      "[ScalableDimension](#cfn-applicationautoscaling-scalabletarget-scalabledimension)" : String,
      "[ScheduledActions](#cfn-applicationautoscaling-scalabletarget-scheduledactions)" : [ [ScheduledAction](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md), ... ],
      "[ServiceNamespace](#cfn-applicationautoscaling-scalabletarget-servicenamespace)" : String,
      "[SuspendedState](#cfn-applicationautoscaling-scalabletarget-suspendedstate)" : [SuspendedState](aws-properties-applicationautoscaling-scalabletarget-suspendedstate.md)
    }
}
```

### YAML<a name="aws-resource-applicationautoscaling-scalabletarget-syntax.yaml"></a>

```
Type: AWS::ApplicationAutoScaling::ScalableTarget
Properties: 
  [MaxCapacity](#cfn-applicationautoscaling-scalabletarget-maxcapacity): Integer
  [MinCapacity](#cfn-applicationautoscaling-scalabletarget-mincapacity): Integer
  [ResourceId](#cfn-applicationautoscaling-scalabletarget-resourceid): String
  [RoleARN](#cfn-applicationautoscaling-scalabletarget-rolearn): String
  [ScalableDimension](#cfn-applicationautoscaling-scalabletarget-scalabledimension): String
  [ScheduledActions](#cfn-applicationautoscaling-scalabletarget-scheduledactions): 
    - [ScheduledAction](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md)
  [ServiceNamespace](#cfn-applicationautoscaling-scalabletarget-servicenamespace): String
  [SuspendedState](#cfn-applicationautoscaling-scalabletarget-suspendedstate): 
    [SuspendedState](aws-properties-applicationautoscaling-scalabletarget-suspendedstate.md)
```

## Properties<a name="aws-resource-applicationautoscaling-scalabletarget-properties"></a>

`MaxCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-maxcapacity"></a>
The maximum value to scale to in response to a scale\-out event\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-mincapacity"></a>
The minimum value to scale to in response to a scale\-in event\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-applicationautoscaling-scalabletarget-resourceid"></a>
The resource identifier to associate with this scalable target\. This string consists of the resource type and unique identifier\. For valid values, see the `ResourceId` parameter for [RegisterScalableTarget](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) in the *Application Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleARN`  <a name="cfn-applicationautoscaling-scalabletarget-rolearn"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that allows Application Auto Scaling to modify the scalable target on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScalableDimension`  <a name="cfn-applicationautoscaling-scalabletarget-scalabledimension"></a>
The scalable dimension that is associated with the scalable target\. Specify the service namespace, resource type, and scaling property, for example, `ecs:service:DesiredCount` for the desired task count of an Amazon ECS service\. For valid values, see the `ScalableDimension` parameter for [RegisterScalableTarget](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) in the *Application Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScheduledActions`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledactions"></a>
The scheduled actions for the scalable target\. Duplicates aren't allowed\.  
*Required*: No  
*Type*: List of [ScheduledAction](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNamespace`  <a name="cfn-applicationautoscaling-scalabletarget-servicenamespace"></a>
The namespace of the AWS service that provides the resource or `custom-resource` for a resource provided by your own application or service\. For valid values, see the `ServiceNamespace` parameter for [RegisterScalableTarget](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) in the *Application Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SuspendedState`  <a name="cfn-applicationautoscaling-scalabletarget-suspendedstate"></a>
An embedded object that contains attributes and attribute values that are used to suspend and resume automatic scaling\. Setting the value of an attribute to `true` suspends the specified scaling activities\. Setting it to `false` \(default\) resumes the specified scaling activities\.   
**Suspension Outcomes**  
+ For `DynamicScalingInSuspended`, while a suspension is in effect, all scale\-in activities that are triggered by a scaling policy are suspended\.
+ For `DynamicScalingOutSuspended`, while a suspension is in effect, all scale\-out activities that are triggered by a scaling policy are suspended\.
+ For `ScheduledScalingSuspended`, while a suspension is in effect, all scaling activities that involve scheduled actions are suspended\. 
For more information, see [Suspend and Resume Application Auto Scaling](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-suspend-resume-scaling.html) in the *Application Auto Scaling User Guide*\.  
*Required*: No  
*Type*: [SuspendedState](aws-properties-applicationautoscaling-scalabletarget-suspendedstate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-applicationautoscaling-scalabletarget-return-values"></a>

### Ref<a name="aws-resource-applicationautoscaling-scalabletarget-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the AWS CloudFormation\-generated ID of the resource\. For example: `service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH|ecs:service:DesiredCount|ecs`\. 

AWS CloudFormation uses the following format to generate the ID: `service/resource_ID|scalable_dimension|service_namespace `\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-applicationautoscaling-scalabletarget--examples"></a>

Each scalable target has a resource ID, scalable dimension, and namespace, as well as values for minimum and maximum capacity\. For more information, see [RegisterScalableTarget](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) in the *Application Auto Scaling API Reference*\.

### Register a Scalable Target<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Register_a_Scalable_Target"></a>

The following example creates a scalable target for an [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)\. Application Auto Scaling can scale the number of tasks at a minimum of 1 task and a maximum of 2\.

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Register_a_Scalable_Target--json"></a>

```
{
  "scalableTarget":{
    "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
    "Properties":{
      "MaxCapacity":2,
      "MinCapacity":1,
      "ResourceId":"service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH",
      "RoleARN" : {"Fn::GetAtt" : ["ApplicationAutoScalingRole", "Arn"] },
      "ScalableDimension":"ecs:service:DesiredCount",
      "ServiceNamespace":"ecs"
      }
    }
  }
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Register_a_Scalable_Target--yaml"></a>

```
scalableTarget:
  Type: AWS::ApplicationAutoScaling::ScalableTarget
  Properties:
    MaxCapacity: 2
    MinCapacity: 1
    ResourceId: service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH
    RoleARN: !GetAtt [ ApplicationAutoScalingRole, Arn ]
    ScalableDimension: ecs:service:DesiredCount
    ServiceNamespace: ecs
```

### Using Functions to Construct the Resource ID<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Using_Functions_to_Construct_the_Resource_ID"></a>

The following example uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and `Ref` intrinsic functions to construct the `ResourceId` property of the scaling target\. 

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Using_Functions_to_Construct_the_Resource_ID--json"></a>

```
{
  "SpotFleetScalingTarget":{
    "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
    "Properties":{
      "MaxCapacity":2,
      "MinCapacity":1,
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
      "RoleARN":{
        "Fn::GetAtt":[
          "AutoScalingRole",
          "Arn"
        ]
      },
      "ScalableDimension":"ec2:spot-fleet-request:TargetCapacity",
      "ServiceNamespace":"ec2"
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Using_Functions_to_Construct_the_Resource_ID--yaml"></a>

```
SpotFleetScalingTarget:
  Type: AWS::ApplicationAutoScaling::ScalableTarget
  Properties:
    MaxCapacity: 2
    MinCapacity: 1
    ResourceId: !Join 
      - /
      - - spot-fleet-request
        - !Ref ECSSpotFleet
    RoleARN: !GetAtt 
      - AutoScalingRole
      - Arn
    ScalableDimension: 'ec2:spot-fleet-request:TargetCapacity'
    ServiceNamespace: ec2
```

### Application Auto Scaling Scalable Target with an Amazon DynamoDB Table<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Application_Auto_Scaling_Scalable_Target_with_an_Amazon_DynamoDB_Table"></a>

This example registers an [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) as a scalable target\. It also defines a `TargetTrackingScaling` scaling policy that scales the `WriteCapacityUnits` throughput for the table\. 

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Application_Auto_Scaling_Scalable_Target_with_an_Amazon_DynamoDB_Table--json"></a>

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

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Application_Auto_Scaling_Scalable_Target_with_an_Amazon_DynamoDB_Table--yaml"></a>

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

### Scheduled Actions<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Scheduled_Actions"></a>

The following example creates a [ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalabletarget-scheduledaction.html) for a scalable target\. 

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Scheduled_Actions--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Description":"Creating ECS service",
  "Parameters":{
    "AppName":{
      "Type":"String",
      "Description":"Name of app requiring ELB exposure",
      "Default":"simple-app"
    },
    "AppContainerPort":{
      "Type":"Number",
      "Description":"Container port of app requiring ELB exposure",
      "Default":"80"
    },
    "AppHostPort":{
      "Type":"Number",
      "Description":"Host port of app requiring ELB exposure",
      "Default":"80"
    }
  },
  "Resources":{
    "scalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
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
        },
        "ServiceNamespace":"ecs",
        "ScalableDimension":"ecs:service:DesiredCount",
        "RoleARN":{
          "Fn::GetAtt":[
            "scalingRole",
            "Arn"
          ]
        },
        "MaxCapacity":"2",
        "MinCapacity":"1",
        "ScheduledActions":[
          {
            "EndTime":"2018-12-04T22:14:41.951Z",
            "ScalableTargetAction":{
              "MaxCapacity":"2",
              "MinCapacity":"1"
            },
            "ScheduledActionName":"First",
            "StartTime":"2018-11-28T22:14:41.951Z",
            "Schedule":"cron(0 12 ? * MON *)"
          }
        ]
      }
    },
    "scalingRole":{
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
                  "Action":"*",
                  "Resource":"*"
                }
              ]
            }
          }
        ]
      }
    },
    "cluster":{
      "Type":"AWS::ECS::Cluster"
    },
    "taskdefinition":{
      "Type":"AWS::ECS::TaskDefinition",
      "Properties":{
        "ContainerDefinitions":[
          {
            "Name":{
              "Ref":"AppName"
            },
            "MountPoints":[
              {
                "SourceVolume":"my-vol",
                "ContainerPath":"/var/www/my-vol"
              }
            ],
            "Image":"amazon/amazon-ecs-sample",
            "Cpu":"10",
            "PortMappings":[
              {
                "ContainerPort":{
                  "Ref":"AppContainerPort"
                },
                "HostPort":{
                  "Ref":"AppHostPort"
                }
              }
            ],
            "EntryPoint":[
              "/usr/sbin/apache2",
              "-D",
              "FOREGROUND"
            ],
            "Memory":"500",
            "Essential":"true"
          },
          {
            "Name":"busybox",
            "Image":"busybox",
            "Cpu":"10",
            "EntryPoint":[
              "sh",
              "-c"
            ],
            "Memory":"500",
            "Command":[
              "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
            ],
            "Essential":"false",
            "VolumesFrom":[
              {
                "SourceContainer":{
                  "Ref":"AppName"
                }
              }
            ]
          }
        ],
        "Volumes":[
          {
            "Host":{
              "SourcePath":"/var/lib/docker/vfs/dir/"
            },
            "Name":"my-vol"
          }
        ]
      }
    },
    "service":{
      "Type":"AWS::ECS::Service",
      "Properties":{
        "Cluster":{
          "Ref":"cluster"
        },
        "DesiredCount":0,
        "TaskDefinition":{
          "Ref":"taskdefinition"
        }
      }
    }
  },
  "Outputs":{
    "resourceId":{
      "Description":"ResourceId",
      "Value":{
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
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget--examples--Scheduled_Actions--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Creating ECS service
Parameters:
  AppName:
    Type: String
    Description: Name of app requiring ELB exposure
    Default: simple-app
  AppContainerPort:
    Type: Number
    Description: Container port of app requiring ELB exposure
    Default: '80'
  AppHostPort:
    Type: Number
    Description: Host port of app requiring ELB exposure
    Default: '80'
Resources:
  scalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      ResourceId: !Join 
        - /
        - - service
          - !Ref cluster
          - !GetAtt service.Name
      ServiceNamespace: ecs
      ScalableDimension: 'ecs:service:DesiredCount'
      RoleARN: !GetAtt 
        - scalingRole
        - Arn
      MaxCapacity: '2'
      MinCapacity: '1'
      ScheduledActions:
        - EndTime: '2018-12-04T22:14:41.951Z'
          ScalableTargetAction:
            MaxCapacity: '2'
            MinCapacity: '1'
          ScheduledActionName: First
          StartTime: '2018-11-28T22:14:41.951Z'
          Schedule: 'cron(0 12 ? * MON *)'
  scalingRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - application-autoscaling.amazonaws.com
            Action:
              - 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: root
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action: '*'
                Resource: '*'
  cluster:
    Type: AWS::ECS::Cluster
  taskdefinition:
    Type: AWS::ECS::TaskDefinition
    Properties:
      ContainerDefinitions:
        - Name: !Ref AppName
          MountPoints:
            - SourceVolume: my-vol
              ContainerPath: /var/www/my-vol
          Image: amazon/amazon-ecs-sample
          Cpu: '10'
          PortMappings:
            - ContainerPort: !Ref AppContainerPort
              HostPort: !Ref AppHostPort
          EntryPoint:
            - /usr/sbin/apache2
            - '-D'
            - FOREGROUND
          Memory: '500'
          Essential: 'true'
        - Name: busybox
          Image: busybox
          Cpu: '10'
          EntryPoint:
            - sh
            - '-c'
          Memory: '500'
          Command:
            - >-
              /bin/sh -c "while true; do /bin/date > /var/www/my-vol/date; sleep
              1; done"
          Essential: 'false'
          VolumesFrom:
            - SourceContainer: !Ref AppName
      Volumes:
        - Host:
            SourcePath: /var/lib/docker/vfs/dir/
          Name: my-vol
  service:
    Type: AWS::ECS::Service
    Properties:
      Cluster: !Ref cluster
      DesiredCount: 0
      TaskDefinition: !Ref taskdefinition
Outputs:
  resourceId:
    Description: ResourceId
    Value: !Join 
      - /
      - - service
        - !Ref cluster
        - !GetAtt service.Name
```

## See Also<a name="aws-resource-applicationautoscaling-scalabletarget--seealso"></a>
+ [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html) 