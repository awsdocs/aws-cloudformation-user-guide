# AWS::OpsWorks::Layer<a name="aws-resource-opsworks-layer"></a>

Creates a layer\. For more information, see [How to Create a Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinglayers-basics-create.html)\.

**Note**  
You should use **CreateLayer** for noncustom layer types such as PHP App Server only if the stack does not have an existing layer of that type\. A stack can have at most one instance of each noncustom layer; if you attempt to create a second instance, **CreateLayer** fails\. A stack can have an arbitrary number of custom layers, so you can call **CreateLayer** as many times as you like for that layer type\.

 **Required Permissions**: To use this action, an IAM user must have a Manage permissions level for the stack, or an attached policy that explicitly grants permissions\. For more information on user permissions, see [Managing User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/opsworks-security-users.html)\.

## Syntax<a name="aws-resource-opsworks-layer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-layer-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::Layer",
  "Properties" : {
      "[Attributes](#cfn-opsworks-layer-attributes)" : {Key : Value, ...},
      "[AutoAssignElasticIps](#cfn-opsworks-layer-autoassignelasticips)" : Boolean,
      "[AutoAssignPublicIps](#cfn-opsworks-layer-autoassignpublicips)" : Boolean,
      "[CustomInstanceProfileArn](#cfn-opsworks-layer-custominstanceprofilearn)" : String,
      "[CustomJson](#cfn-opsworks-layer-customjson)" : Json,
      "[CustomRecipes](#cfn-opsworks-layer-customrecipes)" : Recipes,
      "[CustomSecurityGroupIds](#cfn-opsworks-layer-customsecuritygroupids)" : [ String, ... ],
      "[EnableAutoHealing](#cfn-opsworks-layer-enableautohealing)" : Boolean,
      "[InstallUpdatesOnBoot](#cfn-opsworks-layer-installupdatesonboot)" : Boolean,
      "[LifecycleEventConfiguration](#cfn-opsworks-layer-lifecycleeventconfiguration)" : LifecycleEventConfiguration,
      "[LoadBasedAutoScaling](#cfn-opsworks-layer-loadbasedautoscaling)" : LoadBasedAutoScaling,
      "[Name](#cfn-opsworks-layer-name)" : String,
      "[Packages](#cfn-opsworks-layer-packages)" : [ String, ... ],
      "[Shortname](#cfn-opsworks-layer-shortname)" : String,
      "[StackId](#cfn-opsworks-layer-stackid)" : String,
      "[Tags](#cfn-opsworks-layer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-opsworks-layer-type)" : String,
      "[UseEbsOptimizedInstances](#cfn-opsworks-layer-useebsoptimizedinstances)" : Boolean,
      "[VolumeConfigurations](#cfn-opsworks-layer-volumeconfigurations)" : [ VolumeConfiguration, ... ]
    }
}
```

### YAML<a name="aws-resource-opsworks-layer-syntax.yaml"></a>

```
Type: AWS::OpsWorks::Layer
Properties: 
  [Attributes](#cfn-opsworks-layer-attributes): 
    Key : Value
  [AutoAssignElasticIps](#cfn-opsworks-layer-autoassignelasticips): Boolean
  [AutoAssignPublicIps](#cfn-opsworks-layer-autoassignpublicips): Boolean
  [CustomInstanceProfileArn](#cfn-opsworks-layer-custominstanceprofilearn): String
  [CustomJson](#cfn-opsworks-layer-customjson): 
    Json
  [CustomRecipes](#cfn-opsworks-layer-customrecipes): 
    Recipes
  [CustomSecurityGroupIds](#cfn-opsworks-layer-customsecuritygroupids): 
    - String
  [EnableAutoHealing](#cfn-opsworks-layer-enableautohealing): Boolean
  [InstallUpdatesOnBoot](#cfn-opsworks-layer-installupdatesonboot): Boolean
  [LifecycleEventConfiguration](#cfn-opsworks-layer-lifecycleeventconfiguration): 
    LifecycleEventConfiguration
  [LoadBasedAutoScaling](#cfn-opsworks-layer-loadbasedautoscaling): 
    LoadBasedAutoScaling
  [Name](#cfn-opsworks-layer-name): String
  [Packages](#cfn-opsworks-layer-packages): 
    - String
  [Shortname](#cfn-opsworks-layer-shortname): String
  [StackId](#cfn-opsworks-layer-stackid): String
  [Tags](#cfn-opsworks-layer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-opsworks-layer-type): String
  [UseEbsOptimizedInstances](#cfn-opsworks-layer-useebsoptimizedinstances): Boolean
  [VolumeConfigurations](#cfn-opsworks-layer-volumeconfigurations): 
    - VolumeConfiguration
```

## Properties<a name="aws-resource-opsworks-layer-properties"></a>

`Attributes`  <a name="cfn-opsworks-layer-attributes"></a>
One or more user\-defined key\-value pairs to be added to the stack attributes\.  
To create a cluster layer, set the `EcsClusterArn` attribute to the cluster's ARN\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoAssignElasticIps`  <a name="cfn-opsworks-layer-autoassignelasticips"></a>
Whether to automatically assign an [Elastic IP address](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html) to the layer's instances\. For more information, see [How to Edit a Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinglayers-basics-edit.html)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoAssignPublicIps`  <a name="cfn-opsworks-layer-autoassignpublicips"></a>
For stacks that are running in a VPC, whether to automatically assign a public IP address to the layer's instances\. For more information, see [How to Edit a Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinglayers-basics-edit.html)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomInstanceProfileArn`  <a name="cfn-opsworks-layer-custominstanceprofilearn"></a>
The ARN of an IAM profile to be used for the layer's EC2 instances\. For more information about IAM ARNs, see [Using Identifiers](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_Identifiers.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomJson`  <a name="cfn-opsworks-layer-customjson"></a>
A JSON\-formatted string containing custom stack configuration and deployment attributes to be installed on the layer's instances\. For more information, see [ Using Custom JSON](https://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook-json-override.html)\. This feature is supported as of version 1\.7\.42 of the AWS CLI\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomRecipes`  <a name="cfn-opsworks-layer-customrecipes"></a>
A `LayerCustomRecipes` object that specifies the layer custom recipes\.  
*Required*: No  
*Type*: [Recipes](aws-properties-opsworks-layer-recipes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomSecurityGroupIds`  <a name="cfn-opsworks-layer-customsecuritygroupids"></a>
An array containing the layer custom security group IDs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAutoHealing`  <a name="cfn-opsworks-layer-enableautohealing"></a>
Whether to disable auto healing for the layer\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstallUpdatesOnBoot`  <a name="cfn-opsworks-layer-installupdatesonboot"></a>
Whether to install operating system and package updates when the instance boots\. The default value is `true`\. To control when updates are installed, set this value to `false`\. You must then update your instances manually by using [CreateDeployment](https://docs.aws.amazon.com/goto/WebAPI/opsworks-2013-02-18/CreateDeployment) to run the `update_dependencies` stack command or by manually running `yum` \(Amazon Linux\) or `apt-get` \(Ubuntu\) on the instances\.   
To ensure that your instances have the latest security updates, we strongly recommend using the default value of `true`\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleEventConfiguration`  <a name="cfn-opsworks-layer-lifecycleeventconfiguration"></a>
A `LifeCycleEventConfiguration` object that you can use to configure the Shutdown event to specify an execution timeout and enable or disable Elastic Load Balancer connection draining\.  
*Required*: No  
*Type*: [LifecycleEventConfiguration](aws-properties-opsworks-layer-lifecycleeventconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBasedAutoScaling`  <a name="cfn-opsworks-layer-loadbasedautoscaling"></a>
The load\-based scaling configuration for the AWS OpsWorks layer\.  
*Required*: No  
*Type*: [LoadBasedAutoScaling](aws-properties-opsworks-layer-loadbasedautoscaling.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opsworks-layer-name"></a>
The layer name, which is used by the console\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Packages`  <a name="cfn-opsworks-layer-packages"></a>
An array of `Package` objects that describes the layer packages\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Shortname`  <a name="cfn-opsworks-layer-shortname"></a>
For custom layers only, use this parameter to specify the layer's short name, which is used internally by AWS OpsWorks Stacks and by Chef recipes\. The short name is also used as the name for the directory where your app files are installed\. It can have a maximum of 200 characters, which are limited to the alphanumeric characters, '\-', '\_', and '\.'\.  
The built\-in layers' short names are defined by AWS OpsWorks Stacks\. For more information, see the [Layer Reference](https://docs.aws.amazon.com/opsworks/latest/userguide/layers.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackId`  <a name="cfn-opsworks-layer-stackid"></a>
The layer stack ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-opsworks-layer-tags"></a>
Specifies one or more sets of tags \(key–value pairs\) to associate with this AWS OpsWorks layer\. Use tags to manage your resources\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opsworks-layer-type"></a>
The layer type\. A stack cannot have more than one built\-in layer of the same type\. It can have any number of custom layers\. Built\-in layers are not available in Chef 12 stacks\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `aws-flow-ruby | custom | db-master | ecs-cluster | java-app | lb | memcached | monitoring-master | nodejs-app | php-app | rails-app | web`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UseEbsOptimizedInstances`  <a name="cfn-opsworks-layer-useebsoptimizedinstances"></a>
Whether to use Amazon EBS\-optimized instances\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeConfigurations`  <a name="cfn-opsworks-layer-volumeconfigurations"></a>
A `VolumeConfigurations` object that describes the layer's Amazon EBS volumes\.  
*Required*: No  
*Type*: List of [VolumeConfiguration](aws-properties-opsworks-layer-volumeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-opsworks-layer-return-values"></a>

### Ref<a name="aws-resource-opsworks-layer-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myLayer" }` 

For the AWS OpsWorks layer *myLayer*, `Ref` returns the AWS OpsWorks layer ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-opsworks-layer--examples"></a>

### AWS OpsWorks PHP Layer<a name="aws-resource-opsworks-layer--examples--AWS_OpsWorks_PHP_Layer"></a>

The following snippet creates an AWS OpsWorks PHP layer that is associated with the `myStack` AWS OpsWorks stack\. The layer is dependent on the `myApp` AWS OpsWorks application\.

#### JSON<a name="aws-resource-opsworks-layer--examples--AWS_OpsWorks_PHP_Layer--json"></a>

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

#### YAML<a name="aws-resource-opsworks-layer--examples--AWS_OpsWorks_PHP_Layer--yaml"></a>

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

### Load\-based Auto Scaling Layer<a name="aws-resource-opsworks-layer--examples--Load-based_Auto_Scaling_Layer"></a>

The following snippet creates a load\-based automatic scaling AWS OpsWorks PHP layer that is associated with the `myStack` AWS OpsWorks stack\.

#### JSON<a name="aws-resource-opsworks-layer--examples--Load-based_Auto_Scaling_Layer--json"></a>

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

#### YAML<a name="aws-resource-opsworks-layer--examples--Load-based_Auto_Scaling_Layer--yaml"></a>

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

### Specify tags for layers and stacks<a name="aws-resource-opsworks-layer--examples--Specify_tags_for_layers_and_stacks"></a>

The following complete template example specifies tags for an AWS OpsWorks layer and stack that reference parameter values\.

#### JSON<a name="aws-resource-opsworks-layer--examples--Specify_tags_for_layers_and_stacks--json"></a>

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

#### YAML<a name="aws-resource-opsworks-layer--examples--Specify_tags_for_layers_and_stacks--yaml"></a>

```
Resources:
  ServiceRole:
    Type: AWS::IAM::Role
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
    Type: AWS::IAM::Role
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
    Type: AWS::IAM::InstanceProfile
    Properties:
      Path: /
      Roles:
        - !Ref OpsWorksEC2Role
  myStack:
    Type: AWS::OpsWorks::Stack
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
    Type: AWS::OpsWorks::Layer
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

## See also<a name="aws-resource-opsworks-layer--seealso"></a>
+  [CreateLayer](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateLayer.html) in the *AWS OpsWorks API Reference*\.
+  [Creating an OpsWorks Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/workinglayers-basics-create.html) in the *AWS OpsWorks User Guide*\.

