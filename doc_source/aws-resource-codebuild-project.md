# AWS::CodeBuild::Project<a name="aws-resource-codebuild-project"></a>

The `AWS::CodeBuild::Project` resource configures how AWS CodeBuild builds your source code\. For example, it tells AWS CodeBuild where to get the source code and which build environment to use\.

**Topics**
+ [Syntax](#aws-resource-codebuild-project-syntax)
+ [Properties](#aws-resource-codebuild-project-properties)
+ [Return Values](#aws-resource-codebuild-project-returnvalues)
+ [Examples](#aws-resource-codebuild-project-examples)
+ [See Also](#aws-resource-codebuild-project-seealso)

## Syntax<a name="aws-resource-codebuild-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codebuild-project-syntax.json"></a>

```
{
  "Type" : "AWS::CodeBuild::Project",
  "Properties" : {
    "[Artifacts](#cfn-codebuild-project-artifacts)" : [*Artifacts*](aws-properties-codebuild-project-artifacts.md),
    "[BadgeEnabled](#cfn-codebuild-project-badgeenabled)" : Boolean,
    "[Cache](#cfn-codebuild-project-cache)" : [*ProjectCache*](aws-properties-codebuild-project-projectcache.md),
    "[Description](#cfn-codebuild-project-description)" : String,
    "[EncryptionKey](#cfn-codebuild-project-encryptionkey)" : String,
    "[Environment](#cfn-codebuild-project-environment)" : [*Environment*](aws-properties-codebuild-project-environment.md),
    "[Name](#cfn-codebuild-project-name)" : String,
    "[ServiceRole](#cfn-codebuild-project-servicerole)" : String,
    "[Source](#cfn-codebuild-project-source)" : [*Source*](aws-properties-codebuild-project-source.md),
    "[Tags](#cfn-codebuild-project-tags)" : [ Resource Tag, ... ],
    "[TimeoutInMinutes](#cfn-codebuild-project-timeoutinminutes)" : Integer,
    "[Triggers](#cfn-codebuild-project-triggers)" : [*Triggers*](aws-properties-codebuild-project-projecttriggers.md),
    "[VpcConfig](#cfn-codebuild-project-vpcconfig)" : [*VpcConfig*](aws-properties-codebuild-project-vpcconfig.md)
  }
}
```

### YAML<a name="aws-resource-codebuild-project-syntax.yaml"></a>

```
Type: "AWS::CodeBuild::Project"
Properties: 
  [Artifacts](#cfn-codebuild-project-artifacts):
    [*Artifacts*](aws-properties-codebuild-project-artifacts.md)
  [BadgeEnabled](#cfn-codebuild-project-badgeenabled): Boolean
  [Cache](#cfn-codebuild-project-cache): 
    [*ProjectCache*](aws-properties-codebuild-project-projectcache.md)
  [Description](#cfn-codebuild-project-description): String
  [EncryptionKey](#cfn-codebuild-project-encryptionkey): String
  [Environment](#cfn-codebuild-project-environment):
    [*Environment*](aws-properties-codebuild-project-environment.md)
  [Name](#cfn-codebuild-project-name): String
  [ServiceRole](#cfn-codebuild-project-servicerole): String
  [Source](#cfn-codebuild-project-source):
    [*Source*](aws-properties-codebuild-project-source.md)
  [Tags](#cfn-codebuild-project-tags):
    - Resource Tag
  [TimeoutInMinutes](#cfn-codebuild-project-timeoutinminutes): Integer
  [Triggers](#cfn-codebuild-project-triggers): [*Triggers*](aws-properties-codebuild-project-projecttriggers.md)
  [VpcConfig](#cfn-codebuild-project-vpcconfig): 
    [*VpcConfig*](aws-properties-codebuild-project-vpcconfig.md)
```

## Properties<a name="aws-resource-codebuild-project-properties"></a>

`Artifacts`  <a name="cfn-codebuild-project-artifacts"></a>
The output settings for artifacts that the project generates during a build\.  
*Required*: Yes  
*Type*: [AWS CodeBuild Project Artifacts](aws-properties-codebuild-project-artifacts.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`BadgeEnabled`  <a name="cfn-codebuild-project-badgeenabled"></a>
Indicates whether AWS CodeBuild generates a publicly accessible URL for your project's build badge\. For more information, see [Build Badges Sample](http://docs.aws.amazon.com/codebuild/latest/userguide/sample-build-badges.html) in the *AWS CodeBuild User Guide*\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Cache`  <a name="cfn-codebuild-project-cache"></a>
Settings that AWS CodeBuild uses to store and reuse build dependencies\.  
 *Required*: No  
 *Type*: [AWS CodeBuild Project ProjectCache](aws-properties-codebuild-project-projectcache.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-codebuild-project-description"></a>
A description of the project\. Use the description to identify the purpose of the project\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EncryptionKey`  <a name="cfn-codebuild-project-encryptionkey"></a>
The alias or Amazon Resource Name \(ARN\) of the AWS Key Management Service \(AWS KMS\) customer master key \(CMK\) that AWS CodeBuild uses to encrypt the build output\. If you don't specify a value, AWS CodeBuild uses the AWS\-managed CMK for Amazon Simple Storage Service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Environment`  <a name="cfn-codebuild-project-environment"></a>
The build environment settings for the project, such as the environment type or the environment variables to use for the build environment\.  
*Required*: Yes  
*Type*: [AWS CodeBuild Project Environment](aws-properties-codebuild-project-environment.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-codebuild-project-name"></a>
A name for the project\. The name must be unique across all of the projects in your AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceRole`  <a name="cfn-codebuild-project-servicerole"></a>
The ARN of the service role that AWS CodeBuild uses to interact with services on your behalf\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Source`  <a name="cfn-codebuild-project-source"></a>
The source code settings for the project, such as the source code's repository type and location\.  
*Required*: Yes  
*Type*: [AWS CodeBuild Project Source](aws-properties-codebuild-project-source.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-codebuild-project-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for the AWS CodeBuild project\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimeoutInMinutes`  <a name="cfn-codebuild-project-timeoutinminutes"></a>
The number of minutes after which AWS CodeBuild stops the build if it's not complete\. For valid values, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Triggers`  <a name="cfn-codebuild-project-triggers"></a>
For an existing AWS CodeBuild build project that has its source code stored in a GitHub repository, enables AWS CodeBuild to begin automatically rebuilding the source code every time a code change is pushed to the repository\.  
*Required*: No  
 *Type*: [AWS CodeBuild Project ProjectTriggers](aws-properties-codebuild-project-projecttriggers.md)   
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpcConfig`  <a name="cfn-codebuild-project-vpcconfig"></a>
Settings that enable AWS CodeBuild to access resources in an Amazon VPC\. For more information, see [Use AWS CodeBuild with Amazon Virtual Private Cloud](http://docs.aws.amazon.com/codebuild/latest/userguide/vpc-support.html) in the *AWS CodeBuild User Guide*\.  
 *Required*: No  
 *Type*: [AWS CodeBuild Project VpcConfig](aws-properties-codebuild-project-vpcconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-codebuild-project-returnvalues"></a>

### Ref<a name="aws-resource-codebuild-project-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the name of the AWS CodeBuild project, such as `myProjectName`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-codebuild-project-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. This section lists the available attribute and a sample return value\.

`Arn`  
The ARN of the AWS CodeBuild project, such as `arn:aws:codebuild:us-west-2:123456789012:project/myProjectName`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-codebuild-project-examples"></a>

### <a name="aws-resource-codebuild-project-example1"></a>

The following example creates an AWS CodeBuild project\.

#### JSON<a name="aws-resource-codebuild-project-example1.json"></a>

```
{
  "Project": {
    "Type": "AWS::CodeBuild::Project",
    "Properties": {
      "Name": "myProjectName",
      "Description": "A description about my project",
      "ServiceRole": { "Fn::GetAtt": [ "ServiceRole", "Arn" ] },
      "Artifacts": {
        "Type": "no_artifacts"
      },
      "Environment": {
        "Type": "LINUX_CONTAINER",
        "ComputeType": "BUILD_GENERAL1_SMALL",
        "Image": "aws/codebuild/java:openjdk-8",
        "EnvironmentVariables": [
          {
            "Name": "varName",
            "Value": "varValue"
          }
        ]
      },
      "Source": {
        "Location": "codebuild-demo-test/0123ab9a371ebf0187b0fe5614fbb72c",
        "Type": "S3"
      },
      "TimeoutInMinutes": 10,
      "Tags": [
        {
          "Key": "Key1",
          "Value": "Value1"
        },
        {
          "Key": "Key2",
          "Value": "Value2"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-codebuild-project-example1.yaml"></a>

```
Project:
  Type: AWS::CodeBuild::Project
  Properties:
    Name: myProjectName
    Description: A description about my project
    ServiceRole: !GetAtt ServiceRole.Arn
    Artifacts:
      Type: no_artifacts
    Environment:
      Type: LINUX_CONTAINER
      ComputeType: BUILD_GENERAL1_SMALL
      Image: aws/codebuild/java:openjdk-8
      EnvironmentVariables:
      - Name: varName
        Value: varValue
    Source:
      Location: codebuild-demo-test/0123ab9a371ebf0187b0fe5614fbb72c
      Type: S3
    TimeoutInMinutes: 10
    Tags:
      - Key: Key1
        Value: Value1
      - Key: Key2
        Value: Value2
```

### <a name="aws-resource-codebuild-project-example2"></a>

The following example creates a project that caches build dependencies in Amazon S3 and uses resources in an Amazon VPC\.

#### JSON<a name="aws-resource-codebuild-project-example2.json"></a>

```
{
  "Resources": {
    "CodeBuildProject": {
      "Type": "AWS::CodeBuild::Project",
      "Properties": {
        "ServiceRole": {
          "Ref": "CodeBuildRole"
        },
        "Artifacts": {
          "Type": "CODEPIPELINE"
        },
        "BadgeEnabled": "true",
        "Environment": {
          "Type": "LINUX_CONTAINER",
          "ComputeType": "BUILD_GENERAL1_SMALL",
          "Image": "aws/codebuild/ubuntu-base:14.04",
          "EnvironmentVariables": [
            {
              "Name": "varName1",
              "Value": "varValue1"
            },
            {
              "Name": "varName2",
              "Value": "varValue2",
              "Type": "PLAINTEXT"
            },
            {
              "Name": "varName3",
              "Value": "/CodeBuild/testParameter",
              "Type": "PARAMETER_STORE"
            }
          ]
        },
        "Source": {
          "Type": "CODEPIPELINE"
        },
        "TimeoutInMinutes": 10,
        "VpcConfig": {
          "VpcId": {
            "Ref": "CodeBuildVPC"
          },
          "Subnets": [
            {
              "Ref": "CodeBuildSubnet"
            }
          ],
          "SecurityGroupIds": [
            {
              "Ref": "CodeBuildSecurityGroup"
            }
          ]
        },
        "Cache": {
          "Type": "S3",
          "Location": "mybucket/prefix"
        }
      }
    },
    "CodeBuildRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Statement": [
            {
              "Action": [
                "sts:AssumeRole"
              ],
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "codebuild.amazonaws.com"
                ]
              }
            }
          ],
          "Version": "2012-10-17"
        },
        "Path": "/",
        "Policies": [
          {
            "PolicyName": "CodeBuildAccess",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Action": [
                    "logs:*",
                    "ec2:CreateNetworkInterface",
                    "ec2:DescribeNetworkInterfaces",
                    "ec2:DeleteNetworkInterface",
                    "ec2:DescribeSubnets",
                    "ec2:DescribeSecurityGroups",
                    "ec2:DescribeDhcpOptions",
                    "ec2:DescribeVpcs",
                    "ec2:CreateNetworkInterfacePermission"
                  ],
                  "Effect": "Allow",
                  "Resource": "*"
                }
              ]
            }
          }
        ]
      }
    },
    "CodeBuildVPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "10.0.0.0/16",
        "EnableDnsSupport": "true",
        "EnableDnsHostnames": "true",
        "Tags": [
          {
            "Key": "name",
            "Value": "codebuild"
          }
        ]
      }
    },
    "CodeBuildSubnet": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": {
          "Ref": "CodeBuildVPC"
        },
        "CidrBlock": "10.0.1.0/24"
      }
    },
    "CodeBuildSecurityGroup": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "GroupName": "Codebuild Internet Group",
        "GroupDescription": "CodeBuild SecurityGroup",
        "VpcId": {
          "Ref": "CodeBuildVPC"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-codebuild-project-example2.yaml"></a>

```
Resources:
  CodeBuildProject:
    Type: AWS::CodeBuild::Project
    Properties:
      ServiceRole: !Ref CodeBuildRole
      Artifacts:
        Type: CODEPIPELINE
      BadgeEnabled: 'true'
      Environment:
        Type: LINUX_CONTAINER
        ComputeType: BUILD_GENERAL1_SMALL
        Image: aws/codebuild/ubuntu-base:14.04
        EnvironmentVariables:
          - Name: varName1
            Value: varValue1
          - Name: varName2
            Value: varValue2
            Type: PLAINTEXT
          - Name: varName3
            Value: /CodeBuild/testParameter
            Type: PARAMETER_STORE
      Source:
        Type: CODEPIPELINE
      TimeoutInMinutes: 10
      VpcConfig:
        VpcId: !Ref CodeBuildVPC
        Subnets: [!Ref CodeBuildSubnet]
        SecurityGroupIds: [!Ref CodeBuildSecurityGroup]
      Cache:
        Type: S3
        Location: mybucket/prefix
  CodeBuildRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Statement:
        - Action: ['sts:AssumeRole']
          Effect: Allow
          Principal:
            Service: [codebuild.amazonaws.com]
        Version: '2012-10-17'
      Path: /
      Policies:
        - PolicyName: CodeBuildAccess
          PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Action:
                - 'logs:*'
                - 'ec2:CreateNetworkInterface'
                - 'ec2:DescribeNetworkInterfaces'
                - 'ec2:DeleteNetworkInterface'
                - 'ec2:DescribeSubnets'
                - 'ec2:DescribeSecurityGroups'
                - 'ec2:DescribeDhcpOptions'
                - 'ec2:DescribeVpcs'
                - 'ec2:CreateNetworkInterfacePermission'
                Effect: Allow
                Resource: '*'
  CodeBuildVPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
      EnableDnsSupport: 'true'
      EnableDnsHostnames: 'true'
      Tags:
        - Key: name
          Value: codebuild
  CodeBuildSubnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId:
        Ref: CodeBuildVPC
      CidrBlock: 10.0.1.0/24
  CodeBuildSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupName: Codebuild Internet Group
      GroupDescription: 'CodeBuild SecurityGroup'
      VpcId: !Ref CodeBuildVPC
```

## See Also<a name="aws-resource-codebuild-project-seealso"></a>
+ [ CreateProject](http://docs.aws.amazon.com/codebuild/latest/APIReference/API_CreateProject.html) in the *AWS CodeBuild API Reference*