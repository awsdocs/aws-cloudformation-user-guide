# AWS::SageMaker::ModelBiasJobDefinition<a name="aws-resource-sagemaker-modelbiasjobdefinition"></a>

Creates the definition for a model bias job\.

## Syntax<a name="aws-resource-sagemaker-modelbiasjobdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-modelbiasjobdefinition-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::ModelBiasJobDefinition",
  "Properties" : {
      "[EndpointName](#cfn-sagemaker-modelbiasjobdefinition-endpointname)" : String,
      "[JobDefinitionName](#cfn-sagemaker-modelbiasjobdefinition-jobdefinitionname)" : String,
      "[JobResources](#cfn-sagemaker-modelbiasjobdefinition-jobresources)" : MonitoringResources,
      "[ModelBiasAppSpecification](#cfn-sagemaker-modelbiasjobdefinition-modelbiasappspecification)" : ModelBiasAppSpecification,
      "[ModelBiasBaselineConfig](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig)" : ModelBiasBaselineConfig,
      "[ModelBiasJobInput](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput)" : ModelBiasJobInput,
      "[ModelBiasJobOutputConfig](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjoboutputconfig)" : MonitoringOutputConfig,
      "[NetworkConfig](#cfn-sagemaker-modelbiasjobdefinition-networkconfig)" : NetworkConfig,
      "[RoleArn](#cfn-sagemaker-modelbiasjobdefinition-rolearn)" : String,
      "[StoppingCondition](#cfn-sagemaker-modelbiasjobdefinition-stoppingcondition)" : StoppingCondition,
      "[Tags](#cfn-sagemaker-modelbiasjobdefinition-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-modelbiasjobdefinition-syntax.yaml"></a>

```
Type: AWS::SageMaker::ModelBiasJobDefinition
Properties: 
  [EndpointName](#cfn-sagemaker-modelbiasjobdefinition-endpointname): String
  [JobDefinitionName](#cfn-sagemaker-modelbiasjobdefinition-jobdefinitionname): String
  [JobResources](#cfn-sagemaker-modelbiasjobdefinition-jobresources): 
    MonitoringResources
  [ModelBiasAppSpecification](#cfn-sagemaker-modelbiasjobdefinition-modelbiasappspecification): 
    ModelBiasAppSpecification
  [ModelBiasBaselineConfig](#cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig): 
    ModelBiasBaselineConfig
  [ModelBiasJobInput](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput): 
    ModelBiasJobInput
  [ModelBiasJobOutputConfig](#cfn-sagemaker-modelbiasjobdefinition-modelbiasjoboutputconfig): 
    MonitoringOutputConfig
  [NetworkConfig](#cfn-sagemaker-modelbiasjobdefinition-networkconfig): 
    NetworkConfig
  [RoleArn](#cfn-sagemaker-modelbiasjobdefinition-rolearn): String
  [StoppingCondition](#cfn-sagemaker-modelbiasjobdefinition-stoppingcondition): 
    StoppingCondition
  [Tags](#cfn-sagemaker-modelbiasjobdefinition-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-modelbiasjobdefinition-properties"></a>

`EndpointName`  <a name="cfn-sagemaker-modelbiasjobdefinition-endpointname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobDefinitionName`  <a name="cfn-sagemaker-modelbiasjobdefinition-jobdefinitionname"></a>
The name of the bias job definition\. The name must be unique within an AWS Region in the AWS account\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobResources`  <a name="cfn-sagemaker-modelbiasjobdefinition-jobresources"></a>
Identifies the resources to deploy for a monitoring job\.  
*Required*: Yes  
*Type*: [MonitoringResources](aws-properties-sagemaker-modelbiasjobdefinition-monitoringresources.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelBiasAppSpecification`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasappspecification"></a>
Configures the model bias job to run a specified Docker container image\.  
*Required*: Yes  
*Type*: [ModelBiasAppSpecification](aws-properties-sagemaker-modelbiasjobdefinition-modelbiasappspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelBiasBaselineConfig`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig"></a>
The baseline configuration for a model bias job\.  
*Required*: No  
*Type*: [ModelBiasBaselineConfig](aws-properties-sagemaker-modelbiasjobdefinition-modelbiasbaselineconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelBiasJobInput`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasjobinput"></a>
Inputs for the model bias job\.  
*Required*: Yes  
*Type*: [ModelBiasJobInput](aws-properties-sagemaker-modelbiasjobdefinition-modelbiasjobinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelBiasJobOutputConfig`  <a name="cfn-sagemaker-modelbiasjobdefinition-modelbiasjoboutputconfig"></a>
The output configuration for monitoring jobs\.  
*Required*: Yes  
*Type*: [MonitoringOutputConfig](aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutputconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfig`  <a name="cfn-sagemaker-modelbiasjobdefinition-networkconfig"></a>
Networking options for a model bias job\.  
*Required*: No  
*Type*: [NetworkConfig](aws-properties-sagemaker-modelbiasjobdefinition-networkconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-sagemaker-modelbiasjobdefinition-rolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that Amazon SageMaker can assume to perform tasks on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StoppingCondition`  <a name="cfn-sagemaker-modelbiasjobdefinition-stoppingcondition"></a>
A time limit for how long the monitoring job is allowed to run before stopping\.  
*Required*: No  
*Type*: [StoppingCondition](aws-properties-sagemaker-modelbiasjobdefinition-stoppingcondition.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-modelbiasjobdefinition-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-modelbiasjobdefinition-return-values"></a>

### Ref<a name="aws-resource-sagemaker-modelbiasjobdefinition-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-modelbiasjobdefinition-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-modelbiasjobdefinition-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time when the job definition was created\.

`JobDefinitionArn`  <a name="JobDefinitionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the job definition\.

## Examples<a name="aws-resource-sagemaker-modelbiasjobdefinition--examples"></a>

### SageMaker ModelBiasJobDefinition Example<a name="aws-resource-sagemaker-modelbiasjobdefinition--examples--SageMaker_ModelBiasJobDefinition_Example"></a>

The following example creates a Model Bias monitoring job definition\.

#### JSON<a name="aws-resource-sagemaker-modelbiasjobdefinition--examples--SageMaker_ModelBiasJobDefinition_Example--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Basic SageMaker Hosting entities to create a model bias job definition",
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
            "EndpointConfigName": null
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
                  "ModelName": null,
                  "VariantName": null
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
         "Type": "AWS::SageMaker::ModelBiasJobDefinition",
         "Properties": {
            "ModelBiasAppSpecification": {
               "ImageUri": {
                  "Fn::Sub": "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-clarify-processing:1.0"
               },
               "ConfigUri": "s3://configUri"
            },
            "ModelBiasJobInput": {
               "EndpointInput": {
                  "EndpointName": null,
                  "LocalPath": "/opt/ml/processing/endpointdata",
                  "FeaturesAttribute": "feature",
                  "InferenceAttribute": "inference",
                  "ProbabilityAttribute": "probability",
                  "ProbabilityThresholdAttribute": 0.8,
                  "StartTimeOffset": "-PT1H",
                  "EndTimeOffset": "-P0D"
               },
               "GroundTruthS3Input": {
                  "S3Uri": {
                     "Fn::Sub": "s3://model-bias-job-definition-${AWS::AccountId}/groundtruth"
                  }
               }
            },
            "ModelBiasJobOutputConfig": {
               "MonitoringOutputs": [
                  {
                     "S3Output": {
                        "LocalPath": "/opt/ml/processing/localpath",
                        "S3Uri": {
                           "Fn::Sub": "s3://model-bias-job-definition-${AWS::AccountId}/output"
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
            "RoleArn": null,
            "StoppingCondition": {
               "MaxRuntimeInSeconds": 2000
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-sagemaker-modelbiasjobdefinition--examples--SageMaker_ModelBiasJobDefinition_Example--yaml"></a>

```
---
 
AWSTemplateFormatVersion: '2010-09-09'
Description: Basic SageMaker Hosting entities to create a model bias job definition
 
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
    Type: AWS::SageMaker::ModelBiasJobDefinition
    Properties:
      ModelBiasAppSpecification:
        ImageUri:
          Fn::Sub: "123456789012.dkr.ecr.${AWS::Partition}.amazonaws.com/sagemaker-clarify-processing:1.0"
        ConfigUri: "s3://configUri"
      ModelBiasJobInput:
        EndpointInput:
          EndpointName: !GetAtt Endpoint.EndpointName
          LocalPath: "/opt/ml/processing/endpointdata"
          FeaturesAttribute: feature
          InferenceAttribute: inference
          ProbabilityAttribute: probability
          ProbabilityThresholdAttribute: 0.8
          StartTimeOffset: "-PT1H"
          EndTimeOffset: "-P0D"
        GroundTruthS3Input:
          S3Uri:
            Fn::Sub: "s3://model-bias-job-definition-${AWS::AccountId}/groundtruth"
      ModelBiasJobOutputConfig:
        MonitoringOutputs:
          - S3Output:
              LocalPath: "/opt/ml/processing/localpath"
              S3Uri:
                Fn::Sub: "s3://model-bias-job-definition-${AWS::AccountId}/output"
      JobResources:
        ClusterConfig:
          InstanceCount: 1
          InstanceType: ml.m5.large
          VolumeSizeInGB: 50
      RoleArn: !GetAtt JobDefinitionExecutionRole.Arn
      StoppingCondition:
        MaxRuntimeInSeconds: 2000
```