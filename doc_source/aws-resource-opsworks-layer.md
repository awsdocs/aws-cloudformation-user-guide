# AWS::OpsWorks::Layer<a name="aws-resource-opsworks-layer"></a>

Creates an AWS OpsWorks layer\. A layer defines, for example, which packages and applications are installed and how they are configured\.

**Topics**
+ [Syntax](#aws-resource-opsworks-layer-syntax)
+ [Properties](#w3ab2c21c10d926b9)
+ [Return Values](#w3ab2c21c10d926c11)
+ [Template Examples](#w3ab2c21c10d926c13)
+ [See Also](#w3ab2c21c10d926c15)

## Syntax<a name="aws-resource-opsworks-layer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-layer-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::Layer",
  "Properties": {
    "[Attributes](#cfn-opsworks-layer-attributes)" : { String:String },
    "[AutoAssignElasticIps](#cfn-opsworks-layer-autoassignelasticips)" : Boolean,
    "[AutoAssignPublicIps](#cfn-opsworks-layer-autoassignpublicips)" : Boolean,
    "[CustomInstanceProfileArn](#cfn-opsworks-layer-custinstanceprofilearn)" : String,
    "[CustomJson](#cfn-opsworks-layer-customjson)" : JSON object,
    "[CustomRecipes](#cfn-opsworks-layer-customrecipes)" : Recipes,
    "[CustomSecurityGroupIds](#cfn-opsworks-layer-custsecuritygroupnids)" :  [ String, ... ],
    "[EnableAutoHealing](#cfn-opsworks-layer-enableautohealing)" : Boolean,
    "[InstallUpdatesOnBoot](#cfn-opsworks-layer-installupdatesonboot)" : Boolean,
    "[LifecycleEventConfiguration](#cfn-opsworks-layer-lifecycleeventconfiguration)" : LifeCycleEventConfiguration,
    "[LoadBasedAutoScaling](#cfn-opsworks-layer-loadbasedautoscaling)" : LoadBasedAutoScaling,
    "[Name](#cfn-opsworks-layer-name)" : String,
    "[Packages](#cfn-opsworks-layer-packages)" : [ String, ... ],
    "[Shortname](#cfn-opsworks-layer-shortname)" : String,
    "[StackId](#cfn-opsworks-layer-stackid)" : String,
    "[Tags](#cfn-opsworks-layer-tags)" : [ [Tags](aws-properties-resource-tags.md), ... ],
    "[Type](#cfn-opsworks-layer-type)" : String,
    "[VolumeConfigurations](#cfn-opsworks-layer-volconfig)" : [ VolumeConfiguration, ... ]
  }
}
```

### YAML<a name="aws-resource-opsworks-layer-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::Layer"
Properties:
  [Attributes](#cfn-opsworks-layer-attributes):
    String:String
  [AutoAssignElasticIps](#cfn-opsworks-layer-autoassignelasticips): Boolean
  [AutoAssignPublicIps](#cfn-opsworks-layer-autoassignpublicips): Boolean
  [CustomInstanceProfileArn](#cfn-opsworks-layer-custinstanceprofilearn): String
  [CustomRecipes](#cfn-opsworks-layer-customrecipes):
    Recipes
  [CustomJson](#cfn-opsworks-layer-customjson):
    JSON object
  [CustomSecurityGroupIds](#cfn-opsworks-layer-custsecuritygroupnids):
    - String
  [EnableAutoHealing](#cfn-opsworks-layer-enableautohealing): Boolean
  [InstallUpdatesOnBoot](#cfn-opsworks-layer-installupdatesonboot): Boolean
  [LifecycleEventConfiguration](#cfn-opsworks-layer-lifecycleeventconfiguration):
    LifeCycleEventConfiguration
  [LoadBasedAutoScaling](#cfn-opsworks-layer-loadbasedautoscaling):
    LoadBasedAutoScaling
  [Name](#cfn-opsworks-layer-name): String
  [Packages](#cfn-opsworks-layer-packages):
    - String
  [Shortname](#cfn-opsworks-layer-shortname): String
  [StackId](#cfn-opsworks-layer-stackid): String
  [Tags](#cfn-opsworks-layer-tags): 
  - [Tags](aws-properties-resource-tags.md) 
  [Type](#cfn-opsworks-layer-type): String
  [VolumeConfigurations](#cfn-opsworks-layer-volconfig):
    - VolumeConfiguration
```

## Properties<a name="w3ab2c21c10d926b9"></a>

`Attributes`  <a name="cfn-opsworks-layer-attributes"></a>
One or more user\-defined key\-value pairs to be added to the stack attributes bag\.  
*Required*: No  
*Type*: A list of key\-value pairs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoAssignElasticIps`  <a name="cfn-opsworks-layer-autoassignelasticips"></a>
Whether to automatically assign an Elastic IP address to Amazon EC2 instances in this layer\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoAssignPublicIps`  <a name="cfn-opsworks-layer-autoassignpublicips"></a>
For AWS OpsWorks stacks that are running in a VPC, whether to automatically assign a public IP address to Amazon EC2 instances in this layer\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CustomInstanceProfileArn`  <a name="cfn-opsworks-layer-custinstanceprofilearn"></a>
The Amazon Resource Name \(ARN\) of an IAM instance profile that is to be used for the Amazon EC2 instances in this layer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CustomJson`  <a name="cfn-opsworks-layer-customjson"></a>
A custom stack configuration and deployment attributes that AWS OpsWorks installs on the layer's instances\. For more information, see the `CustomJson` parameter for the [CreateLayer](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateLayer.html) action in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: JSON object

`CustomRecipes`  <a name="cfn-opsworks-layer-customrecipes"></a>
Custom event recipes for this layer\.  
*Required*: No  
*Type*: [AWS OpsWorks Recipes Type](aws-properties-opsworks-layer-recipes.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CustomSecurityGroupIds`  <a name="cfn-opsworks-layer-custsecuritygroupnids"></a>
Custom security group IDs for this layer\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EnableAutoHealing`  <a name="cfn-opsworks-layer-enableautohealing"></a>
Whether to automatically heal Amazon EC2 instances that have become disconnected or timed out\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstallUpdatesOnBoot`  <a name="cfn-opsworks-layer-installupdatesonboot"></a>
Whether to install operating system and package updates when the instance boots\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LifecycleEventConfiguration`  <a name="cfn-opsworks-layer-lifecycleeventconfiguration"></a>
The lifecycle events for the AWS OpsWorks layer\.  
*Required*: No  
*Type*: [AWS OpsWorks Layer LifeCycleConfiguration](aws-properties-opsworks-layer-lifecycleeventconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoadBasedAutoScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling"></a>
The load\-based scaling configuration for the AWS OpsWorks layer\.  
*Required*: No  
*Type*: [AWS OpsWorks LoadBasedAutoScaling Type](aws-properties-opsworks-layer-loadbasedautoscaling.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-opsworks-layer-name"></a>
The AWS OpsWorks layer name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Packages`  <a name="cfn-opsworks-layer-packages"></a>
The packages for this layer\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Shortname`  <a name="cfn-opsworks-layer-shortname"></a>
The layer short name, which is used internally by AWS OpsWorks and by Chef recipes\. The short name is also used as the name for the directory where your app files are installed\.   
The name can have a maximum of 200 characters, which are limited to the alphanumeric characters, '\-', '\_', and '\.'\.  
If you update a property that requires the layer to be replaced, you must specify a new short name\. You cannot have multiple layers with the same short name\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StackId`  <a name="cfn-opsworks-layer-stackid"></a>
The ID of the AWS OpsWorks stack that this layer will be associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-opsworks-layer-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this AWS OpsWorks layer\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-opsworks-layer-type"></a>
The layer type\. A stack cannot have more than one layer of the same type, except for the `custom` type\. You can have any number of `custom` types\. For more information, see [CreateLayer](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateLayer.html) in the *AWS OpsWorks Stacks API Reference*\.  
If you update a property that requires the layer to be replaced, you must specify a new type unless you have a `custom` type\. You can have any number of `custom` types\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VolumeConfigurations`  <a name="cfn-opsworks-layer-volconfig"></a>
Describes the Amazon EBS volumes for this layer\.  
*Required*: No  
*Type*: A list of [AWS OpsWorks VolumeConfiguration Type](aws-properties-opsworks-layer-volumeconfig.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

## Return Values<a name="w3ab2c21c10d926c11"></a>

### Ref<a name="w3ab2c21c10d926c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myLayer" }
```

For the AWS OpsWorks layer `myLayer`, `Ref` returns the AWS OpsWorks layer ID\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Examples<a name="w3ab2c21c10d926c13"></a>

### AWS OpsWorks PHP Layer<a name="w3ab2c21c10d926c13b2"></a>

The following snippet creates an AWS OpsWorks PHP layer that is associated with the `myStack` AWS OpsWorks stack\. The layer is dependent on the `myApp` AWS OpsWorks application\.

#### JSON<a name="aws-resource-opsworks-layer-example1.json"></a>

```
"myLayer": {
  "Type": "AWS::OpsWorks::Layer",
  "DependsOn": "myApp",
  "Properties": {
    "StackId": {"Ref": "myStack"},
    "Type": "php-app",
    "Shortname" : "php-app",
    "EnableAutoHealing" : "true",
    "AutoAssignElasticIps" : "false",
    "AutoAssignPublicIps" : "true",
    "Name": "MyPHPApp"
  }
}
```

#### YAML<a name="aws-resource-opsworks-layer-example1.yaml"></a>

```
myLayer: 
  Type: "AWS::OpsWorks::Layer"
  DependsOn: "myApp"
  Properties: 
    StackId: 
      Ref: "myStack"
    Type: "php-app"
    Shortname: "php-app"
    EnableAutoHealing: "true"
    AutoAssignElasticIps: "false"
    AutoAssignPublicIps: "true"
    Name: "MyPHPApp"
```

### Load\-based Auto Scaling Layer<a name="w3ab2c21c10d926c13b4"></a>

The following snippet creates a load\-based automatic scaling AWS OpsWorks PHP layer that is associated with the `myStack` AWS OpsWorks stack\.

#### JSON<a name="aws-resource-opsworks-layer-example2.json"></a>

```
"myLayer": {
  "Type": "AWS::OpsWorks::Layer",
  "DependsOn": "myApp",
  "Properties": {
    "StackId": {"Ref": "myStack"},
    "Type": "php-app",
    "Shortname" : "php-app",
    "EnableAutoHealing" : "true",
    "AutoAssignElasticIps" : "false",
    "AutoAssignPublicIps" : "true",
    "Name": "MyPHPApp",
    "LoadBasedAutoScaling" : {
      "Enable" : "true",
      "UpScaling" : {
        "InstanceCount" : 1,
        "ThresholdsWaitTime" : 1,
        "IgnoreMetricsTime" : 1,
        "CpuThreshold" : 70.0,
        "MemoryThreshold" : 30.0,
        "LoadThreshold" : 0.7
      },
      "DownScaling" : {
        "InstanceCount" : 1,
        "ThresholdsWaitTime" : 1,
        "IgnoreMetricsTime" : 1,
        "CpuThreshold" : 30.0,
        "MemoryThreshold" : 70.0,
        "LoadThreshold" : 0.3
      }
    }
  }
}
```

#### YAML<a name="aws-resource-opsworks-layer-example2.yaml"></a>

```
myLayer: 
  Type: "AWS::OpsWorks::Layer"
  DependsOn: "myApp"
  Properties: 
    StackId: 
      Ref: "myStack"
    Type: "php-app"
    Shortname: "php-app"
    EnableAutoHealing: "true"
    AutoAssignElasticIps: "false"
    AutoAssignPublicIps: "true"
    Name: "MyPHPApp"
    LoadBasedAutoScaling: 
      Enable: "true"
      UpScaling: 
        InstanceCount: 1
        ThresholdsWaitTime: 1
        IgnoreMetricsTime: 1
        CpuThreshold: 70
        MemoryThreshold: 30
        LoadThreshold: 0.7
      DownScaling: 
        InstanceCount: 1
        ThresholdsWaitTime: 1
        IgnoreMetricsTime: 1
        CpuThreshold: 30
        MemoryThreshold: 70
        LoadThreshold: 0.3
```

### Specify tags for layers and stacks<a name="aws-resource-opsworks-layer-example3"></a>

The following complete template example specifies tags for an AWS OpsWorks layer and stack that reference parameter values\.

#### JSON<a name="aws-resource-opsworks-layer-example3.json"></a>

```
{
    "Resources": {
        "ServiceRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    {
                                        "Ref": "OpsServicePrincipal"
                                    }
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
                        "PolicyName": "opsworks-service",
                        "PolicyDocument": {
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": [
                                        "ec2:*",
                                        "iam:PassRole",
                                        "cloudwatch:GetMetricStatistics",
                                        "elasticloadbalancing:*"
                                    ],
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "OpsWorksEC2Role": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    {
                                        "Ref": "Ec2ServicePrincipal"
                                    }
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/"
            }
        },
        "InstanceRole": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Path": "/",
                "Roles": [
                    {
                        "Ref": "OpsWorksEC2Role"
                    }
                ]
            }
        },
        "myStack": {
            "Type": "AWS::OpsWorks::Stack",
            "Properties": {
                "Name": "TestStack",
                "ServiceRoleArn": {
                    "Fn::GetAtt": [
                        "ServiceRole",
                        "Arn"
                    ]
                },
                "DefaultInstanceProfileArn": {
                    "Fn::GetAtt": [
                        "InstanceRole",
                        "Arn"
                    ]
                },
                "Tags": [
                    {
                        "Key": {
                            "Ref": "StackKey"
                        },
                        "Value": {
                            "Ref": "StackValue"
                        }
                    }
                ]
            }
        },
        "myLayer": {
            "Type": "AWS::OpsWorks::Layer",
            "Properties": {
                "EnableAutoHealing": "true",
                "AutoAssignElasticIps": "false",
                "AutoAssignPublicIps": "true",
                "StackId": {
                    "Ref": "myStack"
                },
                "Type": "custom",
                "Shortname": "shortname",
                "Name": "name",
                "Tags": [
                    {
                        "Key": {
                            "Ref": "LayerKey"
                        },
                        "Value": {
                            "Ref": "LayerValue"
                        }
                    }
                ]
            }
        }
    },
    "Parameters": {
        "StackKey": {
            "Type": "String"
        },
        "LayerKey": {
            "Type": "String"
        },
        "StackValue": {
            "Type": "String"
        },
        "LayerValue": {
            "Type": "String"
        },
        "OpsServicePrincipal": {
            "Type": "String"
        },
        "Ec2ServicePrincipal": {
            "Type": "String"
        }
    }
}
```

#### YAML<a name="aws-resource-opsworks-layer-example3.yaml"></a>

```
Resources:
  ServiceRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - !Ref OpsServicePrincipal
            Action:
              - 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: opsworks-service
          PolicyDocument:
            Statement:
              - Effect: Allow
                Action:
                  - 'ec2:*'
                  - 'iam:PassRole'
                  - 'cloudwatch:GetMetricStatistics'
                  - 'elasticloadbalancing:*'
                Resource: '*'
  OpsWorksEC2Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - !Ref Ec2ServicePrincipal
            Action:
              - 'sts:AssumeRole'
      Path: /
  InstanceRole:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref OpsWorksEC2Role
  myStack:
    Type: 'AWS::OpsWorks::Stack'
    Properties:
      Name: TestStack
      ServiceRoleArn: !GetAtt 
        - ServiceRole
        - Arn
      DefaultInstanceProfileArn: !GetAtt 
        - InstanceRole
        - Arn
      Tags:
        - Key: !Ref StackKey
          Value: !Ref StackValue
  myLayer:
    Type: 'AWS::OpsWorks::Layer'
    Properties:
      EnableAutoHealing: 'true'
      AutoAssignElasticIps: 'false'
      AutoAssignPublicIps: 'true'
      StackId: !Ref myStack
      Type: custom
      Shortname: shortname
      Name: name
      Tags:
        - Key: !Ref LayerKey
          Value: !Ref LayerValue
Parameters:
  StackKey:
    Type: String
  LayerKey:
    Type: String
  StackValue:
    Type: String
  LayerValue:
    Type: String
  OpsServicePrincipal:
    Type: String
  Ec2ServicePrincipal:
    Type: String
```

## See Also<a name="w3ab2c21c10d926c15"></a>
+ [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)
+ [AWS::OpsWorks::App](aws-resource-opsworks-app.md)
+ [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)