# AWS::ElasticBeanstalk::Environment<a name="aws-properties-beanstalk-environment"></a>

The AWS::ElasticBeanstalk::Environment resource is an AWS Elastic Beanstalk resource type that specifies an Elastic Beanstalk environment\.

## Syntax<a name="aws-properties-beanstalk-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-environment-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::Environment",
  "Properties" : {
      "[ApplicationName](#cfn-beanstalk-environment-applicationname)" : String,
      "[CNAMEPrefix](#cfn-beanstalk-environment-cnameprefix)" : String,
      "[Description](#cfn-beanstalk-environment-description)" : String,
      "[EnvironmentName](#cfn-beanstalk-environment-name)" : String,
      "[OptionSettings](#cfn-beanstalk-environment-optionsettings)" : [ OptionSetting, ... ],
      "[PlatformArn](#cfn-beanstalk-environment-platformarn)" : String,
      "[SolutionStackName](#cfn-beanstalk-environment-solutionstackname)" : String,
      "[Tags](#cfn-elasticbeanstalk-environment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TemplateName](#cfn-beanstalk-environment-templatename)" : String,
      "[Tier](#cfn-beanstalk-environment-tier)" : Tier,
      "[VersionLabel](#cfn-beanstalk-environment-versionlabel)" : String
    }
}
```

### YAML<a name="aws-properties-beanstalk-environment-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::Environment
Properties: 
  [ApplicationName](#cfn-beanstalk-environment-applicationname): String
  [CNAMEPrefix](#cfn-beanstalk-environment-cnameprefix): String
  [Description](#cfn-beanstalk-environment-description): String
  [EnvironmentName](#cfn-beanstalk-environment-name): String
  [OptionSettings](#cfn-beanstalk-environment-optionsettings): 
    - OptionSetting
  [PlatformArn](#cfn-beanstalk-environment-platformarn): String
  [SolutionStackName](#cfn-beanstalk-environment-solutionstackname): String
  [Tags](#cfn-elasticbeanstalk-environment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TemplateName](#cfn-beanstalk-environment-templatename): String
  [Tier](#cfn-beanstalk-environment-tier): 
    Tier
  [VersionLabel](#cfn-beanstalk-environment-versionlabel): String
```

## Properties<a name="aws-properties-beanstalk-environment-properties"></a>

`ApplicationName`  <a name="cfn-beanstalk-environment-applicationname"></a>
The name of the application that is associated with this environment\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CNAMEPrefix`  <a name="cfn-beanstalk-environment-cnameprefix"></a>
If specified, the environment attempts to use this value as the prefix for the CNAME in your Elastic Beanstalk environment URL\. If not specified, the CNAME is generated automatically by appending a random alphanumeric string to the environment name\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `63`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-beanstalk-environment-description"></a>
Your description for this environment\.  
*Required*: No  
*Type*: String  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentName`  <a name="cfn-beanstalk-environment-name"></a>
A unique name for the environment\.  
Constraint: Must be from 4 to 40 characters in length\. The name can contain only letters, numbers, and hyphens\. It can't start or end with a hyphen\. This name must be unique within a region in your account\.  
If you don't specify the `CNAMEPrefix` parameter, the environment name becomes part of the CNAME, and therefore part of the visible URL for your application\.  
If you don't specify an environment name, AWS CloudFormation generates a unique physical ID and uses that ID for the environment name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OptionSettings`  <a name="cfn-beanstalk-environment-optionsettings"></a>
Key\-value pairs defining configuration options for this environment, such as the instance type\. These options override the values that are defined in the solution stack or the [configuration template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-beanstalk-configurationtemplate.html)\. If you remove any options during a stack update, the removed options retain their current values\.  
*Required*: No  
*Type*: List of [OptionSetting](aws-properties-beanstalk-option-settings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlatformArn`  <a name="cfn-beanstalk-environment-platformarn"></a>
The Amazon Resource Name \(ARN\) of the custom platform to use with the environment\. For more information, see [Custom Platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
If you specify `PlatformArn`, don't specify `SolutionStackName`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SolutionStackName`  <a name="cfn-beanstalk-environment-solutionstackname"></a>
The name of an Elastic Beanstalk solution stack \(platform version\) to use with the environment\. If specified, Elastic Beanstalk sets the configuration values to the default values associated with the specified solution stack\. For a list of current solution stacks, see [Elastic Beanstalk Supported Platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/platforms/platforms-supported.html) in the *AWS Elastic Beanstalk Platforms* guide\.  
If you specify `SolutionStackName`, don't specify `PlatformArn` or `TemplateName`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-elasticbeanstalk-environment-tags"></a>
Specifies the tags applied to resources in the environment\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-beanstalk-environment-templatename"></a>
The name of the Elastic Beanstalk configuration template to use with the environment\.  
If you specify `TemplateName`, then don't specify `SolutionStackName`\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tier`  <a name="cfn-beanstalk-environment-tier"></a>
Specifies the tier to use in creating this environment\. The environment tier that you choose determines whether Elastic Beanstalk provisions resources to support a web application that handles HTTP\(S\) requests or a web application that handles background\-processing tasks\.  
*Required*: No  
*Type*: [Tier](aws-properties-beanstalk-environment-tier.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`VersionLabel`  <a name="cfn-beanstalk-environment-versionlabel"></a>
The name of the application version to deploy\.  
Default: If not specified, Elastic Beanstalk attempts to deploy the sample application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-beanstalk-environment-return-values"></a>

### Ref<a name="aws-properties-beanstalk-environment-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-beanstalk-environment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-beanstalk-environment-return-values-fn--getatt-fn--getatt"></a>

`EndpointURL`  <a name="EndpointURL-fn::getatt"></a>
For load\-balanced, autoscaling environments, the URL to the load balancer\. For single\-instance environments, the IP address of the instance\.  
Example load balancer URL:  
 `awseb-myst-myen-132MQC4KRLAMD-1371280482.us-east-2.elb.amazonaws.com`   
Example instance IP address:  
 `192.0.2.0` 

## Examples<a name="aws-properties-beanstalk-environment--examples"></a>

### Simple Environment<a name="aws-properties-beanstalk-environment--examples--Simple_Environment"></a>

#### JSON<a name="aws-properties-beanstalk-environment--examples--Simple_Environment--json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Environment",
   "Properties" : {
      "ApplicationName" : { "Ref" : "sampleApplication" },
      "Description" :  "AWS Elastic Beanstalk Environment running PHP Sample Application",
      "EnvironmentName" :  "SamplePHPEnvironment",
      "TemplateName" : "DefaultConfiguration",
      "VersionLabel" : "Initial Version"
   }
}
```

#### YAML<a name="aws-properties-beanstalk-environment--examples--Simple_Environment--yaml"></a>

```
Type: AWS::ElasticBeanstalk::Environment
Properties: 
  ApplicationName: 
    Ref: sampleApplication
  Description: "AWS Elastic Beanstalk Environment running PHP Sample Application"
  EnvironmentName: SamplePHPEnvironment
  TemplateName: DefaultConfiguration
  VersionLabel: "Initial Version"
```

### Environment with Embedded Option Settings<a name="aws-properties-beanstalk-environment--examples--Environment_with_Embedded_Option_Settings"></a>

#### JSON<a name="aws-properties-beanstalk-environment--examples--Environment_with_Embedded_Option_Settings--json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Environment",
   "Properties" : {
      "ApplicationName" : { "Ref" : "sampleApplication" },
      "Description" :  "AWS Elastic Beanstalk Environment running Python Sample Application",
      "EnvironmentName" :  "SamplePythonEnvironment",
      "SolutionStackName" : "64bit Amazon Linux 2017.03 v2.5.0 running Python 2.7",
      "OptionSettings" : [ {
         "Namespace" : "aws:autoscaling:launchconfiguration",
         "OptionName" : "EC2KeyName",
         "Value" : { "Ref" : "KeyName" }
      } ],
      "VersionLabel" : "Initial Version"
   }
}
```

#### YAML<a name="aws-properties-beanstalk-environment--examples--Environment_with_Embedded_Option_Settings--yaml"></a>

```
Type: AWS::ElasticBeanstalk::Environment
Properties: 
  ApplicationName: 
    Ref: sampleApplication
  Description: "AWS Elastic Beanstalk Environment running Python Sample Application"
  EnvironmentName: SamplePythonEnvironment
  SolutionStackName: "64bit Amazon Linux 2017.03 v2.5.0 running Python 2.7"
  OptionSettings: 
    - 
      Namespace: "aws:autoscaling:launchconfiguration"
      OptionName: EC2KeyName
      Value: 
        Ref: KeyName
  VersionLabel: "Initial Version"
```

### Custom or Supported Platform<a name="aws-properties-beanstalk-environment--examples--Custom_or_Supported_Platform"></a>

The following example contains parameters that enable specifying `PlatformArn` for a custom platform or `SolutionStackName` for a supported platform when creating the stack\.

#### JSON<a name="aws-properties-beanstalk-environment--examples--Custom_or_Supported_Platform--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Elasticbeanstalk test template",
  "Parameters": {
    "BeanstalkService": {
      "Type": "String"
    },
    "Ec2Service": {
      "Type": "String"
    },
    "Partition":{
      "Type": "String"
    },
    "SolutionStackName": {
      "Type": "String"
    },
    "PlatformArn": {
      "Type": "String"
    }
  },
  "Resources": {
    "Application": {
      "Type": "AWS::ElasticBeanstalk::Application",
      "Properties": {
        "ApplicationName": "SampleBeanstalkApp",
        "Description": "AWS Elastic Beanstalk Python Sample Application"
      }
    },
    "AppVersion": {
      "Type": "AWS::ElasticBeanstalk::ApplicationVersion",
      "Properties": {
        "ApplicationName": {"Ref" : "Application"},
        "Description": "Version 1.0",
        "SourceBundle": {
          "S3Bucket": {
            "Fn::Join": ["-", [ "elasticbeanstalk-samples", { "Ref" : "AWS::Region" } ] ] },
          "S3Key": "python-sample-20150402.zip"
        }
      }
    },
    "Environment": {
      "Type": "AWS::ElasticBeanstalk::Environment",
      "Properties": {
        "ApplicationName": {"Ref": "Application"},
        "Description": "AWS Elastic Beanstalk Environment running Python Sample Application",
        "PlatformArn": { "Ref" : "PlatformArn"},
        "SolutionStackName": {
          "Ref": "SolutionStackName"
        },
        "VersionLabel": {"Ref": "AppVersion"},
        "OptionSettings": [
          {
            "Namespace": "aws:autoscaling:launchconfiguration",
            "OptionName": "IamInstanceProfile",
            "Value": {
              "Ref": "InstanceProfile"
            }
          },
          {
            "Namespace": "aws:elasticbeanstalk:environment",
            "OptionName": "ServiceRole",
            "Value": {
              "Ref": "ServiceRole"
            }
          }
        ]
      }
    },
    "ServiceRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": {"Ref": "BeanstalkService"}
              },
              "Action": "sts:AssumeRole",
              "Condition": {
                "StringEquals": {
                  "sts:ExternalId": "elasticbeanstalk"
                }
              }
            }
          ]
        },
        "Policies": [
          {
            "PolicyName": "root",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Effect": "Allow",
                  "Action": [
                    "elasticloadbalancing:DescribeInstanceHealth",
                    "ec2:DescribeInstances",
                    "ec2:DescribeInstanceStatus",
                    "ec2:GetConsoleOutput",
                    "ec2:AssociateAddress",
                    "ec2:DescribeAddresses",
                    "ec2:DescribeSecurityGroups",
                    "sqs:GetQueueAttributes",
                    "sqs:GetQueueUrl",
                    "autoscaling:DescribeAutoScalingGroups",
                    "autoscaling:DescribeAutoScalingInstances",
                    "autoscaling:DescribeScalingActivities",
                    "autoscaling:DescribeNotificationConfigurations"
                  ],
                  "Resource": [
                    "*"
                  ]
                }
              ]
            }
          }
        ],
        "Path": "/"
      }
    },
    "InstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Path": "/",
        "Roles": [
          {
            "Ref": "InstanceProfileRole"
          }
        ]
      }
    },
    "InstanceProfileRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  {"Ref": "Ec2Service"}
                ]
              },
              "Action": [
                "sts:AssumeRole"
              ]
            }
          ]
        },
        "Policies": [
          {
            "PolicyName": "root",
            "PolicyDocument": {
              "Version": "2012-10-17",
              "Statement": [
                {
                  "Sid": "BucketAccess",
                  "Action": [
                    "s3:Get*",
                    "s3:List*",
                    "s3:PutObject"
                  ],
                  "Effect": "Allow",
                  "Resource": [
                    {
                      "Fn::Join": [
                        "",
                        [
                          "arn:",
                          {
                            "Ref": "Partition"
                          },
                          ":s3:::elasticbeanstalk-*-",
                          {
                            "Ref": "AWS::AccountId"
                          }
                        ]
                      ]
                    },
                    {
                      "Fn::Join": [
                        "",
                        [
                          "arn:",
                          {
                            "Ref": "Partition"
                          },
                          ":s3:::elasticbeanstalk-*-",
                          {
                            "Ref": "AWS::AccountId"
                          },
                          "/*"
                        ]
                      ]
                    },
                    {
                      "Fn::Join": [
                        "",
                        [
                          "arn:",
                          {
                            "Ref": "Partition"
                          },
                          ":s3:::elasticbeanstalk-*-",
                          {
                            "Ref": "AWS::AccountId"
                          },
                          "-*"
                        ]
                      ]
                    },
                    {
                      "Fn::Join": [
                        "",
                        [
                          "arn:",
                          {
                            "Ref": "Partition"
                          },
                          ":s3:::elasticbeanstalk-*-",
                          {
                            "Ref": "AWS::AccountId"
                          },
                          "-*/*"
                        ]
                      ]
                    }
                  ]
                },
                {
                  "Sid": "ECSAccess",
                  "Effect": "Allow",
                  "Action": [
                    "ecs:StartTask",
                    "ecs:StopTask",
                    "ecs:RegisterContainerInstance",
                    "ecs:DeregisterContainerInstance",
                    "ecs:DescribeContainerInstances",
                    "ecs:DiscoverPollEndpoint",
                    "ecs:Submit*",
                    "ecs:Poll"
                  ],
                  "Resource": "*"
                },
                {
                  "Sid": "QueueAccess",
                  "Action": [
                    "sqs:ChangeMessageVisibility",
                    "sqs:DeleteMessage",
                    "sqs:ReceiveMessage",
                    "sqs:SendMessage"
                  ],
                  "Effect": "Allow",
                  "Resource": "*"
                },
                {
                  "Sid": "DynamoPeriodicTasks",
                  "Action": [
                    "dynamodb:BatchGetItem",
                    "dynamodb:BatchWriteItem",
                    "dynamodb:DeleteItem",
                    "dynamodb:GetItem",
                    "dynamodb:PutItem",
                    "dynamodb:Query",
                    "dynamodb:Scan",
                    "dynamodb:UpdateItem"
                  ],
                  "Effect": "Allow",
                  "Resource": [
                    {
                      "Fn::Join": [
                        "",
                        [
                          "arn:",
                          {
                            "Ref": "Partition"
                          },
                          ":dynamodb:*:",
                          {
                            "Ref": "AWS::AccountId"
                          },
                          ":table/*-stack-AWSEBWorkerCronLeaderRegistry*"
                        ]
                      ]
                    }
                  ]
                },
                {
                  "Sid": "MetricsAccess",
                  "Action": [
                    "cloudwatch:PutMetricData"
                  ],
                  "Effect": "Allow",
                  "Resource": "*"
                }
              ]
            }
          }
        ],
        "Path": "/"
      }
    }
  }
}
```

#### YAML<a name="aws-properties-beanstalk-environment--examples--Custom_or_Supported_Platform--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Elasticbeanstalk test template
Parameters:
  BeanstalkService:
    Type: String
  Ec2Service:
    Type: String
  Partition:
    Type: String
  SolutionStackName:
    Type: String
  PlatformArn:
    Type: String
Resources:
  Application:
    Type: AWS::ElasticBeanstalk::Application
    Properties:
      ApplicationName: SampleBeanstalkApp
      Description: AWS Elastic Beanstalk Python Sample Application
  AppVersion:
    Type: AWS::ElasticBeanstalk::ApplicationVersion
    Properties:
      ApplicationName: !Ref Application
      Description: Version 1.0
      SourceBundle:
        S3Bucket: Fn::Join:
          - '-'
          - 
          - 'elasticbeanstalk-samples'
          - !Ref 'AWS::Region'
        S3Key: python-sample-20150402.zip
  Environment:
    Type: AWS::ElasticBeanstalk::Environment
    Properties:
      ApplicationName: !Ref Application
      Description: AWS Elastic Beanstalk Environment running Python Sample Application
      PlatformArn: !Ref PlatformArn
      SolutionStackName: !Ref SolutionStackName
      VersionLabel: !Ref AppVersion
      OptionSettings:
        - Namespace: 'aws:autoscaling:launchconfiguration'
          OptionName: IamInstanceProfile
          Value: !Ref InstanceProfile
        - Namespace: 'aws:elasticbeanstalk:environment'
          OptionName: ServiceRole
          Value: !Ref ServiceRole
  ServiceRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: !Ref BeanstalkService
            Action: 'sts:AssumeRole'
            Condition:
              StringEquals:
                'sts:ExternalId': elasticbeanstalk
      Policies:
        - PolicyName: root
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action:
                  - 'elasticloadbalancing:DescribeInstanceHealth'
                  - 'ec2:DescribeInstances'
                  - 'ec2:DescribeInstanceStatus'
                  - 'ec2:GetConsoleOutput'
                  - 'ec2:AssociateAddress'
                  - 'ec2:DescribeAddresses'
                  - 'ec2:DescribeSecurityGroups'
                  - 'sqs:GetQueueAttributes'
                  - 'sqs:GetQueueUrl'
                  - 'autoscaling:DescribeAutoScalingGroups'
                  - 'autoscaling:DescribeAutoScalingInstances'
                  - 'autoscaling:DescribeScalingActivities'
                  - 'autoscaling:DescribeNotificationConfigurations'
                Resource:
                  - '*'
      Path: /
  InstanceProfile:
    Type: AWS::IAM::InstanceProfile
    Properties:
      Path: /
      Roles:
        - !Ref InstanceProfileRole
  InstanceProfileRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - !Ref Ec2Service
            Action:
              - 'sts:AssumeRole'
      Policies:
        - PolicyName: root
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Sid: BucketAccess
                Action:
                  - 's3:Get*'
                  - 's3:List*'
                  - 's3:PutObject'
                Effect: Allow
                Resource:
                  - !Join 
                    - ''
                    - - 'arn:'
                      - !Ref Partition
                      - ':s3:::elasticbeanstalk-*-'
                      - !Ref 'AWS::AccountId'
                  - !Join 
                    - ''
                    - - 'arn:'
                      - !Ref Partition
                      - ':s3:::elasticbeanstalk-*-'
                      - !Ref 'AWS::AccountId'
                      - /*
                  - !Join 
                    - ''
                    - - 'arn:'
                      - !Ref Partition
                      - ':s3:::elasticbeanstalk-*-'
                      - !Ref 'AWS::AccountId'
                      - '-*'
                  - !Join 
                    - ''
                    - - 'arn:'
                      - !Ref Partition
                      - ':s3:::elasticbeanstalk-*-'
                      - !Ref 'AWS::AccountId'
                      - '-*/*'
              - Sid: ECSAccess
                Effect: Allow
                Action:
                  - 'ecs:StartTask'
                  - 'ecs:StopTask'
                  - 'ecs:RegisterContainerInstance'
                  - 'ecs:DeregisterContainerInstance'
                  - 'ecs:DescribeContainerInstances'
                  - 'ecs:DiscoverPollEndpoint'
                  - 'ecs:Submit*'
                  - 'ecs:Poll'
                Resource: '*'
              - Sid: QueueAccess
                Action:
                  - 'sqs:ChangeMessageVisibility'
                  - 'sqs:DeleteMessage'
                  - 'sqs:ReceiveMessage'
                  - 'sqs:SendMessage'
                Effect: Allow
                Resource: '*'
              - Sid: DynamoPeriodicTasks
                Action:
                  - 'dynamodb:BatchGetItem'
                  - 'dynamodb:BatchWriteItem'
                  - 'dynamodb:DeleteItem'
                  - 'dynamodb:GetItem'
                  - 'dynamodb:PutItem'
                  - 'dynamodb:Query'
                  - 'dynamodb:Scan'
                  - 'dynamodb:UpdateItem'
                Effect: Allow
                Resource:
                  - !Join 
                    - ''
                    - - 'arn:'
                      - !Ref Partition
                      - ':dynamodb:*:'
                      - !Ref 'AWS::AccountId'
                      - ':table/*-stack-AWSEBWorkerCronLeaderRegistry*'
              - Sid: MetricsAccess
                Action:
                  - 'cloudwatch:PutMetricData'
                Effect: Allow
                Resource: '*'
      Path: /
```

## See also<a name="aws-properties-beanstalk-environment--seealso"></a>
+  [Creating an AWS Elastic Beanstalk Environment](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.environments.html) in the *AWS Elastic Beanstalk Developer Guide* 
+  [Managing Environments](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.managing.html) in the *AWS Elastic Beanstalk Developer Guide* 
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-elasticbeanstalk.html)\.