# AWS::SageMaker::NotebookInstanceLifecycleConfig<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig"></a>

The `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource creates shell scripts that run when you create and/or start a notebook instance\. For information about notebook instance lifecycle configurations, see [Customize a Notebook Instance](https://docs.aws.amazon.com/sagemaker/latest/dg/notebook-lifecycle-config.html) in the *Amazon SageMaker Developer Guide*\.

## Syntax<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::NotebookInstanceLifecycleConfig",
  "Properties" : {
      "[NotebookInstanceLifecycleConfigName](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname)" : String,
      "[OnCreate](#cfn-sagemaker-notebookinstancelifecycleconfig-oncreate)" : [ NotebookInstanceLifecycleHook, ... ],
      "[OnStart](#cfn-sagemaker-notebookinstancelifecycleconfig-onstart)" : [ NotebookInstanceLifecycleHook, ... ]
    }
}
```

### YAML<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax.yaml"></a>

```
Type: AWS::SageMaker::NotebookInstanceLifecycleConfig
Properties: 
  [NotebookInstanceLifecycleConfigName](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname): String
  [OnCreate](#cfn-sagemaker-notebookinstancelifecycleconfig-oncreate): 
    - NotebookInstanceLifecycleHook
  [OnStart](#cfn-sagemaker-notebookinstancelifecycleconfig-onstart): 
    - NotebookInstanceLifecycleHook
```

## Properties<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-properties"></a>

`NotebookInstanceLifecycleConfigName`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname"></a>
The name of the lifecycle configuration\.  
*Required*: No  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OnCreate`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-oncreate"></a>
A shell script that runs only once, when you create a notebook instance\. The shell script must be a base64\-encoded string\.  
*Required*: No  
*Type*: List of [NotebookInstanceLifecycleHook](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnStart`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-onstart"></a>
A shell script that runs every time you start a notebook instance, including when you create the notebook instance\. The shell script must be a base64\-encoded string\.  
*Required*: No  
*Type*: List of [NotebookInstanceLifecycleHook](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-return-values"></a>

### Ref<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the endpoint configuration, such as `arn:aws:sagemaker:us-west-2:012345678901:notebook-instance-lifecycle-config/mylifecycleconfig` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

#### <a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-return-values-fn--getatt-fn--getatt"></a>

`NotebookInstanceLifecycleConfigName`  <a name="NotebookInstanceLifecycleConfigName-fn::getatt"></a>
The name of the lifecycle configuration, such as `MyLifecycleConfig`\.

## Examples<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig--examples"></a>

### SageMaker NotebookInstanceLifecycleConfig Example<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig--examples--SageMaker_NotebookInstanceLifecycleConfig_Example"></a>

The following example creates a notebook instance with an associated lifecycle configuration\.

#### JSON<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig--examples--SageMaker_NotebookInstanceLifecycleConfig_Example--json"></a>

```
{
  "Description": "Basic NotebookInstance test",
  "Resources": {
    "BasicNotebookInstance": {
      "Type": "AWS::SageMaker::NotebookInstance",
      "Properties": {
        "InstanceType": "ml.t2.medium",
        "RoleArn": { "Fn::GetAtt" : [ "ExecutionRole", "Arn" ] },
        "LifecycleConfigName": { "Fn::GetAtt" : [ "BasicNotebookInstanceLifecycleConfig", "NotebookInstanceLifecycleConfigName" ] }
    },
    "BasicNotebookInstanceLifecycleConfig": {
      "Type": "AWS::SageMaker::NotebookInstanceLifecycleConfig",
      "Properties": {
        "OnStart": [
          {
            "Content": {
              "Fn::Base64": "echo 'hello'"
            }
          }
        ]
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
    "BasicNotebookInstanceId": {
      "Value": { "Ref" : "BasicNotebookInstance" }
    },
    "BasicNotebookInstanceLifecycleConfigId": {
      "Value": { "Ref" : "BasicNotebookInstanceLifecycleConfig" }
    }
  },
}
```

#### YAML<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig--examples--SageMaker_NotebookInstanceLifecycleConfig_Example--yaml"></a>

```
Description: "Basic NotebookInstance test"
Resources:
  BasicNotebookInstance:
    Type: "AWS::SageMaker::NotebookInstance"
    Properties:
      InstanceType: "ml.t2.medium"
      RoleArn: !GetAtt ExecutionRole.Arn
      LifecycleConfigName: !GetAtt BasicNotebookInstanceLifecycleConfig.NotebookInstanceLifecycleConfigName
  BasicNotebookInstanceLifecycleConfig:
    Type: "AWS::SageMaker::NotebookInstanceLifecycleConfig"
    Properties:
      OnStart:
        - Content:
            Fn::Base64: "echo 'hello'"
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
  BasicNotebookInstanceId:
    Value: !Ref BasicNotebookInstance
  BasicNotebookInstanceLifecycleConfigId:
    Value: !Ref BasicNotebookInstanceLifecycleConfig
```