# AWS::SageMaker::MonitoringSchedule<a name="aws-resource-sagemaker-monitoringschedule"></a>

The `AWS::SageMaker::MonitoringSchedule` resource is an Amazon SageMaker resource type that regularly starts SageMaker processing Jobs to monitor the data captured for a SageMaker endpoint\.

## Syntax<a name="aws-resource-sagemaker-monitoringschedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-monitoringschedule-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::MonitoringSchedule",
  "Properties" : {
      "[EndpointName](#cfn-sagemaker-monitoringschedule-endpointname)" : String,
      "[FailureReason](#cfn-sagemaker-monitoringschedule-failurereason)" : String,
      "[LastMonitoringExecutionSummary](#cfn-sagemaker-monitoringschedule-lastmonitoringexecutionsummary)" : MonitoringExecutionSummary,
      "[MonitoringScheduleConfig](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig)" : MonitoringScheduleConfig,
      "[MonitoringScheduleName](#cfn-sagemaker-monitoringschedule-monitoringschedulename)" : String,
      "[MonitoringScheduleStatus](#cfn-sagemaker-monitoringschedule-monitoringschedulestatus)" : String,
      "[Tags](#cfn-sagemaker-monitoringschedule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-monitoringschedule-syntax.yaml"></a>

```
Type: AWS::SageMaker::MonitoringSchedule
Properties: 
  [EndpointName](#cfn-sagemaker-monitoringschedule-endpointname): String
  [FailureReason](#cfn-sagemaker-monitoringschedule-failurereason): String
  [LastMonitoringExecutionSummary](#cfn-sagemaker-monitoringschedule-lastmonitoringexecutionsummary): 
    MonitoringExecutionSummary
  [MonitoringScheduleConfig](#cfn-sagemaker-monitoringschedule-monitoringscheduleconfig): 
    MonitoringScheduleConfig
  [MonitoringScheduleName](#cfn-sagemaker-monitoringschedule-monitoringschedulename): String
  [MonitoringScheduleStatus](#cfn-sagemaker-monitoringschedule-monitoringschedulestatus): String
  [Tags](#cfn-sagemaker-monitoringschedule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-monitoringschedule-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-monitoringschedule-endpointname"></a>
The name of the endpoint using the monitoring schedule\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureReason`  <a name="cfn-sagemaker-monitoringschedule-failurereason"></a>
Contains the reason a monitoring job failed, if it failed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastMonitoringExecutionSummary`  <a name="cfn-sagemaker-monitoringschedule-lastmonitoringexecutionsummary"></a>
Describes metadata on the last execution to run, if there was one\.  
*Required*: No  
*Type*: [MonitoringExecutionSummary](aws-properties-sagemaker-monitoringschedule-monitoringexecutionsummary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringScheduleConfig`  <a name="cfn-sagemaker-monitoringschedule-monitoringscheduleconfig"></a>
The configuration object that specifies the monitoring schedule and defines the monitoring job\.  
*Required*: Yes  
*Type*: [MonitoringScheduleConfig](aws-properties-sagemaker-monitoringschedule-monitoringscheduleconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitoringScheduleName`  <a name="cfn-sagemaker-monitoringschedule-monitoringschedulename"></a>
The name of the monitoring schedule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitoringScheduleStatus`  <a name="cfn-sagemaker-monitoringschedule-monitoringschedulestatus"></a>
The status of the monitoring schedule\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Failed | Pending | Scheduled | Stopped`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-monitoringschedule-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-monitoringschedule-return-values"></a>

### Ref<a name="aws-resource-sagemaker-monitoringschedule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the monitoring schedule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-monitoringschedule-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-monitoringschedule-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time when the monitoring schedule was created\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
The last time that the monitoring schedule was modified\.

`MonitoringScheduleArn`  <a name="MonitoringScheduleArn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-sagemaker-monitoringschedule--examples"></a>

### SageMaker MonitoringSchedule Example<a name="aws-resource-sagemaker-monitoringschedule--examples--SageMaker_MonitoringSchedule_Example"></a>

The following example creates a monitoring schedule for a SageMaker endpoint\.

#### JSON<a name="aws-resource-sagemaker-monitoringschedule--examples--SageMaker_MonitoringSchedule_Example--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Basic SageMaker Hosting entities to create a monitoring schedule",
   "Mappings": {
      "RegionMap": {
         "us-west-2": {
            "NullTransformer": "123456789012.dkr.ecr.us-west-2.amazonaws.com/mymodel:latest"
         },
         "us-east-2": {
            "NullTransformer": "123456789012.dkr.ecr.us-east-2.amazonaws.com/mymodel:latest"
         },
         "us-east-1": {
            "NullTransformer": "123456789012.dkr.ecr.us-east-1.amazonaws.com/mymodel:latest"
         },
         "eu-west-1": {
            "NullTransformer": "123456789012.dkr.ecr.eu-west-1.amazonaws.com/mymodel:latest"
         },
         "ap-northeast-1": {
            "NullTransformer": "123456789012.dkr.ecr.ap-northeast-1.amazonaws.com/mymodel:latest"
         },
         "ap-northeast-2": {
            "NullTransformer": "123456789012.dkr.ecr.ap-northeast-2.amazonaws.com/mymodel:latest"
         },
         "ap-southeast-2": {
            "NullTransformer": "123456789012.dkr.ecr.ap-southeast-2.amazonaws.com/mymodel:latest"
         },
         "eu-central-1": {
            "NullTransformer": "123456789012.dkr.ecr.eu-central-1.amazonaws.com/mymodel:latest"
         }
      }
   },
   "Resources": {
      "Endpoint": {
         "Type": "AWS::SageMaker::Endpoint",
         "Properties": {
            "EndpointConfigName": null
         }
      },
      "EndpointConfig": {
         "Type": "AWS::SageMaker::EndpointConfig",
         "Properties": {
            "ProductionVariants": [
               {
                  "InitialInstanceCount": 1,
                  "InitialVariantWeight": 1,
                  "InstanceType": "ml.t2.large",
                  "ModelName": null,
                  "VariantName": null
               }
            ]
         }
      },
      "Model": {
         "Type": "AWS::SageMaker::Model",
         "Properties": {
            "PrimaryContainer": {
               "Image": null
            },
            "ExecutionRoleArn": null
         }
      },
      "ExecutionRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version": "2012-10-17",
               "Statement": [
                  {
                     "Effect": "Allow",
                     "Principal": {
                        "Service": [
                           "sagemaker.amazonaws.com"
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
                           "Action": "*",
                           "Resource": "*"
                        }
                     ]
                  }
               }
            ]
         }
      },
      "MonitoringScheduleExecutionRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
            "AssumeRolePolicyDocument": {
               "Version": "2012-10-17",
               "Statement": [
                  {
                     "Effect": "Allow",
                     "Principal": {
                        "Service": [
                           "sagemaker.amazonaws.com"
                        ]
                     },
                     "Action": [
                        "sts:AssumeRole"
                     ]
                  }
               ]
            },
            "ManagedPolicyArns": [
               {
                  "Fn::Sub": "arn:${AWS::Partition}:iam::aws:policy/AmazonSageMakerFullAccess"
               },
               {
                  "Fn::Sub": "arn:${AWS::Partition}:iam::aws:policy/AmazonS3FullAccess"
               },
               {
                  "Fn::Sub": "arn:${AWS::Partition}:iam::aws:policy/AmazonEC2ContainerRegistryReadOnly"
               }
            ]
         }
      },
      "MonitoringSchedule": {
         "Type": "AWS::SageMaker::MonitoringSchedule",
         "Properties": {
            "MonitoringScheduleConfig": {
               "MonitoringJobDefinition": {
                  "MonitoringAppSpecification": {
                     "ImageUri": {
                        "Fn::Sub": "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-model-monitor-analyzer:latest"
                     }
                  },
                  "MonitoringInputs": [
                     {
                        "EndpointInput": {
                           "EndpointName": {
                              "Fn::ImportValue": "CanaryEndpointName"
                           },
                           "LocalPath": "/opt/ml/processing/endpointdata"
                        }
                     }
                  ],
                  "MonitoringOutputConfig": {
                     "MonitoringOutputs": [
                        {
                           "S3Output": {
                              "LocalPath": "/opt/ml/processing/localpath",
                              "S3Uri": "s3://endpoint-data-capture/myEndpoint"
                           }
                        }
                     ]
                  },
                  "MonitoringResources": {
                     "ClusterConfig": {
                        "InstanceCount": 1,
                        "InstanceType": "ml.m5.large",
                        "VolumeSizeInGB": 50
                     }
                  },
                  "RoleArn": null
               },
               "ScheduleConfig": {
                  "ScheduleExpression": "cron(0 * ? * * *)"
               }
            },
            "MonitoringScheduleName": "BasicMonitoringSchedule"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-sagemaker-monitoringschedule--examples--SageMaker_MonitoringSchedule_Example--yaml"></a>

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: Basic SageMaker Hosting entities to create a monitoring schedule
 
Description: "Basic Hosting entities test.  We need models to create endpoint configs."
Mappings: 
  RegionMap: 
    "us-west-2":
      "NullTransformer": "123456789012.dkr.ecr.us-west-2.amazonaws.com/mymodel:latest"
    "us-east-2":
      "NullTransformer": "123456789012.dkr.ecr.us-east-2.amazonaws.com/mymodel:latest"
    "us-east-1":
      "NullTransformer": "123456789012.dkr.ecr.us-east-1.amazonaws.com/mymodel:latest"
    "eu-west-1":
      "NullTransformer": "123456789012.dkr.ecr.eu-west-1.amazonaws.com/mymodel:latest"
    "ap-northeast-1":
      "NullTransformer": "123456789012.dkr.ecr.ap-northeast-1.amazonaws.com/mymodel:latest"
    "ap-northeast-2":
      "NullTransformer": "123456789012.dkr.ecr.ap-northeast-2.amazonaws.com/mymodel:latest"
    "ap-southeast-2":
      "NullTransformer": "123456789012.dkr.ecr.ap-southeast-2.amazonaws.com/mymodel:latest"
    "eu-central-1":
      "NullTransformer": "123456789012.dkr.ecr.eu-central-1.amazonaws.com/mymodel:latest"
Resources:
  Endpoint:
    Type: "AWS::SageMaker::Endpoint"
    Properties:
      EndpointConfigName:
        !GetAtt EndpointConfig.EndpointConfigName
  EndpointConfig:
    Type: "AWS::SageMaker::EndpointConfig"
    Properties:
      ProductionVariants:
        - InitialInstanceCount: 1
          InitialVariantWeight: 1.0
          InstanceType: ml.t2.large
          ModelName: !GetAtt Model.ModelName
          VariantName: !GetAtt Model.ModelName
  Model:
    Type: "AWS::SageMaker::Model"
    Properties:
      PrimaryContainer:
        Image: !FindInMap [RegionMap, !Ref "AWS::Region", "NullTransformer"]
      ExecutionRoleArn: !GetAtt ExecutionRole.Arn
 
  ExecutionRole: 
    Type: "AWS::IAM::Role"
    Properties: 
      AssumeRolePolicyDocument: 
        Version: "2012-10-17"
        Statement: 
          - 
            Effect: "Allow"
            Principal: 
              Service: 
                - "sagemaker.amazonaws.com"
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
                Action: "*"
                Resource: "*"
 
  MonitoringScheduleExecutionRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Principal:
              Service:
                - "sagemaker.amazonaws.com"
            Action:
              - "sts:AssumeRole"
      ManagedPolicyArns:
        - Fn::Sub: "arn:${AWS::Partition}:iam::aws:policy/AmazonSageMakerFullAccess"
        - Fn::Sub: "arn:${AWS::Partition}:iam::aws:policy/AmazonS3FullAccess"
        - Fn::Sub: "arn:${AWS::Partition}:iam::aws:policy/AmazonEC2ContainerRegistryReadOnly"
 
  MonitoringSchedule:
    Type: AWS::SageMaker::MonitoringSchedule
    Properties:
      MonitoringScheduleConfig:
        MonitoringJobDefinition:
          MonitoringAppSpecification:
            ImageUri: 
              Fn::Sub: "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-model-monitor-analyzer:latest"
          MonitoringInputs:
            - EndpointInput:
                EndpointName:
                  Fn::ImportValue: CanaryEndpointName
                LocalPath: "/opt/ml/processing/endpointdata"
          MonitoringOutputConfig:
            MonitoringOutputs:
              - S3Output:
                  LocalPath: "/opt/ml/processing/localpath"
                  S3Uri: s3://endpoint-data-capture/myEndpoint
          MonitoringResources:
            ClusterConfig:
              InstanceCount: 1
              InstanceType: ml.m5.large
              VolumeSizeInGB: 50
          RoleArn: !GetAtt MonitoringScheduleExecutionRole.Arn
        ScheduleConfig:
          ScheduleExpression: cron(0 * ? * * *)
      MonitoringScheduleName: BasicMonitoringSchedule
```