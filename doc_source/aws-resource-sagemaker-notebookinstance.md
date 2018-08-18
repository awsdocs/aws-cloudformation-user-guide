# AWS::SageMaker::NotebookInstance<a name="aws-resource-sagemaker-notebookinstance"></a>

The `AWS::SageMaker::NotebookInstance` resource Creates an Amazon SageMaker notebook instance\. A notebook instance is a machine learning \(ML\) compute instance running on a Jupyter notebook\. For more information, see [Using Notebook Instances](http://docs.aws.amazon.com/sagemaker/latest/dg/nbi.html) in the *Amazon SageMaker Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-sagemaker-notebookinstance-syntax)
+ [Properties](#aws-resource-sagemaker-notebookinstance-properties)
+ [Return Values](#aws-resource-sagemaker-notebookinstance-returnvalues)
+ [Examples](#aws-resource-sagemaker-notebookinstance-examples)

## Syntax<a name="aws-resource-sagemaker-notebookinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-notebookinstance-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::NotebookInstance",
  "Properties" : {
    "[KmsKeyId](#cfn-sagemaker-notebookinstance-kmskeyid)" : String,
    "[DirectInternetAccess](#cfn-sagemaker-notebookinstance-directinternetaccess)" : String,
    "[SubnetId](#cfn-sagemaker-notebookinstance-subnetid)" : String,
    "[NotebookInstanceName](#cfn-sagemaker-notebookinstance-notebookinstancename)" : String,
    "[InstanceType](#cfn-sagemaker-notebookinstance-instancetype)" : String,
    "[LifecycleConfigName](#cfn-sagemaker-notebookinstance-lifecycleconfigname)" : String,
    "[SecurityGroupIds](#cfn-sagemaker-notebookinstance-securitygroupids)" : [ String, ... ],
    "[RoleArn](#cfn-sagemaker-notebookinstance-rolearn)" : String,
    "[Tags](#cfn-sagemaker-notebookinstance-tags)" : [ [*Tag*](aws-properties-sagemaker-notebookinstance-tag.md), ... ]
  }
}
```

### YAML<a name="aws-resource-sagemaker-notebookinstance-syntax.yaml"></a>

```
Type: "AWS::SageMaker::NotebookInstance"
Properties:
  [KmsKeyId](#cfn-sagemaker-notebookinstance-kmskeyid): String
  [DirectInternetAccess](#cfn-sagemaker-notebookinstance-directinternetaccess): String
  [SubnetId](#cfn-sagemaker-notebookinstance-subnetid): String
  [NotebookInstanceName](#cfn-sagemaker-notebookinstance-notebookinstancename): String
  [InstanceType](#cfn-sagemaker-notebookinstance-instancetype): String
  [LifecycleConfigName](#cfn-sagemaker-notebookinstance-lifecycleconfigname): String
  [SecurityGroupIds](#cfn-sagemaker-notebookinstance-securitygroupids): String
  [SecurityGroupIds](#cfn-sagemaker-notebookinstance-securitygroupids): 
    - String
  [RoleArn](#cfn-sagemaker-notebookinstance-rolearn): String
  [Tags](#cfn-sagemaker-notebookinstance-tags): 
    - [*Tag*](aws-properties-sagemaker-notebookinstance-tag.md)
```

## Properties<a name="aws-resource-sagemaker-notebookinstance-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-notebookinstance-kmskeyid"></a>
If you provide a AWS KMS key ID, Amazon SageMaker uses it to encrypt data at rest on the ML storage volume that is attached to your notebook instance\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DirectInternetAccess`  <a name="cfn-sagemaker-notebookinstance-directinternetaccess"></a>
Sets whether Amazon SageMaker provides internet access to the notebook instance\. If you set this to Disabled this notebook instance will be able to access resources only in your VPC, and will not be able to connect to Amazon SageMaker training and endpoint services unless your configure a NAT Gateway in your VPC\. For more information, see [Notebook Instances Are Enabled with Internet Access by Default](sagemaker/latest/dg/appendix-additional-considerations.html#appendix-notebook-and-internet-access)\. You can set the value of this parameter to Disabled only if you set a value for the SubnetId parameter\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubnetId`  <a name="cfn-sagemaker-notebookinstance-subnetid"></a>
The ID of the subnet in a VPC to which you would like to have a connectivity from your ML compute instance\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`NotebookInstanceName`  <a name="cfn-sagemaker-notebookinstance-notebookinstancename"></a>
The name of the notebook instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceType`  <a name="cfn-sagemaker-notebookinstance-instancetype"></a>
The type of ML compute instance to launch for the notebook instance\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LifecycleConfigName`  <a name="cfn-sagemaker-notebookinstance-lifecycleconfigname"></a>
The name of a lifecycle configuration to associate with the notebook instance\. For information about lifestyle configurations, see [Customize a Notebook Instance](http://docs.aws.amazon.com/sagemaker/latest/dg/notebook-lifecycle-config.html) in the *Amazon SageMaker Developer Guide*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SecurityGroupIds`  <a name="cfn-sagemaker-notebookinstance-securitygroupids"></a>
The VPC security group IDs, in the form sg\-xxxxxxxx\. The security groups must be for the same VPC as specified in the subnet\.  
 *Required*: No  
 *Type*: List of Strings  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RoleArn`  <a name="cfn-sagemaker-notebookinstance-rolearn"></a>
When you send any requests to AWS resources from the notebook instance, Amazon SageMaker assumes this role to perform tasks on your behalf\. You must grant this role necessary permissions so Amazon SageMaker can perform these tasks\. The policy must allow the Amazon SageMaker service principal \(sagemaker\.amazonaws\.com\) permissions to assume this role\. For more information, see [Amazon SageMaker Roles](http://docs.aws.amazon.com/sagemaker/latest/dg/sagemaker-roles.html)\.  
 *Required*: Yes  
 *Type*:   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-sagemaker-notebookinstance-tags"></a>
A list of tags to associate with the notebook instance\.  
 *Required*: No  
 *Type*: List of [Amazon SageMaker NotebookInstance Tag](aws-properties-sagemaker-notebookinstance-tag.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-sagemaker-notebookinstance-returnvalues"></a>

### Ref<a name="aws-resource-sagemaker-notebookinstance-ref"></a>

When you pass the logical ID of an `AWS::SageMaker::NotebookInstance` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the notebook instance, such as `arn:aws:sagemaker:us-west-2:012345678901:notebook-instance/mynotebookinstance`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-sagemaker-notebookinstance-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`NotebookInstanceName`  
The name of the notebook instance, such as `MyNotebookInstance`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-sagemaker-notebookinstance-examples"></a>

### SageMaker Notebook Instance Example<a name="aws-resource-sagemaker-notebookinstance-example1"></a>

The following example creates a notebook instance\.

#### JSON<a name="aws-resource-sagemaker-notebookinstance-example1.json"></a>

```
{
  "Description": "Basic NotebookInstance test update to a different instance type",
  "Resources": {
    "BasicNotebookInstance": {
      "Type": "AWS::SageMaker::NotebookInstance",
      "Properties": {
        "InstanceType": "ml.t2.large",
        "RoleArn": { "Fn::GetAtt" : [ "ExecutionRole", "Arn" ] }
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
       }
  },
  
}
```

#### YAML<a name="aws-resource-sagemaker-notebookinstance-example1.yaml"></a>

```
Description: "Basic NotebookInstance test update to a different instance type"
Resources:
  BasicNotebookInstance:
    Type: "AWS::SageMaker::NotebookInstance"
    Properties:
      InstanceType: "ml.t2.large"
      RoleArn: !GetAtt ExecutionRole.Arn
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
```