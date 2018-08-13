# AWS::OpsWorks::Stack<a name="aws-resource-opsworks-stack"></a>

Creates an AWS OpsWorks stack\. An AWS OpsWorks stack represents a set of instances that you want to manage collectively, typically because they have a common purpose such as serving PHP applications\.

**Topics**
+ [Syntax](#aws-resource-opsworks-stack-syntax)
+ [Properties](#w3ab2c21c10d935b9)
+ [Return Values](#w3ab2c21c10d935c11)
+ [Template Examples](#w3ab2c21c10d935c13)
+ [Additional Information](#w3ab2c21c10d935c15)

## Syntax<a name="aws-resource-opsworks-stack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-stack-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::Stack",
  "Properties" : {
    "[AgentVersion](#cfn-opsworks-stack-agentversion)" : String,
    "[Attributes](#cfn-opsworks-stack-attributes)" : { String:String, ... },
    "[ChefConfiguration](#cfn-opsworks-stack-chefconfiguration)" : { ChefConfiguration },
    "[CloneAppIds](#cfn-opsworks-stack-cloneappids)" : [ String, ... ],
    "[ClonePermissions](#cfn-opsworks-stack-clonepermissions)" : Boolean,
    "[ConfigurationManager](#cfn-opsworks-stack-configmanager)" : { StackConfigurationManager },
    "[CustomCookbooksSource](#cfn-opsworks-stack-custcookbooksource)" : { Source },
    "[CustomJson](#cfn-opsworks-stack-custjson)" : JSON,
    "[DefaultAvailabilityZone](#cfn-opsworks-stack-defaultaz)" : String,
    "[DefaultInstanceProfileArn](#cfn-opsworks-stack-defaultinstanceprof)" : String,
    "[DefaultOs](#cfn-opsworks-stack-defaultos)" : String,
    "[DefaultRootDeviceType](#cfn-opsworks-stack-defaultrootdevicetype)" : String,
    "[DefaultSshKeyName](#cfn-opsworks-stack-defaultsshkeyname)" : String,
    "[DefaultSubnetId](#cfn-opsworks-stack-defaultsubnet)" : String,
    "[EcsClusterArn](#cfn-opsworks-stack-ecsclusterarn)" : String,
    "[ElasticIps](#cfn-opsworks-stack-elasticips)" : [ [ElasticIp](aws-properties-opsworks-stack-elasticip.md), ... ],
    "[HostnameTheme](#cfn-opsworks-stack-hostnametheme)" : String,
    "[Name](#cfn-opsworks-stack-name)" : String,
    "[RdsDbInstances](#cfn-opsworks-stack-rdsdbinstances)" : [ [RdsDbInstance](aws-properties-opsworks-stack-rdsdbinstance.md), ... ],
    "[ServiceRoleArn](#cfn-opsworks-stack-servicerolearn)" : String,
    "[SourceStackId](#cfn-opsworks-stack-sourcestackid)" : String,
    "[Tags](#cfn-opsworks-stack-tags)" : [ [Tags](aws-properties-resource-tags.md), ... ], 
    "[UseCustomCookbooks](#cfn-opsworks-stack-usecustcookbooks)" : Boolean,
    "[UseOpsworksSecurityGroups](#cfn-opsworks-stack-useopsworkssecuritygroups)" : Boolean,
    "[VpcId](#cfn-opsworks-stack-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-stack-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::Stack"
Properties: 
  [AgentVersion](#cfn-opsworks-stack-agentversion): String
  [Attributes](#cfn-opsworks-stack-attributes):
    String:String
  [ChefConfiguration](#cfn-opsworks-stack-chefconfiguration):
    ChefConfiguration
  [CloneAppIds](#cfn-opsworks-stack-cloneappids): 
  - String
  [ClonePermissions](#cfn-opsworks-stack-clonepermissions): Boolean
  [ConfigurationManager](#cfn-opsworks-stack-configmanager):
    StackConfigurationManager
  [CustomCookbooksSource](#cfn-opsworks-stack-custcookbooksource):
    Source
  [CustomJson](#cfn-opsworks-stack-custjson): JSON
  [DefaultAvailabilityZone](#cfn-opsworks-stack-defaultaz): String
  [DefaultInstanceProfileArn](#cfn-opsworks-stack-defaultinstanceprof): String
  [DefaultOs](#cfn-opsworks-stack-defaultos): String
  [DefaultRootDeviceType](#cfn-opsworks-stack-defaultrootdevicetype): String
  [DefaultSshKeyName](#cfn-opsworks-stack-defaultsshkeyname): String
  [DefaultSubnetId](#cfn-opsworks-stack-defaultsubnet): String
  [EcsClusterArn](#cfn-opsworks-stack-ecsclusterarn): String
  [ElasticIps](#cfn-opsworks-stack-elasticips): 
  - [ElasticIp](aws-properties-opsworks-stack-elasticip.md)
  [HostnameTheme](#cfn-opsworks-stack-hostnametheme): String
  [Name](#cfn-opsworks-stack-name): String
  [RdsDbInstances](#cfn-opsworks-stack-rdsdbinstances): 
  - [RdsDbInstance](aws-properties-opsworks-stack-rdsdbinstance.md)
  [ServiceRoleArn](#cfn-opsworks-stack-servicerolearn): String
  [SourceStackId](#cfn-opsworks-stack-sourcestackid): String
  [Tags](#cfn-opsworks-stack-tags): 
  - [Tags](aws-properties-resource-tags.md)
  [UseCustomCookbooks](#cfn-opsworks-stack-usecustcookbooks): Boolean
  [UseOpsworksSecurityGroups](#cfn-opsworks-stack-useopsworkssecuritygroups): Boolean
  [VpcId](#cfn-opsworks-stack-vpcid): String
```

## Properties<a name="w3ab2c21c10d935b9"></a>

`AgentVersion`  <a name="cfn-opsworks-stack-agentversion"></a>
The AWS OpsWorks agent version that you want to use\. The agent communicates with the service and handles tasks such as initiating Chef runs in response to lifecycle events\. For valid values, see the [AgentVersion](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html#opsworks-CreateStack-request-AgentVersion) parameter for the `CreateStack` action in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Attributes`  <a name="cfn-opsworks-stack-attributes"></a>
One or more user\-defined key\-value pairs to be added to the stack attributes bag\.  
*Required*: No  
*Type*: A list of key\-value pairs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ChefConfiguration`  <a name="cfn-opsworks-stack-chefconfiguration"></a>
Describes the Chef configuration\. For more information, see the [CreateStack ChefConfiguration](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html#opsworks-CreateStack-request-ChefConfiguration) parameter in the *AWS OpsWorks Stacks API Reference*\.  
To enable Berkshelf, you must select a Chef version in the `ConfigurationManager` property that supports Berkshelf\.
*Required*: No  
*Type*: [AWS OpsWorks ChefConfiguration Type](aws-properties-opsworks-stack-chefconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CloneAppIds`  <a name="cfn-opsworks-stack-cloneappids"></a>
If you're cloning an AWS OpsWorks stack, a list of AWS OpsWorks application stack IDs from the source stack to include in the cloned stack\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ClonePermissions`  <a name="cfn-opsworks-stack-clonepermissions"></a>
If you're cloning an AWS OpsWorks stack, indicates whether to clone the source stack's permissions\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ConfigurationManager`  <a name="cfn-opsworks-stack-configmanager"></a>
Describes the configuration manager\. When you create a stack, you use the configuration manager to specify the Chef version\. For supported Chef versions, see the [CreateStack ConfigurationManager](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html#opsworks-CreateStack-request-ConfigurationManager) parameter in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: [AWS OpsWorks StackConfigurationManager Type](aws-properties-opsworks-stack-stackconfigmanager.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CustomCookbooksSource`  <a name="cfn-opsworks-stack-custcookbooksource"></a>
Contains the information required to retrieve a cookbook from a repository\.  
*Required*: No  
*Type*: [AWS OpsWorks Source Type](aws-properties-opsworks-stack-source.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CustomJson`  <a name="cfn-opsworks-stack-custjson"></a>
A user\-defined custom JSON object\. The custom JSON is used to override the corresponding default stack configuration JSON values\. For more information, see [CreateStack](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html) in the *AWS OpsWorks Stacks API Reference*\.  
AWS CloudFormation submits all JSON attributes as strings, including any Boolean or number attributes\. If you have recipes that expect booleans or numbers, you must modify the recipes to accept strings and to interpret those strings as booleans or numbers\.
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultAvailabilityZone`  <a name="cfn-opsworks-stack-defaultaz"></a>
The stack's default Availability Zone, which must be in the specified region\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultInstanceProfileArn`  <a name="cfn-opsworks-stack-defaultinstanceprof"></a>
The Amazon Resource Name \(ARN\) of an IAM instance profile that is the default profile for all of the stack's Amazon EC2 instances\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultOs`  <a name="cfn-opsworks-stack-defaultos"></a>
The stack's default operating system\. For more information, see [CreateStack](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultRootDeviceType`  <a name="cfn-opsworks-stack-defaultrootdevicetype"></a>
The default root device type\. This value is used by default for all instances in the stack, but you can override it when you create an instance\. For more information, see [CreateStack](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultSshKeyName`  <a name="cfn-opsworks-stack-defaultsshkeyname"></a>
A default SSH key for the stack instances\. You can override this value when you create or update an instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DefaultSubnetId`  <a name="cfn-opsworks-stack-defaultsubnet"></a>
The stack's default subnet ID\. All instances are launched into this subnet unless you specify another subnet ID when you create the instance\.  
*Required*: Conditional\. If you specify the `VpcId` property, you must specify this property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EcsClusterArn`  <a name="cfn-opsworks-stack-ecsclusterarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Elastic Container Service \(Amazon ECS\) cluster to register with the AWS OpsWorks stack\.  
If you specify a cluster that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the cluster\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ElasticIps`  <a name="cfn-opsworks-stack-elasticips"></a>
A list of Elastic IP addresses to register with the AWS OpsWorks stack\.  
If you specify an IP address that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the IP address\.
*Required*: No  
*Type*: List of [AWS OpsWorks Stack ElasticIp](aws-properties-opsworks-stack-elasticip.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HostnameTheme`  <a name="cfn-opsworks-stack-hostnametheme"></a>
The stack's host name theme, with spaces replaced by underscores\. The theme is used to generate host names for the stack's instances\. For more information, see [CreateStack](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateStack.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-opsworks-stack-name"></a>
The name of the AWS OpsWorks stack\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RdsDbInstances`  <a name="cfn-opsworks-stack-rdsdbinstances"></a>
The Amazon Relational Database Service \(Amazon RDS\) DB instance to register with the AWS OpsWorks stack\.  
If you specify a DB instance that's registered with another AWS OpsWorks stack, AWS CloudFormation deregisters the existing association before registering the DB instance\.
*Required*: No  
*Type*: List of [AWS OpsWorks Stack RdsDbInstance](aws-properties-opsworks-stack-rdsdbinstance.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-opsworks-stack-servicerolearn"></a>
The AWS Identity and Access Management \(IAM\) role that AWS OpsWorks uses to work with AWS resources on your behalf\. You must specify an Amazon Resource Name \(ARN\) for an existing IAM role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SourceStackId`  <a name="cfn-opsworks-stack-sourcestackid"></a>
If you're cloning an AWS OpsWorks stack, the stack ID of the source AWS OpsWorks stack to clone\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-opsworks-stack-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this AWS OpsWorks stack\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UseCustomCookbooks`  <a name="cfn-opsworks-stack-usecustcookbooks"></a>
Whether the stack uses custom cookbooks\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`UseOpsworksSecurityGroups`  <a name="cfn-opsworks-stack-useopsworkssecuritygroups"></a>
Whether to associate the AWS OpsWorks built\-in security groups with the stack's layers\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcId`  <a name="cfn-opsworks-stack-vpcid"></a>
The ID of the VPC that the stack is to be launched into, which must be in the specified region\. All instances are launched into this VPC\. If you specify this property, you must specify the `DefaultSubnetId` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d935c11"></a>

### Ref<a name="w3ab2c21c10d935c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myStack" }
```

For the AWS OpsWorks stack `myStack`, `Ref` returns the AWS OpsWorks stack ID\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Examples<a name="w3ab2c21c10d935c13"></a>

The following snippet creates an AWS OpsWorks stack that uses the default service role and Amazon EC2 role, which are created after you use AWS OpsWorks for the first time:

### JSON<a name="aws-resource-opsworks-stack-example.json"></a>

```
"myStack" : {
  "Type" : "AWS::OpsWorks::Stack",
  "Properties" : {
    "Name" : {"Ref":"OpsWorksStackName"},
    "ServiceRoleArn" : { "Fn::Join": ["", ["arn:aws:iam::", {"Ref":"AWS::AccountId"}, ":role/aws-opsworks-service-role"]] },
    "DefaultInstanceProfileArn" : { "Fn::Join": ["", ["arn:aws:iam::", {"Ref":"AWS::AccountId"}, ":instance-profile/aws-opsworks-ec2-role"]] },
    "DefaultSshKeyName" : {"Ref":"KeyName"}
  }
}
```

### YAML<a name="aws-resource-opsworks-stack-example.yaml"></a>

```
myStack: 
  Type: "AWS::OpsWorks::Stack"
  Properties: 
    Name: 
      Ref: "OpsWorksStackName"
    ServiceRoleArn: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:iam::"
          - 
            Ref: "AWS::AccountId"
          - ":role/aws-opsworks-service-role"
    DefaultInstanceProfileArn: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:iam::"
          - 
            Ref: "AWS::AccountId"
          - ":instance-profile/aws-opsworks-ec2-role"
    DefaultSshKeyName: 
      Ref: "KeyName"
```

### Specify tags for layers and stacks<a name="aws-resource-opsworks-stack-example3"></a>

The following complete template example specifies tags for an AWS OpsWorks layer and stack that reference parameter values\.

#### JSON<a name="aws-resource-opsworks-stack-example3.json"></a>

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

#### YAML<a name="aws-resource-opsworks-stack-example3.yaml"></a>

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

## Additional Information<a name="w3ab2c21c10d935c15"></a>
+ For a complete sample AWS OpsWorks template, see [AWS OpsWorks Template Snippets](quickref-opsworks.md)\.
+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)
+ [AWS::OpsWorks::App](aws-resource-opsworks-app.md)
+ [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)