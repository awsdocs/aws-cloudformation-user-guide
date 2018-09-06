# AWS::SageMaker::EndpointConfig<a name="aws-resource-sagemaker-endpointconfig"></a>

The `AWS::SageMaker::EndpointConfig` resource creates a configuration for an Amazon SageMaker endpoint\. For more information, see [CreateEndpointConfig](http://docs.aws.amazon.com/sagemaker/latest/dg/API_CreateEndpointConfig.html) in the *SageMaker Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-sagemaker-endpointconfig-syntax)
+ [Properties](#aws-resource-sagemaker-endpointconfig-properties)
+ [Return Values](#aws-resource-sagemaker-endpointconfig-returnvalues)
+ [Examples](#aws-resource-sagemaker-endpointconfig-examples)

## Syntax<a name="aws-resource-sagemaker-endpointconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-endpointconfig-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::EndpointConfig",
  "Properties" : {
    "[Tags](aws-resource-sagemaker-endpoint.md#cfn-sagemaker-endpoint-tags)" : [ [*ProductionVariants*](aws-properties-sagemaker-endpointconfig-productionvariant.md), ... ]
    "[EndpointConfigName](#cfn-sagemaker-endpointconfig-endpointconfigname)" : String,
    "[KmsKeyId](#cfn-sagemaker-endpointconfig-kmskeyid)" : String,
    "[Tags](#cfn-sagemaker-endpointconfig-tags)" : [ [*Tag*](aws-properties-sagemaker-endpointconfig-tag.md), ... ]
  }
}
```

### YAML<a name="aws-resource-sagemaker-endpointconfig-syntax.yaml"></a>

```
Type: "AWS::SageMaker::EndpointConfig"
Properties:
    [ProductionVariants](#cfn-sagemaker-endpointconfig-productionvariants): 
    - [*ProductionVariants*](aws-properties-sagemaker-endpointconfig-productionvariant.md)
  [EndpointConfigName](#cfn-sagemaker-endpointconfig-endpointconfigname): String
  [KmsKeyId](#cfn-sagemaker-endpointconfig-kmskeyid): String
  [Tags](#cfn-sagemaker-endpointconfig-tags): 
    - [*Tag*](aws-properties-sagemaker-endpointconfig-tag.md)
```

## Properties<a name="aws-resource-sagemaker-endpointconfig-properties"></a>

`ProductionVariants`  <a name="cfn-sagemaker-endpointconfig-productionvariants"></a>
A list of the production variants that specify the models you want to host at this endpoint\.  
 *Required*: Yes  
 *Type*: List of [Amazon SageMaker EndpointConfig ProductionVariant](aws-properties-sagemaker-endpointconfig-productionvariant.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EndpointConfigName`  <a name="cfn-sagemaker-endpointconfig-endpointconfigname"></a>
The name of the endpoint configuration\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`KmsKeyId`  <a name="cfn-sagemaker-endpointconfig-kmskeyid"></a>
If you provide a AWS KMS key ID, Amazon SageMaker uses it to encrypt data at rest on the ML storage volume that is attached to your notebook instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-sagemaker-endpointconfig-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: Yes  
 *Type*: List of [Amazon SageMaker EndpointConfig Tag](aws-properties-sagemaker-endpointconfig-tag.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-sagemaker-endpointconfig-returnvalues"></a>

### Ref<a name="aws-resource-sagemaker-endpointconfig-ref"></a>

When you pass the logical ID of an `AWS::SageMaker::EndpointConfig` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the endpoint configuration, such as `arn:aws:sagemaker:us-west-2:012345678901:endpoint-config/myendpointconfig`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-sagemaker-endpointconfig-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`EndpointConfigName`  
The name of the endpoint confugration, such as `MyEndpointConfiguration`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-sagemaker-endpointconfig-examples"></a>

### SageMaker Endpoint Example<a name="aws-resource-sagemaker-endpointconfig-example1"></a>

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