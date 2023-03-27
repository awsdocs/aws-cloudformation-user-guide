# AWS::SageMaker::ModelQualityJobDefinition<a name="aws-resource-sagemaker-modelqualityjobdefinition"></a>

Creates a definition for a job that monitors model quality and drift\. For information about model monitor, see [Amazon SageMaker Model Monitor](https://docs.aws.amazon.com/sagemaker/latest/dg/model-monitor.html)\.

## Syntax<a name="aws-resource-sagemaker-modelqualityjobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-modelqualityjobdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::ModelQualityJobDefinition",
  "Properties" : {
      "[EndpointName](#cfn-sagemaker-modelqualityjobdefinition-endpointname)" : String,
      "[JobDefinitionName](#cfn-sagemaker-modelqualityjobdefinition-jobdefinitionname)" : String,
      "[JobResources](#cfn-sagemaker-modelqualityjobdefinition-jobresources)" : MonitoringResources,
      "[ModelQualityAppSpecification](#cfn-sagemaker-modelqualityjobdefinition-modelqualityappspecification)" : ModelQualityAppSpecification,
      "[ModelQualityBaselineConfig](#cfn-sagemaker-modelqualityjobdefinition-modelqualitybaselineconfig)" : ModelQualityBaselineConfig,
      "[ModelQualityJobInput](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput)" : ModelQualityJobInput,
      "[ModelQualityJobOutputConfig](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjoboutputconfig)" : MonitoringOutputConfig,
      "[NetworkConfig](#cfn-sagemaker-modelqualityjobdefinition-networkconfig)" : NetworkConfig,
      "[RoleArn](#cfn-sagemaker-modelqualityjobdefinition-rolearn)" : String,
      "[StoppingCondition](#cfn-sagemaker-modelqualityjobdefinition-stoppingcondition)" : StoppingCondition,
      "[Tags](#cfn-sagemaker-modelqualityjobdefinition-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-modelqualityjobdefinition-syntax.yaml"></a>

```
Type: AWS::SageMaker::ModelQualityJobDefinition
Properties: 
  [EndpointName](#cfn-sagemaker-modelqualityjobdefinition-endpointname): String
  [JobDefinitionName](#cfn-sagemaker-modelqualityjobdefinition-jobdefinitionname): String
  [JobResources](#cfn-sagemaker-modelqualityjobdefinition-jobresources): 
    MonitoringResources
  [ModelQualityAppSpecification](#cfn-sagemaker-modelqualityjobdefinition-modelqualityappspecification): 
    ModelQualityAppSpecification
  [ModelQualityBaselineConfig](#cfn-sagemaker-modelqualityjobdefinition-modelqualitybaselineconfig): 
    ModelQualityBaselineConfig
  [ModelQualityJobInput](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput): 
    ModelQualityJobInput
  [ModelQualityJobOutputConfig](#cfn-sagemaker-modelqualityjobdefinition-modelqualityjoboutputconfig): 
    MonitoringOutputConfig
  [NetworkConfig](#cfn-sagemaker-modelqualityjobdefinition-networkconfig): 
    NetworkConfig
  [RoleArn](#cfn-sagemaker-modelqualityjobdefinition-rolearn): String
  [StoppingCondition](#cfn-sagemaker-modelqualityjobdefinition-stoppingcondition): 
    StoppingCondition
  [Tags](#cfn-sagemaker-modelqualityjobdefinition-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-modelqualityjobdefinition-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-modelqualityjobdefinition-endpointname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobDefinitionName`  <a name="cfn-sagemaker-modelqualityjobdefinition-jobdefinitionname"></a>
The name of the monitoring job definition\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobResources`  <a name="cfn-sagemaker-modelqualityjobdefinition-jobresources"></a>
Identifies the resources to deploy for a monitoring job\.  
*Required*: Yes  
*Type*: [MonitoringResources](aws-properties-sagemaker-modelqualityjobdefinition-monitoringresources.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelQualityAppSpecification`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualityappspecification"></a>
Container image configuration object for the monitoring job\.  
*Required*: Yes  
*Type*: [ModelQualityAppSpecification](aws-properties-sagemaker-modelqualityjobdefinition-modelqualityappspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelQualityBaselineConfig`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualitybaselineconfig"></a>
Specifies the constraints and baselines for the monitoring job\.  
*Required*: No  
*Type*: [ModelQualityBaselineConfig](aws-properties-sagemaker-modelqualityjobdefinition-modelqualitybaselineconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelQualityJobInput`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualityjobinput"></a>
A list of the inputs that are monitored\. Currently endpoints are supported\.  
*Required*: Yes  
*Type*: [ModelQualityJobInput](aws-properties-sagemaker-modelqualityjobdefinition-modelqualityjobinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelQualityJobOutputConfig`  <a name="cfn-sagemaker-modelqualityjobdefinition-modelqualityjoboutputconfig"></a>
The output configuration for monitoring jobs\.  
*Required*: Yes  
*Type*: [MonitoringOutputConfig](aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfig`  <a name="cfn-sagemaker-modelqualityjobdefinition-networkconfig"></a>
Specifies the network configuration for the monitoring job\.  
*Required*: No  
*Type*: [NetworkConfig](aws-properties-sagemaker-modelqualityjobdefinition-networkconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-sagemaker-modelqualityjobdefinition-rolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that Amazon SageMaker can assume to perform tasks on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StoppingCondition`  <a name="cfn-sagemaker-modelqualityjobdefinition-stoppingcondition"></a>
A time limit for how long the monitoring job is allowed to run before stopping\.  
*Required*: No  
*Type*: [StoppingCondition](aws-properties-sagemaker-modelqualityjobdefinition-stoppingcondition.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-modelqualityjobdefinition-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-modelqualityjobdefinition-return-values"></a>

### Ref<a name="aws-resource-sagemaker-modelqualityjobdefinition-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-modelqualityjobdefinition-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-modelqualityjobdefinition-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time when the job definition was created\.

`JobDefinitionArn`  <a name="JobDefinitionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the job definition\.

## Examples<a name="aws-resource-sagemaker-modelqualityjobdefinition--examples"></a>

### SageMaker ModelQualityJobDefinition Example<a name="aws-resource-sagemaker-modelqualityjobdefinition--examples--SageMaker_ModelQualityJobDefinition_Example"></a>

The following example creates a Model Quality monitoring job defintion\.

#### JSON<a name="aws-resource-sagemaker-modelqualityjobdefinition--examples--SageMaker_ModelQualityJobDefinition_Example--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Basic SageMaker Hosting entities to create a model quality job definition",
   "Mappings": {
      "RegionMap": {
         "us-west-2": {
            "MyModelImage": "123456789012.dkr.ecr.us-west-2.amazonaws.com/mymodel:latest"
         },
         "us-east-2": {
            "MyModelImage": "123456789012.dkr.ecr.us-east-2.amazonaws.com/mymodel:latest"
         },
         "us-east-1": {
            "MyModelImage": "123456789012.dkr.ecr.us-east-1.amazonaws.com/mymodel:latest"
         },
         "eu-west-1": {
            "MyModelImage": "123456789012.dkr.ecr.eu-west-1.amazonaws.com/mymodel:latest"
         },
         "ap-northeast-1": {
            "MyModelImage": "123456789012.dkr.ecr.ap-northeast-1.amazonaws.com/mymodel:latest"
         },
         "ap-northeast-2": {
            "MyModelImage": "123456789012.dkr.ecr.ap-northeast-2.amazonaws.com/mymodel:latest"
         },
         "ap-southeast-2": {
            "MyModelImage": "123456789012.dkr.ecr.ap-southeast-2.amazonaws.com/mymodel:latest"
         },
         "eu-central-1": {
            "MyModelImage": "123456789012.dkr.ecr.eu-central-1.amazonaws.com/mymodel:latest"
         }
      }
   },
   "Resources": {
      "Endpoint": {
         "Type": "AWS::SageMaker::Endpoint",
         "Properties": {
            "EndpointConfigName": { "Fn::GetAtt" : ["EndpointConfigWithDataCapture", "EndpointConfigName"] }
         }
      },
      "EndpointConfigWithDataCapture": {
         "Type": "AWS::SageMaker::EndpointConfig",
         "Properties": {
            "ProductionVariants": [
               {
                  "InitialInstanceCount": 1,
                  "InitialVariantWeight": 1,
                  "InstanceType": "ml.t2.large",
                  "ModelName": { "Fn::GetAtt" : ["Model", "ModelName"] },
                  "VariantName": { "Fn::GetAtt" : ["Model", "ModelName"] }
               }
            ],
            "DataCaptureConfig": {
               "EnableCapture": true,
               "InitialSamplingPercentage": 100,
               "DestinationS3Uri": "s3://bucket/prefix",
               "KmsKeyId": "kmskeyid",
               "CaptureOptions": [
                  {
                     "CaptureMode": "Input"
                  }
               ],
               "CaptureContentTypeHeader": {
                  "CsvContentTypes": [
                     "text/csv"
                  ],
                  "JsonContentTypes": [
                     "application/json"
                  ]
               }
            }
         }
      },
      "Model": {
         "Type": "AWS::SageMaker::Model",
         "Properties": {
            "PrimaryContainer": {
               "Image": { "Fn::FindInMap": [
                  "RegionMap",
                  {"Ref": "AWS::Region"},
                  "MyModelImage"
                 ]
               }
            },
            "ExecutionRoleArn": { "Fn::GetAtt" : ["ExecutionRole", "Arn"] }
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
      "JobDefinitionExecutionRole": {
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
      "JobDefinition": {
         "Type": "AWS::SageMaker::ModelQualityJobDefinition",
         "Properties": {
            "ModelQualityAppSpecification": {
               "ImageUri": {
                  "Fn::Sub": "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-model-monitor-analyzer:latest"
               },
               "ProblemType": "BinaryClassification"
            },
            "ModelQualityJobInput": {
               "EndpointInput": {
                  "EndpointName": { "Fn::GetAtt" : ["Endpoint", "EndpointName"] },
                  "LocalPath": "/opt/ml/processing/endpointdata",
                  "InferenceAttribute": "inference",
                  "ProbabilityAttribute": "probability",
                  "ProbabilityThresholdAttribute": 0.8,
                  "StartTimeOffset": "-PT1H",
                  "EndTimeOffset": "-P0D"
               },
               "GroundTruthS3Input": {
                  "S3Uri": {
                     "Fn::Sub": "s3://model-quality-job-definition-${AWS::AccountId}/groundtruth"
                  }
               }
            },
            "ModelQualityJobOutputConfig": {
               "MonitoringOutputs": [
                  {
                     "S3Output": {
                        "LocalPath": "/opt/ml/processing/localpath",
                        "S3Uri": {
                           "Fn::Sub": "s3://model-quality-job-definition-${AWS::AccountId}/output"
                        }
                     }
                  }
               ]
            },
            "JobResources": {
               "ClusterConfig": {
                  "InstanceCount": 1,
                  "InstanceType": "ml.m5.large",
                  "VolumeSizeInGB": 50
               }
            },
            "RoleArn": { "Fn::GetAtt" : ["JobDefinitionExecutionRole", "Arn"] },
            "StoppingCondition": {
               "MaxRuntimeInSeconds": 2000
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-sagemaker-modelqualityjobdefinition--examples--SageMaker_ModelQualityJobDefinition_Example--yaml"></a>

```
---
 
AWSTemplateFormatVersion: '2010-09-09'
Description: Basic SageMaker Hosting entities to create a model quality job definition
 
Mappings: 
  RegionMap: 
    "us-west-2":
      "MyModelImage": "123456789012.dkr.ecr.us-west-2.amazonaws.com/mymodel:latest"
    "us-east-2":
      "MyModelImage": "123456789012.dkr.ecr.us-east-2.amazonaws.com/mymodel:latest"
    "us-east-1":
      "MyModelImage": "123456789012.dkr.ecr.us-east-1.amazonaws.com/mymodel:latest"
    "eu-west-1":
      "MyModelImage": "123456789012.dkr.ecr.eu-west-1.amazonaws.com/mymodel:latest"
    "ap-northeast-1":
      "MyModelImage": "123456789012.dkr.ecr.ap-northeast-1.amazonaws.com/mymodel:latest"
    "ap-northeast-2":
      "MyModelImage": "123456789012.dkr.ecr.ap-northeast-2.amazonaws.com/mymodel:latest"
    "ap-southeast-2":
      "MyModelImage": "123456789012.dkr.ecr.ap-southeast-2.amazonaws.com/mymodel:latest"
    "eu-central-1":
      "MyModelImage": "123456789012.dkr.ecr.eu-central-1.amazonaws.com/mymodel:latest"
 
Resources:
  Endpoint:
    Type: "AWS::SageMaker::Endpoint"
    Properties:
      EndpointConfigName:
        !GetAtt EndpointConfigWithDataCapture.EndpointConfigName
 
  EndpointConfigWithDataCapture:
    Type: "AWS::SageMaker::EndpointConfig"
    Properties:
      ProductionVariants:
        - InitialInstanceCount: 1
          InitialVariantWeight: 1.0
          InstanceType: ml.t2.large
          ModelName: !GetAtt Model.ModelName
          VariantName: !GetAtt Model.ModelName
      DataCaptureConfig:
        EnableCapture: true
        InitialSamplingPercentage: 100
        DestinationS3Uri: s3://bucket/prefix
        KmsKeyId: kmskeyid
        CaptureOptions:
          - CaptureMode: Input
        CaptureContentTypeHeader:
          CsvContentTypes:
            - "text/csv"
          JsonContentTypes:
            - "application/json"
            
  Model:
    Type: "AWS::SageMaker::Model"
    Properties:
      PrimaryContainer:
        Image: !FindInMap [RegionMap, !Ref "AWS::Region", "MyModelImage"]
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
 
  JobDefinitionExecutionRole:
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
 
  JobDefinition:
    Type: AWS::SageMaker::ModelQualityJobDefinition
    Properties:
      ModelQualityAppSpecification:
        ImageUri:
          Fn::Sub: "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-model-monitor-analyzer:latest"
        ProblemType: BinaryClassification
      ModelQualityJobInput:
        EndpointInput:
          EndpointName: !GetAtt Endpoint.EndpointName
          LocalPath: "/opt/ml/processing/endpointdata"
          InferenceAttribute: inference
          ProbabilityAttribute: probability
          ProbabilityThresholdAttribute: 0.8
          StartTimeOffset: "-PT1H"
          EndTimeOffset: "-P0D"
        GroundTruthS3Input:
          S3Uri:
            Fn::Sub: "s3://model-quality-job-definition-${AWS::AccountId}/groundtruth"
      ModelQualityJobOutputConfig:
        MonitoringOutputs:
          - S3Output:
              LocalPath: "/opt/ml/processing/localpath"
              S3Uri:
                Fn::Sub: "s3://model-quality-job-definition-${AWS::AccountId}/output"
      JobResources:
        ClusterConfig:
          InstanceCount: 1
          InstanceType: ml.m5.large
          VolumeSizeInGB: 50
      RoleArn: !GetAtt JobDefinitionExecutionRole.Arn
      StoppingCondition:
        MaxRuntimeInSeconds: 2000
```