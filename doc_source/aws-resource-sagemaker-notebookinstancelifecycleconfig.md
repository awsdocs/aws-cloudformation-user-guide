# AWS::SageMaker::NotebookInstanceLifecycleConfig<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig"></a>

The `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource specifies shell scripts that run when you create and/or start a notebook instance\. For more information, see [Customize a Notebook Instance](http://docs.aws.amazon.com/sagemaker/latest/dg/notebook-lifecycle-config.html) in the *Amazon SageMaker Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax)
+ [Properties](#aws-resource-sagemaker-notebookinstancelifecycleconfig-properties)
+ [Return Values](#aws-resource-sagemaker-notebookinstancelifecycleconfig-returnvalues)
+ [Examples](#aws-resource-sagemaker-notebookinstancelifecycleconfig-examples)

## Syntax<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::NotebookInstanceLifecycleConfig",
  "Properties" : {
    "[OnStart](#cfn-sagemaker-notebookinstancelifecycleconfig-onstart)" : [ [*NotebookInstanceLifecycleHook*](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md), ... ],
    "[NotebookInstanceLifecycleConfigName](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname)" : String,
    "[OnCreate](#cfn-sagemaker-notebookinstancelifecycleconfig-oncreate)" : [ [*NotebookInstanceLifecycleHook*](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md), ... ]
  }
}
```

### YAML<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-syntax.yaml"></a>

```
Type: "AWS::SageMaker::NotebookInstanceLifecycleConfig"
Properties:
  [OnStart](#cfn-sagemaker-notebookinstancelifecycleconfig-onstart): 
    - [*NotebookInstanceLifecycleHook*](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)  
  [NotebookInstanceLifecycleConfigName](#cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname): String
  [OnCreate](#cfn-sagemaker-notebookinstancelifecycleconfig-oncreate): 
    - [*NotebookInstanceLifecycleHook*](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)
```

## Properties<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-properties"></a>

`OnStart`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-onstart"></a>
A shell script that runs once when you create a notebook instance, and then each time you start the notebook instance\.  
 *Required*: No  
 *Type*: List of [Amazon SageMaker NotebookInstanceLifecycleConfig NotebookInstanceLifecycleHook](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NotebookInstanceLifecycleConfigName`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecycleconfigname"></a>
The name of the lifecycle configuration\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`OnCreate`  <a name="cfn-sagemaker-notebookinstancelifecycleconfig-oncreate"></a>
A shell script that runs only once, when you create a notebook instance\.  
 *Required*: No  
 *Type*: List of [Amazon SageMaker NotebookInstanceLifecycleConfig NotebookInstanceLifecycleHook](aws-properties-sagemaker-notebookinstancelifecycleconfig-notebookinstancelifecyclehook.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-returnvalues"></a>

### Ref<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-ref"></a>

When you pass the logical ID of an `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the lifecycle configuration, such as `arn:aws:sagemaker:us-west-2:012345678901:notebook-instance-lifecycle-config/mylifecycleconfig`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`NotebookInstanceLifecycleConfigName`  
The name of the lifecycle configuration, such as `MyLifecycleConfig`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-examples"></a>

### Notebook Instance Lifecycle Config Example<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-example1"></a>

The following example creates a notebook instance with an associated lifecycle configuration\.

#### JSON<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-example1.json"></a>

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

#### YAML<a name="aws-resource-sagemaker-notebookinstancelifecycleconfig-example1.yaml"></a>

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