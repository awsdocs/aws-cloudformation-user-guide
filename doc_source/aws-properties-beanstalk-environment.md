# AWS::ElasticBeanstalk::Environment<a name="aws-properties-beanstalk-environment"></a>

Creates or updates an AWS Elastic Beanstalk environment\.

**Topics**
+ [Syntax](#aws-resource-elasticbeanstalk-environment-syntax)
+ [Properties](#aws-properties-beanstalk-environment-prop)
+ [Return Values](#aws-properties-beanstalk-environment-ref)
+ [Examples](#aws-resource-elasticbeanstalk-environment-examples)
+ [See Also](#aws-resource-elasticbeanstalk-environment-seealso)

## Syntax<a name="aws-resource-elasticbeanstalk-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-environment-syntax.json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Environment",
   "Properties" : {
      "[ApplicationName](#cfn-beanstalk-environment-applicationname)" : String,
      "[CNAMEPrefix](#cfn-beanstalk-environment-cnameprefix)" : String,
      "[Description](#cfn-beanstalk-environment-description)" :  String,
      "[EnvironmentName](#cfn-beanstalk-environment-name)" :  String,
      "[OptionSettings](#cfn-beanstalk-environment-optionsettings)" : [ OptionSetting, ... ],
      "[PlatformArn](#cfn-beanstalk-environment-platformarn)" : String,
      "[SolutionStackName](#cfn-beanstalk-environment-solutionstackname)" : String,
      "[Tags](#cfn-beanstalk-environment-tags)" : [ Resource Tag, ... ],
      "[TemplateName](#cfn-beanstalk-environment-templatename)" : String,
      "[Tier](#cfn-beanstalk-environment-tier)" : Environment Tier,
      "[VersionLabel](#cfn-beanstalk-environment-versionlabel)" : String
   }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-environment-syntax.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Environment"
Properties:
  [ApplicationName](#cfn-beanstalk-environment-applicationname): String
  [CNAMEPrefix](#cfn-beanstalk-environment-cnameprefix): String
  [Description](#cfn-beanstalk-environment-description): String
  [EnvironmentName](#cfn-beanstalk-environment-name): String
  [OptionSettings](#cfn-beanstalk-environment-optionsettings): 
    - OptionSetting
  [PlatformArn](#cfn-beanstalk-environment-platformarn): String
  [SolutionStackName](#cfn-beanstalk-environment-solutionstackname): String
  [Tags](#cfn-beanstalk-environment-tags):
    - Resource Tag, ...
  [TemplateName](#cfn-beanstalk-environment-templatename): String
  [Tier](#cfn-beanstalk-environment-tier):
    Environment Tier
  [VersionLabel](#cfn-beanstalk-environment-versionlabel): String
```

## Properties<a name="aws-properties-beanstalk-environment-prop"></a>

For more information, see [ CreateEnvironment](http://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_CreateEnvironment.html) in the *AWS Elastic Beanstalk API Reference*\.

`ApplicationName`  <a name="cfn-beanstalk-environment-applicationname"></a>
The name of the application that is associated with this environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CNAMEPrefix`  <a name="cfn-beanstalk-environment-cnameprefix"></a>
A prefix for your Elastic Beanstalk environment URL\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-beanstalk-environment-description"></a>
A description that helps you identify this environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EnvironmentName`  <a name="cfn-beanstalk-environment-name"></a>
A name for the Elastic Beanstalk environment\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the environment name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`OptionSettings`  <a name="cfn-beanstalk-environment-optionsettings"></a>
Key\-value pairs defining configuration options for this environment, such as the instance type\. These options override the values that are defined in the solution stack or the [configuration template](aws-resource-beanstalk-configurationtemplate.md)\. If you remove any options during a stack update, the removed options revert to default values\.  
*Required*: Yes\. The `IamInstanceProfile` and `ServiceRole` options are required\.  
*Type*: List of [Elastic Beanstalk Environment OptionSetting](aws-properties-beanstalk-option-settings.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`PlatformArn`  <a name="cfn-beanstalk-environment-platformarn"></a>
The Amazon Resource Name \(ARN\) of the custom platform to use with the environment\. For more information, see [ Custom Platforms](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
If you specify `PlatformArn`, then don't specify `SolutionStackName`\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)   
*Example*: `"PlatformArn": "arn:aws:elasticbeanstalk:us-east-1::platform/PHP 5.4 running on 64bit Amazon Linux/2.4.4"`

`SolutionStackName`  <a name="cfn-beanstalk-environment-solutionstackname"></a>
The name of an Elastic Beanstalk solution stack that this configuration will use\. For more information, see [Supported Platforms](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
If you specify `SolutionStackName`, then don't specify `PlatformArn` or `TemplateName`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-beanstalk-environment-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this environment\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: You can update tags only if you update another property that requires that the environment be replaced, such as the `ApplicationName` property\.

`TemplateName`  <a name="cfn-beanstalk-environment-templatename"></a>
The name of the Elastic Beanstalk configuration template to use with the environment\.  
If you specify `TemplateName`, then don't specify `SolutionStackName`\.
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Tier`  <a name="cfn-beanstalk-environment-tier"></a>
Specifies the tier to use in creating this environment\. The environment tier that you choose determines whether Elastic Beanstalk provisions resources to support a web application that handles HTTP\(S\) requests or a web application that handles background\-processing tasks\.  
*Required*: No  
*Type*: [Elastic Beanstalk Environment Tier Property Type](aws-properties-beanstalk-environment-tier.md)  
*Update requires*: See [Elastic Beanstalk Environment Tier Property Type](aws-properties-beanstalk-environment-tier.md)

`VersionLabel`  <a name="cfn-beanstalk-environment-versionlabel"></a>
The version to associate with the environment\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

## Return Values<a name="aws-properties-beanstalk-environment-ref"></a>

### Ref<a name="w3ab2c21c10d627c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d627c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`EndpointURL`  
The URL to the load balancer for this environment\.  
Example:  
`awseb-myst-myen-132MQC4KRLAMD-1371280482.``us-east-2``.elb.amazonaws.com`

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-elasticbeanstalk-environment-examples"></a>

### Simple Environment<a name="aws-resource-elasticbeanstalk-environment-example1"></a>

#### JSON<a name="aws-resource-elasticbeanstalk-environment-example1.json"></a>

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

#### YAML<a name="aws-resource-elasticbeanstalk-environment-example1.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Environment"
Properties: 
  ApplicationName: 
    Ref: sampleApplication
  Description: "AWS Elastic Beanstalk Environment running PHP Sample Application"
  EnvironmentName: SamplePHPEnvironment
  TemplateName: DefaultConfiguration
  VersionLabel: "Initial Version"
```

### Environment with Embedded Option Settings<a name="aws-resource-elasticbeanstalk-environment-example2"></a>

#### JSON<a name="aws-resource-elasticbeanstalk-environment-example2.json"></a>

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

#### YAML<a name="aws-resource-elasticbeanstalk-environment-example2.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Environment"
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

### Custom or Supported Platform<a name="aws-resource-elasticbeanstalk-environment-example3"></a>

The following example contains parameters that enable specifying `PlatformArn` for a custom platform or `SolutionStackName` for a supported platform when creating the stack\.

#### JSON<a name="aws-resource-elasticbeanstalk-environment-example3.json"></a>

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
      "Properties": {
        "ApplicationVersions": [
          {
            "Description": "Version 1.0",
            "SourceBundle": {
              "S3Bucket": {
                "Fn::Join": ["", ["elasticbeanstalk-samples-", {"Ref": "AWS::Region"}]]
              },
              "S3Key": "python-sample-20150402.zip"
            },
            "VersionLabel": "Initial Version"
          }
        ],
        "Description": "AWS Elastic Beanstalk Python Sample Application"
      },
      "Type": "AWS::ElasticBeanstalk::Application"
    },
    "Environment": {
      "Properties": {
        "ApplicationName": {
          "Ref": "Application"
        },
        "Description": "AWS Elastic Beanstalk Environment running Python Sample Application",
        "PlatformArn": { "Ref" : "PlatformArn"},
        "SolutionStackName": {
          "Ref": "SolutionStackName"
        },
        "VersionLabel": "Initial Version",
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
      },
      "Type": "AWS::ElasticBeanstalk::Environment"
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

#### YAML<a name="aws-resource-elasticbeanstalk-environment-example3.yaml"></a>

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
    Properties:
      ApplicationVersions:
        - Description: Version 1.0
          SourceBundle:
            S3Bucket: !Join 
              - ''
              - - elasticbeanstalk-samples-
                - !Ref 'AWS::Region'
            S3Key: python-sample-20150402.zip
          VersionLabel: Initial Version
      Description: AWS Elastic Beanstalk Python Sample Application
    Type: 'AWS::ElasticBeanstalk::Application'
  Environment:
    Properties:
      ApplicationName: !Ref Application
      Description: AWS Elastic Beanstalk Environment running Python Sample Application
      PlatformArn: !Ref PlatformArn
      SolutionStackName: !Ref SolutionStackName
      VersionLabel: Initial Version
      OptionSettings:
        - Namespace: 'aws:autoscaling:launchconfiguration'
          OptionName: IamInstanceProfile
          Value: !Ref InstanceProfile
        - Namespace: 'aws:elasticbeanstalk:environment'
          OptionName: ServiceRole
          Value: !Ref ServiceRole
    Type: 'AWS::ElasticBeanstalk::Environment'
  ServiceRole:
    Type: 'AWS::IAM::Role'
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
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref InstanceProfileRole
  InstanceProfileRole:
    Type: 'AWS::IAM::Role'
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

## See Also<a name="aws-resource-elasticbeanstalk-environment-seealso"></a>
+  [Launching New Environments](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.environments.html) in the *AWS Elastic Beanstalk Developer Guide* 
+  [Managing Environments](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.managing.html) in the *AWS Elastic Beanstalk Developer Guide* 
+ For another complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.