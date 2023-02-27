# AWS::SageMaker::EndpointConfig<a name="aws-resource-sagemaker-endpointconfig"></a>

The `AWS::SageMaker::EndpointConfig` resource creates a configuration for an Amazon SageMaker endpoint\. For more information, see [CreateEndpointConfig](https://docs.aws.amazon.com/sagemaker/latest/dg/API_CreateEndpointConfig.html) in the *SageMaker Developer Guide*\.

## Syntax<a name="aws-resource-sagemaker-endpointconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-endpointconfig-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::EndpointConfig",
  "Properties" : {
      "[AsyncInferenceConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig)" : AsyncInferenceConfig,
      "[DataCaptureConfig](#cfn-sagemaker-endpointconfig-datacaptureconfig)" : DataCaptureConfig,
      "[EndpointConfigName](#cfn-sagemaker-endpointconfig-endpointconfigname)" : String,
      "[ExplainerConfig](#cfn-sagemaker-endpointconfig-explainerconfig)" : ExplainerConfig,
      "[KmsKeyId](#cfn-sagemaker-endpointconfig-kmskeyid)" : String,
      "[ProductionVariants](#cfn-sagemaker-endpointconfig-productionvariants)" : [ ProductionVariant, ... ],
      "[ShadowProductionVariants](#cfn-sagemaker-endpointconfig-shadowproductionvariants)" : [ ProductionVariant, ... ],
      "[Tags](#cfn-sagemaker-endpointconfig-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-endpointconfig-syntax.yaml"></a>

```
Type: AWS::SageMaker::EndpointConfig
Properties: 
  [AsyncInferenceConfig](#cfn-sagemaker-endpointconfig-asyncinferenceconfig): 
    AsyncInferenceConfig
  [DataCaptureConfig](#cfn-sagemaker-endpointconfig-datacaptureconfig): 
    DataCaptureConfig
  [EndpointConfigName](#cfn-sagemaker-endpointconfig-endpointconfigname): String
  [ExplainerConfig](#cfn-sagemaker-endpointconfig-explainerconfig): 
    ExplainerConfig
  [KmsKeyId](#cfn-sagemaker-endpointconfig-kmskeyid): String
  [ProductionVariants](#cfn-sagemaker-endpointconfig-productionvariants): 
    - ProductionVariant
  [ShadowProductionVariants](#cfn-sagemaker-endpointconfig-shadowproductionvariants): 
    - ProductionVariant
  [Tags](#cfn-sagemaker-endpointconfig-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-endpointconfig-properties"></a>

`AsyncInferenceConfig`  <a name="cfn-sagemaker-endpointconfig-asyncinferenceconfig"></a>
Specifies configuration for how an endpoint performs asynchronous inference\.  
*Required*: No  
*Type*: [AsyncInferenceConfig](aws-properties-sagemaker-endpointconfig-asyncinferenceconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataCaptureConfig`  <a name="cfn-sagemaker-endpointconfig-datacaptureconfig"></a>
Specifies how to capture endpoint data for model monitor\. The data capture configuration applies to all production variants hosted at the endpoint\.  
*Required*: No  
*Type*: [DataCaptureConfig](aws-properties-sagemaker-endpointconfig-datacaptureconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointConfigName`  <a name="cfn-sagemaker-endpointconfig-endpointconfigname"></a>
The name of the endpoint configuration\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExplainerConfig`  <a name="cfn-sagemaker-endpointconfig-explainerconfig"></a>
Property description not available\.  
*Required*: No  
*Type*: [ExplainerConfig](aws-properties-sagemaker-endpointconfig-explainerconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-sagemaker-endpointconfig-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of an AWS Key Management Service key that Amazon SageMaker uses to encrypt data on the storage volume attached to the ML compute instance that hosts the endpoint\.  
+ Key ID: `1234abcd-12ab-34cd-56ef-1234567890ab`
+ Key ARN: `arn:aws:kms:us-west-2:111122223333:key/1234abcd-12ab-34cd-56ef-1234567890ab`
+ Alias name: `alias/ExampleAlias`
+ Alias name ARN: `arn:aws:kms:us-west-2:111122223333:alias/ExampleAlias`
The KMS key policy must grant permission to the IAM role that you specify in your `CreateEndpoint`, `UpdateEndpoint` requests\. For more information, refer to the AWS Key Management Service section [Using Key Policies in AWS KMS ](https://docs.aws.amazon.com/kms/latest/developerguide/key-policies.html)  
Certain Nitro\-based instances include local storage, dependent on the instance type\. Local storage volumes are encrypted using a hardware module on the instance\. You can't request a `KmsKeyId` when using an instance type with local storage\. If any of the models that you specify in the `ProductionVariants` parameter use nitro\-based instances with local storage, do not specify a value for the `KmsKeyId` parameter\. If you specify a value for `KmsKeyId` when using any nitro\-based instances with local storage, the call to `CreateEndpointConfig` fails\.  
For a list of instance types that support local instance storage, see [Instance Store Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html#instance-store-volumes)\.  
For more information about local instance storage encryption, see [SSD Instance Store Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ssd-instance-store.html)\.
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductionVariants`  <a name="cfn-sagemaker-endpointconfig-productionvariants"></a>
A list of `ProductionVariant` objects, one for each model that you want to host at this endpoint\.  
*Required*: Yes  
*Type*: List of [ProductionVariant](aws-properties-sagemaker-endpointconfig-productionvariant.md)  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShadowProductionVariants`  <a name="cfn-sagemaker-endpointconfig-shadowproductionvariants"></a>
Array of `ProductionVariant` objects\. There is one for each model that you want to host at this endpoint in shadow mode with production traffic replicated from the model specified on `ProductionVariants`\. If you use this field, you can only specify one variant for `ProductionVariants` and one variant for `ShadowProductionVariants`\.  
*Required*: No  
*Type*: List of [ProductionVariant](aws-properties-sagemaker-endpointconfig-productionvariant.md)  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-endpointconfig-tags"></a>
A list of key\-value pairs to apply to this resource\.  
For more information, see [Resource Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) and [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html#allocation-what)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-endpointconfig-return-values"></a>

### Ref<a name="aws-resource-sagemaker-endpointconfig-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the endpoint configuration, such as `arn:aws:sagemaker:us-west-2:01234567>8901:endpoint-config/myendpointconfig` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-endpointconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-sagemaker-endpointconfig-return-values-fn--getatt-fn--getatt"></a>

`EndpointConfigName`  <a name="EndpointConfigName-fn::getatt"></a>
The name of the endpoint configuration, such as `MyEndpointConfiguration`\.

## Examples<a name="aws-resource-sagemaker-endpointconfig--examples"></a>

### SageMaker EndpointConfig Example<a name="aws-resource-sagemaker-endpointconfig--examples--SageMaker_EndpointConfig_Example"></a>

The following example creates an endpoint configuration from a trained model, and then creates an endpoint\.

#### JSON<a name="aws-resource-sagemaker-endpointconfig--examples--SageMaker_EndpointConfig_Example--json"></a>

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

#### YAML<a name="aws-resource-sagemaker-endpointconfig--examples--SageMaker_EndpointConfig_Example--yaml"></a>

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