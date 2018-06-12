# AWS::SageMaker::Model<a name="aws-resource-sagemaker-model"></a>

The `AWS::SageMaker::Model` resource to create a model to host at an Amazon SageMaker endpoint\. For more information, see [Deploying a Model on Amazon SageMaker Hosting Services](http://docs.aws.amazon.com/sagemaker/latest/dg/how-it-works-hosting.html) in the *Amazon SageMaker Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-sagemaker-model-syntax)
+ [Properties](#aws-resource-sagemaker-model-properties)
+ [Return Values](#aws-resource-sagemaker-model-returnvalues)
+ [Examples](#aws-resource-sagemaker-model-examples)

## Syntax<a name="aws-resource-sagemaker-model-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-model-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Model",
  "Properties" : {
    "[ExecutionRoleArn](#cfn-sagemaker-model-executionrolearn)" : String,
    "[PrimaryContainer](#cfn-sagemaker-model-primarycontainer)" : [*Tag*](aws-properties-sagemaker-model-containerdefinition.md),
    "[ModelName](#cfn-sagemaker-model-modelname)" : String,
    "[VpcConfig](#cfn-sagemaker-model-vpcconfig)" : [*Tag*](aws-properties-sagemaker-notebookinstance-tag.md),
    "[Tags](#cfn-sagemaker-model-tags)" : [ [*Tag*](aws-properties-sagemaker-model-tag.md), ... ]
  }
}
```

### YAML<a name="aws-resource-sagemaker-model-syntax.yaml"></a>

```
Type: "AWS::SageMaker::Model"
Properties:
  [ExecutionRoleArn](#cfn-sagemaker-model-executionrolearn): String
  [PrimaryContainer](#cfn-sagemaker-model-primarycontainer): [*Tag*](aws-properties-sagemaker-model-containerdefinition.md)
  [ModelName](#cfn-sagemaker-model-modelname): String
  [VpcConfig](#cfn-sagemaker-model-vpcconfig): [*Tag*](aws-properties-sagemaker-notebookinstance-tag.md)
  [Tags](#cfn-sagemaker-model-tags): 
    - [*Tag*](aws-properties-sagemaker-model-tag.md)
```

## Properties<a name="aws-resource-sagemaker-model-properties"></a>

`ExecutionRoleArn`  <a name="cfn-sagemaker-model-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that Amazon SageMaker can assume to access model artifacts and docker image for deployment on ML compute instances\. Deploying on ML compute instances is part of model hosting\. For more information, see [Amazon SageMaker Roles](http://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-roles.html)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`PrimaryContainer`  <a name="cfn-sagemaker-model-primarycontainer"></a>
The location of the primary docker image containing inference code, associated artifacts, and custom environment map that the inference code uses when the model is deployed into production\.   
 *Required*: Yes  
 *Type*: [Amazon SageMaker Model ContainerDefinition](aws-properties-sagemaker-model-containerdefinition.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ModelName`  <a name="cfn-sagemaker-model-modelname"></a>
The name of the model\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VpcConfig`  <a name="cfn-sagemaker-model-vpcconfig"></a>
A VpcConfig object that specifies the VPC that you want your model to connect to\. Control access to and from your model container by configuring the VPC\. For more information, see [Protect Models by Using an Amazon Virtual Private Cloud](http://docs.aws.amazon.com/sagemaker/latest/dg/host-vpc.html)\.  
 *Required*: No  
 *Type*: [Amazon SageMaker Model VpcConfig](aws-properties-sagemaker-model-vpcconfig.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-sagemaker-model-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: No  
 *Type*: List of [Amazon SageMaker Model Tag](aws-properties-sagemaker-model-tag.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-sagemaker-model-returnvalues"></a>

### Ref<a name="aws-resource-sagemaker-model-ref"></a>

When you pass the logical ID of an `AWS::SageMaker::Model` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the model, such as `arn:aws:sagemaker:us-west-2:012345678901:model/mymodel`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-sagemaker-model-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`ModelName`  
The name of the model, such as `MyModel`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-sagemaker-model-examples"></a>

### SageMaker Endpoint Example<a name="aws-resource-sagemaker-model-example1"></a>

The following example creates an endpoint configuration from a trained model, and then creates an endpoint\.

#### JSON<a name="aws-resource-sagemaker-endpoint-example1.json"></a>

```
{
  "Description": "Basic Hosting entities test.  We need models to create endpoint configs.",
  "Mappings": {
    "RegionMap": {
      "us-west-2": {
        "NullTransformer": "12345678901.dkr.ecr.us-west-2.amazonaws.com/mymodel:latest"
      },
      "us-east-2": {
        "NullTransformer": "12345678901.dkr.ecr.us-east-2.amazonaws.com/mymodel:latest"
      },
      "us-east-1": {
        "NullTransformer": "12345678901.dkr.ecr.us-east-1.amazonaws.com/mymodel:latest"
      },
      "eu-west-1": {
        "NullTransformer": "12345678901.dkr.ecr.eu-west-1.amazonaws.com/mymodel:latest"
      },
      "ap-northeast-1": {
        "NullTransformer": "12345678901.dkr.ecr.ap-northeast-1.amazonaws.com/mymodel:latest"
      },
      "ap-northeast-2": {
        "NullTransformer": "12345678901.dkr.ecr.ap-northeast-2.amazonaws.com/mymodel:latest"
      },
      "ap-southeast-2": {
        "NullTransformer": "12345678901.dkr.ecr.ap-southeast-2.amazonaws.com/mymodel:latest"
      },
      "eu-central-1": {
        "NullTransformer": "12345678901.dkr.ecr.eu-central-1.amazonaws.com/mymodel:latest"
      }
    }
  },
  "Resources": {
    "Endpoint": {
      "Type": "AWS::SageMaker::Endpoint",
      "Properties": {
        "EndpointConfigName": { "Fn::GetAtt" : ["EndpointConfig", "EndpointConfigName" ] }
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
            "ModelName": { "Fn::GetAtt" : ["Model", "ModelName" ] },
            "VariantName": { "Fn::GetAtt" : ["Model", "ModelName" ] }
          }
        ]
      }
    },
    "Model": {
      "Type": "AWS::SageMaker::Model",
      "Properties": {
        "PrimaryContainer": {
          "Image": { "Fn::FindInMap" : [ "AWS::Region", "NullTransformer"] }
        },
        "ExecutionRoleArn": { "Fn::GetAtt" : [ "ExecutionRole", "Arn" ] }
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
    }
  },
  "Outputs": {
    "EndpointId": {
      "Value": { "Ref" : "Endpoint" }
    },
    "EndpointName": {
      "Value": { "Fn::GetAtt" : [ "Endpoint", "EndpointName" ] }
    }
    
  },
  
}
```

#### YAML<a name="aws-resource-sagemaker-endpoint-example1.yaml"></a>

```
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
  Outputs:
    EndpointId:
      Value: !Ref Endpoint
    EndpointName:
      Value: !GetAtt Endpoint.EndpointName
```