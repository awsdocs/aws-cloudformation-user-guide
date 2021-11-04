# Elastic Beanstalk template snippets<a name="quickref-elasticbeanstalk"></a>

With Elastic Beanstalk, you can quickly deploy and manage applications in AWS without worrying about the infrastructure that runs those applications\. The following sample template can help you describe Elastic Beanstalk resources in your AWS CloudFormation template\.

## Elastic Beanstalk sample PHP<a name="quickref-elasticbeanstalk-sampleenv"></a>

The following sample template deploys a sample PHP web application that's stored in an Amazon S3 bucket\. The environment is also an autoscaling, load\-balancing environment, with a minimum of two Amazon EC2 instances and a maximum of six\.

Replace `solution-stack` with a solution stack name \(platform version\)\. For a list of available solution stacks, use the AWS CLI command `aws elasticbeanstalk list-available-solution-stacks`\.

### JSON<a name="quickref-elasticbeanstalk-example-1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "sampleApplication": {
            "Type": "AWS::ElasticBeanstalk::Application",
            "Properties": {
                "Description": "AWS Elastic Beanstalk Sample Application"
            }
        },
        "sampleApplicationVersion": {
            "Type": "AWS::ElasticBeanstalk::ApplicationVersion",
            "Properties": {
                "ApplicationName": {
                    "Ref": "sampleApplication"
                },
                "Description": "AWS ElasticBeanstalk Sample Application Version",
                "SourceBundle": {
                    "S3Bucket": {
                        "Fn::Sub": "elasticbeanstalk-samples-${AWS::Region}"
                    },
                    "S3Key": "php-newsample-app.zip"
                }
            }
        },
        "sampleConfigurationTemplate": {
            "Type": "AWS::ElasticBeanstalk::ConfigurationTemplate",
            "Properties": {
                "ApplicationName": {
                    "Ref": "sampleApplication"
                },
                "Description": "AWS ElasticBeanstalk Sample Configuration Template",
                "OptionSettings": [
                    {
                        "Namespace": "aws:autoscaling:asg",
                        "OptionName": "MinSize",
                        "Value": "2"
                    },
                    {
                        "Namespace": "aws:autoscaling:asg",
                        "OptionName": "MaxSize",
                        "Value": "6"
                    },
                    {
                        "Namespace": "aws:elasticbeanstalk:environment",
                        "OptionName": "EnvironmentType",
                        "Value": "LoadBalanced"
                    },
                    {
                        "Namespace": "aws:autoscaling:launchconfiguration",
                        "OptionName": "IamInstanceProfile",
                        "Value": {
                            "Ref": "MyInstanceProfile"
                        }
                    }
                ],
                "SolutionStackName": "solution-stack"
            }
        },
        "sampleEnvironment": {
            "Type": "AWS::ElasticBeanstalk::Environment",
            "Properties": {
                "ApplicationName": {
                    "Ref": "sampleApplication"
                },
                "Description": "AWS ElasticBeanstalk Sample Environment",
                "TemplateName": {
                    "Ref": "sampleConfigurationTemplate"
                },
                "VersionLabel": {
                    "Ref": "sampleApplicationVersion"
                }
            }
        },
        "MyInstanceRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "ec2.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Description": "Beanstalk EC2 role",
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/AWSElasticBeanstalkWebTier",
                    "arn:aws:iam::aws:policy/AWSElasticBeanstalkMulticontainerDocker",
                    "arn:aws:iam::aws:policy/AWSElasticBeanstalkWorkerTier"
                ]
            }
        },
        "MyInstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Roles": [
                    {
                        "Ref": "MyInstanceRole"
                    }
                ]
            }
        }
    }
}
```

### YAML<a name="quickref-elasticbeanstalk-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  sampleApplication:
    Type: AWS::ElasticBeanstalk::Application
    Properties:
      Description: AWS Elastic Beanstalk Sample Application
  sampleApplicationVersion:
    Type: AWS::ElasticBeanstalk::ApplicationVersion
    Properties:
      ApplicationName:
        Ref: sampleApplication
      Description: AWS ElasticBeanstalk Sample Application Version
      SourceBundle:
        S3Bucket: !Sub "elasticbeanstalk-samples-${AWS::Region}"
        S3Key: php-newsample-app.zip
  sampleConfigurationTemplate:
    Type: AWS::ElasticBeanstalk::ConfigurationTemplate
    Properties:
      ApplicationName:
        Ref: sampleApplication
      Description: AWS ElasticBeanstalk Sample Configuration Template
      OptionSettings:
      - Namespace: aws:autoscaling:asg
        OptionName: MinSize
        Value: '2'
      - Namespace: aws:autoscaling:asg
        OptionName: MaxSize
        Value: '6'
      - Namespace: aws:elasticbeanstalk:environment
        OptionName: EnvironmentType
        Value: LoadBalanced
      - Namespace: aws:autoscaling:launchconfiguration
        OptionName: IamInstanceProfile
        Value: !Ref MyInstanceProfile        
      SolutionStackName: solution-stack
  sampleEnvironment:
    Type: AWS::ElasticBeanstalk::Environment
    Properties:
      ApplicationName:
        Ref: sampleApplication
      Description: AWS ElasticBeanstalk Sample Environment
      TemplateName:
        Ref: sampleConfigurationTemplate
      VersionLabel:
        Ref: sampleApplicationVersion
  MyInstanceRole:
    Type: AWS::IAM::Role
    Properties: 
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - ec2.amazonaws.com
            Action:
              - sts:AssumeRole
      Description: Beanstalk EC2 role
      ManagedPolicyArns: 
        - arn:aws:iam::aws:policy/AWSElasticBeanstalkWebTier
        - arn:aws:iam::aws:policy/AWSElasticBeanstalkMulticontainerDocker
        - arn:aws:iam::aws:policy/AWSElasticBeanstalkWorkerTier
  MyInstanceProfile:
    Type: AWS::IAM::InstanceProfile
    Properties: 
      Roles:
        - !Ref MyInstanceRole
```