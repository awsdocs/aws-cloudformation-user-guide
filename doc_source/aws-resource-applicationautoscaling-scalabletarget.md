# AWS::ApplicationAutoScaling::ScalableTarget<a name="aws-resource-applicationautoscaling-scalabletarget"></a>

The `AWS::ApplicationAutoScaling::ScalableTarget` resource specifies a resource that Application Auto Scaling can scale up or down\. For more information, see the [RegisterScalableTarget](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) action in the *Application Auto Scaling API Reference*\.

Updates to `AWS::DynamoDB::Table` resources that are associated with `AWS::ApplicationAutoScaling::ScalableTarget` resources will always result in an update failure and then an update rollback failure\. The following `ScalableDimension` attributes cause this problem when associated with the table:
+ dynamodb:table:ReadCapacityUnits
+ dynamodb:table:WriteCapacityUnits
+ dynamodb:index:ReadCapacityUnits
+ dynamodb:index:WriteCapacityUnits

As a workaround, please deregister scalable targets before performing updates to `AWS::DynamoDB::Table` resources\.

**Topics**
+ [Syntax](#w3ab2c21c10c97c13)
+ [Properties](#w3ab2c21c10c97c15)
+ [Return Value](#aws-resource-applicationautoscaling-scalabletarget-returnvalues)
+ [Examples](#aws-resource-applicationautoscaling-scalabletarget-examples)

## Syntax<a name="w3ab2c21c10c97c13"></a>

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
    "[ScheduledActions](#cfn-applicationautoscaling-scalabletarget-scheduledactions)" : [ [*ScheduledAction*](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md), ... ],
    "[ServiceNamespace](#cfn-applicationautoscaling-scalabletarget-servicenamespace)" : String
  }
}
```

### YAML<a name="aws-resource-applicationautoscaling-scalabletarget-syntax.yaml"></a>

```
Type: "AWS::ApplicationAutoScaling::ScalableTarget"
Properties:
  [MaxCapacity](#cfn-applicationautoscaling-scalabletarget-maxcapacity): Integer
  [MinCapacity](#cfn-applicationautoscaling-scalabletarget-mincapacity): Integer
  [ResourceId](#cfn-applicationautoscaling-scalabletarget-resourceid): String
  [RoleARN](#cfn-applicationautoscaling-scalabletarget-rolearn): String
  [ScalableDimension](#cfn-applicationautoscaling-scalabletarget-scalabledimension): String
  [ScheduledActions](#cfn-applicationautoscaling-scalabletarget-scheduledactions): 
    - [*ScheduledAction*](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md)
  [ServiceNamespace](#cfn-applicationautoscaling-scalabletarget-servicenamespace): String
```

## Properties<a name="w3ab2c21c10c97c15"></a>

`MaxCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-maxcapacity"></a>
The maximum value that Application Auto Scaling can use to scale a target during a scaling activity\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MinCapacity`  <a name="cfn-applicationautoscaling-scalabletarget-mincapacity"></a>
The minimum value that Application Auto Scaling can use to scale a target during a scaling activity\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceId`  <a name="cfn-applicationautoscaling-scalabletarget-resourceid"></a>
The resource identifier to associate with this scalable target\. This string consists of the resource type and unique identifier\. For more information, see the `ResourceId` parameter for the [RegisterScalableTarget](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html) action in the *Application Auto Scaling API Reference*, or see the [`ScalableTarget` examples](#aws-resource-applicationautoscaling-scalabletarget-examples)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoleARN`  <a name="cfn-applicationautoscaling-scalabletarget-rolearn"></a>
The Amazon Resource Name \(ARN\) of an AWS Identity and Access Management \(IAM\) role that allows Application Auto Scaling to modify your scalable target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ScalableDimension`  <a name="cfn-applicationautoscaling-scalabletarget-scalabledimension"></a>
The scalable dimension that's associated with the scalable target\. Specify the service namespace, resource type, and scaling property—for example, `ecs:service:DesiredCount` for the desired task count of an Amazon Elastic Container Service service\. For valid values, see the `ScalableDimension` content for the [ScalingPolicy](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_ScalingPolicy.html) data type in the *Application Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ScheduledActions`  <a name="cfn-applicationautoscaling-scalabletarget-scheduledactions"></a>
The scheduled actions for the scalable target\. Duplicates aren't allowed\.  
 *Required*: No  
 *Type*: List of [Application Auto Scaling ScalableTarget ScheduledAction](aws-properties-applicationautoscaling-scalabletarget-scheduledaction.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceNamespace`  <a name="cfn-applicationautoscaling-scalabletarget-servicenamespace"></a>
The AWS service namespace of the scalable target\. For a list of service namespaces, see [AWS Service Namespaces](http://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-applicationautoscaling-scalabletarget-returnvalues"></a>

### Ref<a name="w3ab2c21c10c97c17b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the AWS CloudFormation\-generated ID of the resource, such as `service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH|ecs:service:DesiredCount|ecs`\.

AWS CloudFormation uses the following format to generate the ID: `service/[resource\_ID](#cfn-applicationautoscaling-scalabletarget-resourceid)|scalable_dimension|service_namespace`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-applicationautoscaling-scalabletarget-examples"></a>

### Number of Tasks<a name="w3ab2c21c10c97c19b2"></a>

The following example creates a scalable target for an Amazon Elastic Container Service service\. Application Auto Scaling scales the number of tasks at a minimum of 1 task and a maximum of 2\.

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget-example.json"></a>

```
"scalableTarget" : {
  "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
  "Properties" : {
    "MaxCapacity" : 2,
    "MinCapacity" : 1,
    "ResourceId" : "service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH",
    "RoleARN" : {"Fn::GetAtt" : ["ApplicationAutoScalingRole", "Arn"] },
    "ScalableDimension" : "ecs:service:DesiredCount",
    "ServiceNamespace" : "ecs"
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget-example.yaml"></a>

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

### Using `Fn::Join` and `Ref` to Construct the `ResourceId`<a name="w3ab2c21c10c97c19b4"></a>

The following example uses the `Fn::Join` and `Ref` intrinsic functions to construct the `ResourceId` property of the scaling target\.

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget-example2.json"></a>

```
"SpotFleetScalingTarget": {
  "Type": "AWS::ApplicationAutoScaling::ScalableTarget",
  "Properties": {
    "MaxCapacity": 2,
    "MinCapacity": 1,
    "ResourceId": {
      "Fn::Join": [
        "/",
        [
          "spot-fleet-request",
          {
            "Ref": "ECSSpotFleet"
          }
        ]
      ]
    },
    "RoleARN": {
      "Fn::GetAtt": [
        "AutoScalingRole",
        "Arn"
      ]
    },
    "ScalableDimension": "ec2:spot-fleet-request:TargetCapacity",
    "ServiceNamespace": "ec2"
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget-example2.yaml"></a>

```
SpotFleetScalingTarget:
  Type: 'AWS::ApplicationAutoScaling::ScalableTarget'
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

### Application Auto Scaling Scalable Target with an Amazon DynamoDB Table<a name="aws-resource-applicationautoscaling-scalabletarget-ddb-example"></a>

This example sets up Application Auto Scaling for an `AWS::DynamoDB::Table` resource\. The template defines a `TargetTrackingScaling` scaling policy that scales up the `WriteCapacityUnits` throughput for the table\.

#### JSON<a name="aws-resource-applicationautoscaling-scalabletarget-ddb-example.json"></a>

```
{
  "Resources": {
    "DDBTable": {
      "Type": "AWS::DynamoDB::Table",
      "Properties": {
        "AttributeDefinitions": [
          {
            "AttributeName": "ArtistId",
            "AttributeType": "S"
          },
          {
            "AttributeName": "Concert",
            "AttributeType": "S"
          },
          {
            "AttributeName": "TicketSales",
            "AttributeType": "S"
          }
        ],
        "KeySchema": [
          {
            "AttributeName": "ArtistId",
            "KeyType": "HASH"
          },
          {
            "AttributeName": "Concert",
            "KeyType": "RANGE"
          }
        ],
        "GlobalSecondaryIndexes": [
          {
            "IndexName": "GSI",
            "KeySchema": [
              {
                "AttributeName": "TicketSales",
                "KeyType": "HASH"
              }
            ],
            "Projection": {
              "ProjectionType": "KEYS_ONLY"
            },
            "ProvisionedThroughput": {
              "ReadCapacityUnits": 5,
              "WriteCapacityUnits": 5
            }
          }
        ],
        "ProvisionedThroughput": {
          "ReadCapacityUnits": 5,
          "WriteCapacityUnits": 5
        }
      }
    },
    "WriteCapacityScalableTarget": {
      "Type": "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties": {
        "MaxCapacity": 15,
        "MinCapacity": 5,
        "ResourceId": { "Fn::Join": [
          "/",
          [
            "table",
            { "Ref": "DDBTable" }
          ]
        ] },
        "RoleARN": {
          "Fn::GetAtt": ["ScalingRole", "Arn"]
        },
        "ScalableDimension": "dynamodb:table:WriteCapacityUnits",
        "ServiceNamespace": "dynamodb"
      }
    },
    "ScalingRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "application-autoscaling.amazonaws.com"
                ]
              },
              "Action": [
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Path": "/",
        "Policies": [
          {
            "PolicyName": "root",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "dynamodb:DescribeTable",
                    "dynamodb:UpdateTable",
                    "cloudwatch:PutMetricAlarm",
                    "cloudwatch:DescribeAlarms",
                    "cloudwatch:GetMetricStatistics",
                    "cloudwatch:SetAlarmState",
                    "cloudwatch:DeleteAlarms"
                  ],
                  "Resource": "*"
                }
              ]
            }
          }
        ]
      }
    },
    "WriteScalingPolicy": {
      "Type": "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties": {
        "PolicyName": "WriteAutoScalingPolicy",
        "PolicyType": "TargetTrackingScaling",
        "ScalingTargetId": {
          "Ref": "WriteCapacityScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration": {
          "TargetValue": 50.0,
          "ScaleInCooldown": 60,
          "ScaleOutCooldown": 60,
          "PredefinedMetricSpecification": {
            "PredefinedMetricType": "DynamoDBWriteCapacityUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalabletarget-ddb-example.yaml"></a>

```
Resources:
  DDBTable:
    Type: "AWS::DynamoDB::Table"
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
    Type: "AWS::ApplicationAutoScaling::ScalableTarget"
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
    Type: "AWS::IAM::Role"
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
    Type: "AWS::ApplicationAutoScaling::ScalingPolicy"
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

### Scheduled Actions<a name="aws-resource-applicationautoscaling-scalabletarget-scheduledactions-example"></a>

The following example creates a scheduled action for a target\.

#### JSON<a name=".json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Description" : "Creating ECS service",
  "Parameters": {
    "AppName": {
      "Type":"String",
      "Description": "Name of app requiring ELB exposure",
      "Default": "simple-app"
    },
    "AppContainerPort": {
      "Type":"Number",
      "Description": "Container port of app requiring ELB exposure",
      "Default": "80"
    },
    "AppHostPort": {
      "Type":"Number",
      "Description": "Host port of app requiring ELB exposure",
      "Default": "80"
    }
  },
  "Resources": {
    "scalableTarget": {
      "Type": "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties": {
        "ResourceId": {
          "Fn::Join": [
            "/",
            [
              "service",
              {
                "Ref": "cluster"
              },
              {
                "Fn::GetAtt": [
                  "service",
                  "Name"
                ]
              }
            ]
          ]
        },
        "ServiceNamespace": "ecs",
        "ScalableDimension": "ecs:service:DesiredCount",
        "RoleARN": {
          "Fn::GetAtt": [
            "scalingRole",
            "Arn"
          ]
        },
        "MaxCapacity": "2",
        "MinCapacity": "1",
        "ScheduledActions": [{
          "EndTime": "2018-12-04T22:14:41.951Z",
          "ScalableTargetAction": {
            "MaxCapacity": "2",
            "MinCapacity": "1"
          },
          "ScheduledActionName": "First",
          "StartTime": "2018-11-28T22:14:41.951Z",
          "Schedule": "cron(0 0 12 ? * MON *)"
          }
        ]
      }
    },
    "scalingRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": ["application-autoscaling.amazonaws.com"]
              },
              "Action": [
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Path": "/",
        "Policies": [
          {
            "PolicyName": "root",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": "*",
                  "Resource": "*"
                }
              ]
            }
          }
        ]
      }
    },
    "cluster": {
      "Type": "AWS::ECS::Cluster"
    },
    "taskdefinition": {
      "Type": "AWS::ECS::TaskDefinition",
      "Properties": {
        "ContainerDefinitions": [
          {
            "Name": {
              "Ref": "AppName"
            },
            "MountPoints": [
              {
                "SourceVolume": "my-vol",
                "ContainerPath": "/var/www/my-vol"
              }
            ],
            "Image": "amazon/amazon-ecs-sample",
            "Cpu": "10",
            "PortMappings": [
              {
                "ContainerPort": {
                  "Ref": "AppContainerPort"
                },
                "HostPort": {
                  "Ref": "AppHostPort"
                }
              }
            ],
            "EntryPoint": [
              "/usr/sbin/apache2",
              "-D",
              "FOREGROUND"
            ],
            "Memory": "500",
            "Essential": "true"
          },
          {
            "Name": "busybox",
            "Image": "busybox",
            "Cpu": "10",
            "EntryPoint": [
              "sh",
              "-c"
            ],
            "Memory": "500",
            "Command": [
              "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
            ],
            "Essential": "false",
            "VolumesFrom": [
              {
                "SourceContainer": {
                  "Ref": "AppName"
                }
              }
            ]
          }
        ],
        "Volumes": [
          {
            "Host": {
              "SourcePath": "/var/lib/docker/vfs/dir/"
            },
            "Name": "my-vol"
          }
        ]
      }
    },
    "service": {
      "Type": "AWS::ECS::Service",
      "Properties": {
        "Cluster": {
          "Ref": "cluster"
        },
        "DesiredCount": 0,
        "TaskDefinition": {
          "Ref": "taskdefinition"
        }
      }
    }
  },
  "Outputs" : {
    "resourceId" : {
      "Description" : "ResourceId",
      "Value" : {"Fn::Join" : [ "/" , ["service", {"Ref" : "cluster"}, {"Fn::GetAtt" : ["service", "Name"]}]]}
    }
  }
}
```

#### YAML<a name=".yaml"></a>

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
    Type: 'AWS::ApplicationAutoScaling::ScalableTarget'
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
          Schedule: cron(0 0 12 ? * MON *)
  scalingRole:
    Type: 'AWS::IAM::Role'
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
    Type: 'AWS::ECS::Cluster'
  taskdefinition:
    Type: 'AWS::ECS::TaskDefinition'
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
    Type: 'AWS::ECS::Service'
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