# AWS::SageMaker::Model<a name="aws-resource-sagemaker-model"></a>

The `AWS::SageMaker::Model` resource to create a model to host at an Amazon SageMaker endpoint\. For more information, see [Deploying a Model on Amazon SageMaker Hosting Services](https://docs.aws.amazon.com/sagemaker/latest/dg/how-it-works-hosting.html) in the *Amazon SageMaker Developer Guide*\. 

## Syntax<a name="aws-resource-sagemaker-model-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-model-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Model",
  "Properties" : {
      "[Containers](#cfn-sagemaker-model-containers)" : [ ContainerDefinition, ... ],
      "[EnableNetworkIsolation](#cfn-sagemaker-model-enablenetworkisolation)" : Boolean,
      "[ExecutionRoleArn](#cfn-sagemaker-model-executionrolearn)" : String,
      "[ModelName](#cfn-sagemaker-model-modelname)" : String,
      "[PrimaryContainer](#cfn-sagemaker-model-primarycontainer)" : ContainerDefinition,
      "[Tags](#cfn-sagemaker-model-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcConfig](#cfn-sagemaker-model-vpcconfig)" : VpcConfig
    }
}
```

### YAML<a name="aws-resource-sagemaker-model-syntax.yaml"></a>

```
Type: AWS::SageMaker::Model
Properties: 
  [Containers](#cfn-sagemaker-model-containers): 
    - ContainerDefinition
  [EnableNetworkIsolation](#cfn-sagemaker-model-enablenetworkisolation): Boolean
  [ExecutionRoleArn](#cfn-sagemaker-model-executionrolearn): String
  [ModelName](#cfn-sagemaker-model-modelname): String
  [PrimaryContainer](#cfn-sagemaker-model-primarycontainer): 
    ContainerDefinition
  [Tags](#cfn-sagemaker-model-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcConfig](#cfn-sagemaker-model-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-resource-sagemaker-model-properties"></a>

`Containers`  <a name="cfn-sagemaker-model-containers"></a>
Specifies the containers in the inference pipeline\.  
*Required*: No  
*Type*: List of [ContainerDefinition](aws-properties-sagemaker-model-containerdefinition.md)  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableNetworkIsolation`  <a name="cfn-sagemaker-model-enablenetworkisolation"></a>
Isolates the model container\. No inbound or outbound network calls can be made to or from the model container\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecutionRoleArn`  <a name="cfn-sagemaker-model-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that Amazon SageMaker can assume to access model artifacts and docker image for deployment on ML compute instances or for batch transform jobs\. Deploying on ML compute instances is part of model hosting\. For more information, see [Amazon SageMaker Roles](https://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-roles.html)\.   
To be able to pass this role to Amazon SageMaker, the caller of this API must have the `iam:PassRole` permission\.
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelName`  <a name="cfn-sagemaker-model-modelname"></a>
The name of the new model\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrimaryContainer`  <a name="cfn-sagemaker-model-primarycontainer"></a>
The location of the primary docker image containing inference code, associated artifacts, and custom environment map that the inference code uses when the model is deployed for predictions\.   
*Required*: No  
*Type*: [ContainerDefinition](aws-properties-sagemaker-model-containerdefinition.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-model-tags"></a>
A list of key\-value pairs to apply to this resource\.  
For more information, see [Resource Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) and [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what) in the *AWS Billing and Cost Management User Guide*\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-sagemaker-model-vpcconfig"></a>
A [VpcConfig](https://docs.aws.amazon.com/sagemaker/latest/dg/API_VpcConfig.html) object that specifies the VPC that you want your model to connect to\. Control access to and from your model container by configuring the VPC\. `VpcConfig` is used in hosting services and in batch transform\. For more information, see [Protect Endpoints by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/host-vpc.html) and [Protect Data in Batch Transform Jobs by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/batch-vpc.html)\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-sagemaker-model-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-model-return-values"></a>

### Ref<a name="aws-resource-sagemaker-model-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the model, such as `arn:aws:sagemaker:us-west-2:012345678901:model/mymodel`\.

When you pass the logical ID of an `AWS::SageMaker::Model` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the model, such as `arn:aws:sagemaker:us-west-2:012345678901:model/mymodel`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-model-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

#### <a name="aws-resource-sagemaker-model-return-values-fn--getatt-fn--getatt"></a>

`ModelName`  <a name="ModelName-fn::getatt"></a>
The name of the model, such as `MyModel`\.

## Examples<a name="aws-resource-sagemaker-model--examples"></a>

### SageMaker Model Endpoint Example<a name="aws-resource-sagemaker-model--examples--SageMaker_Model_Endpoint_Example"></a>

The following example creates an endpoint configuration from a trained model, and then creates an endpoint\.

#### JSON<a name="aws-resource-sagemaker-model--examples--SageMaker_Model_Endpoint_Example--json"></a>

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
    
  }
  
}
```

#### YAML<a name="aws-resource-sagemaker-model--examples--SageMaker_Model_Endpoint_Example--yaml"></a>

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