# Amazon CloudWatch Logs template snippets<a name="quickref-cloudwatchlogs"></a>

Amazon CloudWatch Logs can monitor your system, application, and custom log files from Amazon EC2 instances or other sources\. You can use AWS CloudFormation to provision and manage log groups and metric filters\. For more information about getting started with Amazon CloudWatch Logs, see [Monitoring system, application, and custom log files ](https://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/WhatIsCloudWatchLogs.html) in the *Amazon CloudWatch User Guide*\.

**Topics**
+ [Send logs to CloudWatch Logs from a Linux instance](#quickref-cloudwatchlogs-example1)
+ [Send logs to CloudWatch Logs from a Windows instance](#quickref-cloudwatchlogs-example2)
+ [See also](#w2ab1c23c21c35c11)

## Send logs to CloudWatch Logs from a Linux instance<a name="quickref-cloudwatchlogs-example1"></a>

The following template describes a web server and its custom metrics\. Log events from the web server's log provides the data for the custom metrics\. To send log events to a custom metric, the `UserData` field installs a CloudWatch Logs agent on the Amazon EC2 instance\. The configuration information for the agent, such as the location of the server log file, the log group name, and the log stream name, are defined in the `/tmp/cwlogs/apacheaccess.conf` file\. The log stream is created after the web server starts sending log events to the `/var/log/httpd/access_log` file\.

**Note**  
A note about permissions: The `WebServerHost` instance references the `LogRoleInstanceProfile` instance profile, which in turn references the `LogRole` role\. `LogRole` specifies the `s3:GetObject` permission for *arn:aws:s3:::\**\.  
This permission is required because `WebServerHost` downloads the CloudWatch Logs agent \(`awslogs-agent-setup.py`\) from Amazon S3 in the `UserData` section\.

The two metric filters describe how the log information is transformed into CloudWatch metrics\. The 404 metric counts the number of 404 occurrences\. The size metric tracks the size of a request\. The two CloudWatch alarms will send notifications if there are more than two 404s within 2 minutes or if the average request size is over 3500 KB over 10 minutes\.

### JSON<a name="quickref-cloudwatchlogs-example.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for CloudWatch Logs.",
    "Parameters": {
        "KeyName": {
            "Description": "Name of an existing EC2 KeyPair to enable SSH access to the instances",
            "Type": "AWS::EC2::KeyPair::KeyName",
            "ConstraintDescription": "must be the name of an existing EC2 KeyPair."
        },
        "SSHLocation": {
            "Description": "The IP address range that can be used to SSH to the EC2 instances",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "0.0.0.0/0",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        },
        "OperatorEmail": {
            "Description": "Email address to notify if there are any scaling operations",
            "Type": "String"
        }
    },
    "Mappings": {
        "RegionMap": {
            "us-east-1": {
                "AMI": "ami-0ff8a91507f77f867"
            },
            "us-west-1": {
                "AMI": "ami-0bdb828fd58c52235"
            },
            "us-west-2": {
                "AMI": "ami-a0cfeed8"
            },
            "eu-west-1": {
                "AMI": "ami-047bb4163c506cd98"
            },
            "ap-southeast-1": {
                "AMI": "ami-08569b978cc4dfa10"
            },
            "ap-southeast-2": {
                "AMI": "ami-09b42976632b27e9b"
            },
            "ap-northeast-1": {
                "AMI": "ami-06cd52961ce9f0d85"
            },
            "sa-east-1": {
                "AMI": "ami-07b14488da8ea02a0"
            },
            "eu-central-1": {
                "AMI": "ami-0233214e13e500f77"
            }
        }
    },
    "Resources": {
        "LogRole": {
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
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "LogRolePolicy",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": [
                                        "logs:Create*",
                                        "logs:PutLogEvents",
                                        "s3:GetObject"
                                    ],
                                    "Resource": [
                                        "arn:aws:logs:*:*:*",
                                        "arn:aws:s3:::*"
                                    ]
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "LogRoleInstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Path": "/",
                "Roles": [
                    {
                        "Ref": "LogRole"
                    }
                ]
            }
        },
        "WebServerSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable HTTP access via port 80 and SSH access via port 22",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 80,
                        "ToPort": 80,
                        "CidrIp": "0.0.0.0/0"
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 22,
                        "ToPort": 22,
                        "CidrIp": {
                            "Ref": "SSHLocation"
                        }
                    }
                ]
            }
        },
        "WebServerHost": {
            "Type": "AWS::EC2::Instance",
            "Metadata": {
                "Comment": "Install a simple PHP application",
                "AWS::CloudFormation::Init": {
                    "config": {
                        "packages": {
                            "yum": {
                                "httpd": [],
                                "php": []
                            }
                        },
                        "files": {
                            "/tmp/cwlogs/apacheaccess.conf": {
                                "content": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "[general]\n",
                                            "state_file= /var/awslogs/agent-state\n",
                                            "[/var/log/httpd/access_log]\n",
                                            "file = /var/log/httpd/access_log\n",
                                            "log_group_name = ",
                                            {
                                                "Ref": "WebServerLogGroup"
                                            },
                                            "\n",
                                            "log_stream_name = {instance_id}/apache.log\n",
                                            "datetime_format = %d/%b/%Y:%H:%M:%S"
                                        ]
                                    ]
                                },
                                "mode": "000400",
                                "owner": "apache",
                                "group": "apache"
                            },
                            "/var/www/html/index.php": {
                                "content": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "<?php\n",
                                            "echo '<h1>AWS CloudFormation sample PHP application</h1>';\n",
                                            "?>\n"
                                        ]
                                    ]
                                },
                                "mode": "000644",
                                "owner": "apache",
                                "group": "apache"
                            },
                            "/etc/cfn/cfn-hup.conf": {
                                "content": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "[main]\n",
                                            "stack=",
                                            {
                                                "Ref": "AWS::StackId"
                                            },
                                            "\n",
                                            "region=",
                                            {
                                                "Ref": "AWS::Region"
                                            },
                                            "\n"
                                        ]
                                    ]
                                },
                                "mode": "000400",
                                "owner": "root",
                                "group": "root"
                            },
                            "/etc/cfn/hooks.d/cfn-auto-reloader.conf": {
                                "content": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "[cfn-auto-reloader-hook]\n",
                                            "triggers=post.update\n",
                                            "path=Resources.WebServerHost.Metadata.AWS::CloudFormation::Init\n",
                                            "action=/opt/aws/bin/cfn-init -s ",
                                            {
                                                "Ref": "AWS::StackId"
                                            },
                                            " -r WebServerHost ",
                                            " --region     ",
                                            {
                                                "Ref": "AWS::Region"
                                            },
                                            "\n",
                                            "runas=root\n"
                                        ]
                                    ]
                                }
                            }
                        },
                        "services": {
                            "sysvinit": {
                                "httpd": {
                                    "enabled": "true",
                                    "ensureRunning": "true"
                                },
                                "sendmail": {
                                    "enabled": "false",
                                    "ensureRunning": "false"
                                }
                            }
                        }
                    }
                }
            },
            "CreationPolicy": {
                "ResourceSignal": {
                    "Timeout": "PT5M"
                }
            },
            "Properties": {
                "ImageId": {
                    "Fn::FindInMap": [
                        "RegionMap",
                        {
                            "Ref": "AWS::Region"
                        },
                        "AMI"
                    ]
                },
                "KeyName": {
                    "Ref": "KeyName"
                },
                "InstanceType": "t1.micro",
                "SecurityGroups": [
                    {
                        "Ref": "WebServerSecurityGroup"
                    }
                ],
                "IamInstanceProfile": {
                    "Ref": "LogRoleInstanceProfile"
                },
                "UserData": {
                    "Fn::Base64": {
                        "Fn::Join": [
                            "",
                            [
                                "#!/bin/bash -xe\n",
                                "# Get the latest CloudFormation package\n",
                                "yum install -y aws-cfn-bootstrap\n",
                                "# Start cfn-init\n",
                                "/opt/aws/bin/cfn-init -s ",
                                {
                                    "Ref": "AWS::StackId"
                                },
                                " -r WebServerHost ",
                                " --region ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                " || error_exit 'Failed to run cfn-init'\n",
                                "# Start up the cfn-hup daemon to listen for changes to the EC2 instance metadata\n",
                                "/opt/aws/bin/cfn-hup || error_exit 'Failed to start cfn-hup'\n",
                                "# Get the CloudWatch Logs agent\n",
                                "wget https://s3.amazonaws.com/aws-cloudwatch/downloads/latest/awslogs-agent-setup.py\n",
                                "# Install the CloudWatch Logs agent\n",
                                "python awslogs-agent-setup.py -n -r ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                " -c /tmp/cwlogs/apacheaccess.conf || error_exit 'Failed to run CloudWatch Logs agent setup'\n",
                                "# All done so signal success\n",
                                "/opt/aws/bin/cfn-signal -e $? ",
                                "         --stack ",
                                {
                                    "Ref": "AWS::StackName"
                                },
                                "         --resource WebServerHost ",
                                "         --region ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                "\n"
                            ]
                        ]
                    }
                }
            }
        },
        "WebServerLogGroup": {
            "Type": "AWS::Logs::LogGroup",
            "Properties": {
                "RetentionInDays": 7
            }
        },
        "404MetricFilter": {
            "Type": "AWS::Logs::MetricFilter",
            "Properties": {
                "LogGroupName": {
                    "Ref": "WebServerLogGroup"
                },
                "FilterPattern": "[ip, identity, user_id, timestamp, request, status_code = 404, size, ...]",
                "MetricTransformations": [
                    {
                        "MetricValue": "1",
                        "MetricNamespace": "test/404s",
                        "MetricName": "test404Count"
                    }
                ]
            }
        },
        "BytesTransferredMetricFilter": {
            "Type": "AWS::Logs::MetricFilter",
            "Properties": {
                "LogGroupName": {
                    "Ref": "WebServerLogGroup"
                },
                "FilterPattern": "[ip, identity, user_id, timestamp, request, status_code, size, ...]",
                "MetricTransformations": [
                    {
                        "MetricValue": "$size",
                        "MetricNamespace": "test/BytesTransferred",
                        "MetricName": "testBytesTransferred"
                    }
                ]
            }
        },
        "404Alarm": {
            "Type": "AWS::CloudWatch::Alarm",
            "Properties": {
                "AlarmDescription": "The number of 404s is greater than 2 over 2 minutes",
                "MetricName": "test404Count",
                "Namespace": "test/404s",
                "Statistic": "Sum",
                "Period": "60",
                "EvaluationPeriods": "2",
                "Threshold": "2",
                "AlarmActions": [
                    {
                        "Ref": "AlarmNotificationTopic"
                    }
                ],
                "ComparisonOperator": "GreaterThanThreshold"
            }
        },
        "BandwidthAlarm": {
            "Type": "AWS::CloudWatch::Alarm",
            "Properties": {
                "AlarmDescription": "The average volume of traffic is greater 3500 KB over 10 minutes",
                "MetricName": "testBytesTransferred",
                "Namespace": "test/BytesTransferred",
                "Statistic": "Average",
                "Period": "300",
                "EvaluationPeriods": "2",
                "Threshold": "3500",
                "AlarmActions": [
                    {
                        "Ref": "AlarmNotificationTopic"
                    }
                ],
                "ComparisonOperator": "GreaterThanThreshold"
            }
        },
        "AlarmNotificationTopic": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "Subscription": [
                    {
                        "Endpoint": {
                            "Ref": "OperatorEmail"
                        },
                        "Protocol": "email"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "InstanceId": {
            "Description": "The instance ID of the web server",
            "Value": {
                "Ref": "WebServerHost"
            }
        },
        "WebsiteURL": {
            "Value": {
                "Fn::Join": [
                    "",
                    [
                        "http://",
                        {
                            "Fn::GetAtt": [
                                "WebServerHost",
                                "PublicDnsName"
                            ]
                        }
                    ]
                ]
            },
            "Description": "URL for newly created LAMP stack"
        },
        "PublicIP": {
            "Description": "Public IP address of the web server",
            "Value": {
                "Fn::GetAtt": [
                    "WebServerHost",
                    "PublicIp"
                ]
            }
        },
        "CloudWatchLogGroupName": {
            "Description": "The name of the CloudWatch log group",
            "Value": {
                "Ref": "WebServerLogGroup"
            }
        }
    }
}
```

### YAML<a name="quickref-cloudwatchlogs-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Sample Template for CloudWatch Logs.
Parameters:
  KeyName:
    Description: Name of an existing EC2 KeyPair to enable SSH access to the instances
    Type: 'AWS::EC2::KeyPair::KeyName'
    ConstraintDescription: must be the name of an existing EC2 KeyPair.
  SSHLocation:
    Description: The IP address range that can be used to SSH to the EC2 instances
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 0.0.0.0/0
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  OperatorEmail:
    Description: Email address to notify if there are any scaling operations
    Type: String
Mappings:
  RegionMap:
    us-east-1:
      AMI: ami-0ff8a91507f77f867
    us-west-1:
      AMI: ami-0bdb828fd58c52235
    us-west-2:
      AMI: ami-a0cfeed8
    eu-west-1:
      AMI: ami-047bb4163c506cd98
    ap-southeast-1:
      AMI: ami-08569b978cc4dfa10
    ap-southeast-2:
      AMI: ami-09b42976632b27e9b
    ap-northeast-1:
      AMI: ami-06cd52961ce9f0d85
    sa-east-1:
      AMI: ami-07b14488da8ea02a0
    eu-central-1:
      AMI: ami-0233214e13e500f77
Resources:
  LogRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - ec2.amazonaws.com
            Action:
              - 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: LogRolePolicy
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action:
                  - 'logs:Create*'
                  - 'logs:PutLogEvents'
                  - 's3:GetObject'
                Resource:
                  - 'arn:aws:logs:*:*:*'
                  - 'arn:aws:s3:::*'
  LogRoleInstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref LogRole
  WebServerSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable HTTP access via port 80 and SSH access via port 22
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: !Ref SSHLocation
  WebServerHost:
    Type: 'AWS::EC2::Instance'
    Metadata:
      Comment: Install a simple PHP application
      'AWS::CloudFormation::Init':
        config:
          packages:
            yum:
              httpd: []
              php: []
          files:
            /tmp/cwlogs/apacheaccess.conf:
              content: !Join 
                - ''
                - - |
                    [general]
                  - |
                    state_file= /var/awslogs/agent-state
                  - |
                    [/var/log/httpd/access_log]
                  - |
                    file = /var/log/httpd/access_log
                  - 'log_group_name = '
                  - !Ref WebServerLogGroup
                  - |+

                  - |
                    log_stream_name = {instance_id}/apache.log
                  - 'datetime_format = %d/%b/%Y:%H:%M:%S'
              mode: '000400'
              owner: apache
              group: apache
            /var/www/html/index.php:
              content: !Join 
                - ''
                - - |
                    <?php
                  - |
                    echo '<h1>AWS CloudFormation sample PHP application</h1>';
                  - |
                    ?>
              mode: '000644'
              owner: apache
              group: apache
            /etc/cfn/cfn-hup.conf:
              content: !Join 
                - ''
                - - |
                    [main]
                  - stack=
                  - !Ref 'AWS::StackId'
                  - |+

                  - region=
                  - !Ref 'AWS::Region'
                  - |+

              mode: '000400'
              owner: root
              group: root
            /etc/cfn/hooks.d/cfn-auto-reloader.conf:
              content: !Join 
                - ''
                - - |
                    [cfn-auto-reloader-hook]
                  - |
                    triggers=post.update
                  - >
                    path=Resources.WebServerHost.Metadata.AWS::CloudFormation::Init
                  - 'action=/opt/aws/bin/cfn-init -s '
                  - !Ref 'AWS::StackId'
                  - ' -r WebServerHost '
                  - ' --region     '
                  - !Ref 'AWS::Region'
                  - |+

                  - |
                    runas=root
          services:
            sysvinit:
              httpd:
                enabled: 'true'
                ensureRunning: 'true'
              sendmail:
                enabled: 'false'
                ensureRunning: 'false'
    CreationPolicy:
      ResourceSignal:
        Timeout: PT5M
    Properties:
      ImageId: !FindInMap 
        - RegionMap
        - !Ref 'AWS::Region'
        - AMI
      KeyName: !Ref KeyName
      InstanceType: t1.micro
      SecurityGroups:
        - !Ref WebServerSecurityGroup
      IamInstanceProfile: !Ref LogRoleInstanceProfile
      UserData: !Base64 
        'Fn::Join':
          - ''
          - - |
              #!/bin/bash -xe
            - |
              # Get the latest CloudFormation package
            - |
              yum install -y aws-cfn-bootstrap
            - |
              # Start cfn-init
            - '/opt/aws/bin/cfn-init -s '
            - !Ref 'AWS::StackId'
            - ' -r WebServerHost '
            - ' --region '
            - !Ref 'AWS::Region'
            - |2
               || error_exit 'Failed to run cfn-init'
            - >
              # Start up the cfn-hup daemon to listen for changes to the EC2
              instance metadata
            - |
              /opt/aws/bin/cfn-hup || error_exit 'Failed to start cfn-hup'
            - |
              # Get the CloudWatch Logs agent
            - >
              wget
              https://s3.amazonaws.com/aws-cloudwatch/downloads/latest/awslogs-agent-setup.py
            - |
              # Install the CloudWatch Logs agent
            - 'python awslogs-agent-setup.py -n -r '
            - !Ref 'AWS::Region'
            - |2
               -c /tmp/cwlogs/apacheaccess.conf || error_exit 'Failed to run CloudWatch Logs agent setup'
            - |
              # All done so signal success
            - '/opt/aws/bin/cfn-signal -e $? '
            - '         --stack '
            - !Ref 'AWS::StackName'
            - '         --resource WebServerHost '
            - '         --region '
            - !Ref 'AWS::Region'
            - |+

  WebServerLogGroup:
    Type: 'AWS::Logs::LogGroup'
    Properties:
      RetentionInDays: 7
  404MetricFilter:
    Type: 'AWS::Logs::MetricFilter'
    Properties:
      LogGroupName: !Ref WebServerLogGroup
      FilterPattern: >-
        [ip, identity, user_id, timestamp, request, status_code = 404, size,
        ...]
      MetricTransformations:
        - MetricValue: '1'
          MetricNamespace: test/404s
          MetricName: test404Count
  BytesTransferredMetricFilter:
    Type: 'AWS::Logs::MetricFilter'
    Properties:
      LogGroupName: !Ref WebServerLogGroup
      FilterPattern: '[ip, identity, user_id, timestamp, request, status_code, size, ...]'
      MetricTransformations:
        - MetricValue: $size
          MetricNamespace: test/BytesTransferred
          MetricName: testBytesTransferred
  404Alarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      AlarmDescription: The number of 404s is greater than 2 over 2 minutes
      MetricName: test404Count
      Namespace: test/404s
      Statistic: Sum
      Period: '60'
      EvaluationPeriods: '2'
      Threshold: '2'
      AlarmActions:
        - !Ref AlarmNotificationTopic
      ComparisonOperator: GreaterThanThreshold
  BandwidthAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      AlarmDescription: The average volume of traffic is greater 3500 KB over 10 minutes
      MetricName: testBytesTransferred
      Namespace: test/BytesTransferred
      Statistic: Average
      Period: '300'
      EvaluationPeriods: '2'
      Threshold: '3500'
      AlarmActions:
        - !Ref AlarmNotificationTopic
      ComparisonOperator: GreaterThanThreshold
  AlarmNotificationTopic:
    Type: 'AWS::SNS::Topic'
    Properties:
      Subscription:
        - Endpoint: !Ref OperatorEmail
          Protocol: email
Outputs:
  InstanceId:
    Description: The instance ID of the web server
    Value: !Ref WebServerHost
  WebsiteURL:
    Value: !Join 
      - ''
      - - 'http://'
        - !GetAtt 
          - WebServerHost
          - PublicDnsName
    Description: URL for newly created LAMP stack
  PublicIP:
    Description: Public IP address of the web server
    Value: !GetAtt 
      - WebServerHost
      - PublicIp
  CloudWatchLogGroupName:
    Description: The name of the CloudWatch log group
    Value: !Ref WebServerLogGroup
```

## Send logs to CloudWatch Logs from a Windows instance<a name="quickref-cloudwatchlogs-example2"></a>

The following template configures CloudWatch Logs for a Windows 2012R2 instance\.

The CloudWatch Logs agent on Windows \(SSM agent on Windows 2012R2 and Windows 2016 AMIs\) only sends logs after it's started, so any logs that are generated before startup aren't sent\. To work around this, the template helps to ensure that the agent starts before any logs are written by:
+ Configuring the agent setup as the first `config` item in cfn\-init `configSets`\.
+ Using `waitAfterCompletion` to insert a pause after the command that starts the agent\.

### JSON<a name="quickref-cloudwatchlogs-example2.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Sample template that sets up and configures CloudWatch logs on Windows 2012R2 instance instance.",
    "Parameters": {
        "KeyPair": {
            "Description": "Name of an existing EC2 KeyPair to enable RDP access to the instances",
            "Type": "AWS::EC2::KeyPair::KeyName",
            "ConstraintDescription": "must be the name of an existing EC2 KeyPair."
        },
        "RDPLocation": {
            "Description": "The IP address range that can be used to RDP to the EC2 instances",
            "Type": "String",
            "MinLength": "9",
            "MaxLength": "18",
            "Default": "0.0.0.0/0",
            "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
            "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        },
        "OperatorEmail": {
            "Description": "Email address to notify if there are any scaling operations",
            "Type": "String"
        }
    },
    "Mappings": {
        "AWSAMIRegionMap": {
            "ap-northeast-1": {
                "WS2012R2": "ami-09e7006451ad8bf4d"
            },
            "ap-northeast-2": {
                "WS2012R2": "ami-0754980e4d02153f9"
            },
            "ap-south-1": {
                "WS2012R2": "ami-00ad91b37d56c1d08"
            },
            "ap-southeast-1": {
                "WS2012R2": "ami-09e7006451ad8bf4d"
            },
            "ap-southeast-2": {
                "WS2012R2": "ami-000d23d3067008aea"
            },
            "ca-central-1": {
                "WS2012R2": "ami-0d8e70862465b9da0"
            },
            "eu-central-1": {
                "WS2012R2": "ami-0c0f322f5676ba254"
            },
            "eu-west-1": {
                "WS2012R2": "ami-0a46adf18f8875ad6"
            },
            "eu-west-2": {
                "WS2012R2": "ami-0651428174d9438e9"
            },
            "sa-east-1": {
                "WS2012R2": "ami-08ebd138109a6c223"
            },
            "us-east-1": {
                "WS2012R2": "ami-0ef6fb504535468b2"
            },
            "us-east-2": {
                "WS2012R2": "ami-0f466c6044f510bd3"
            },
            "us-west-1": {
                "WS2012R2": "ami-026f68ef6465e6c09"
            },
            "us-west-2": {
                "WS2012R2": "ami-0274ca53943a86543"
            }
        }
    },
    "Resources": {
        "WebServerSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable HTTP access via port 80 and RDP access via port 3389",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "80",
                        "ToPort": "80",
                        "CidrIp": "0.0.0.0/0"
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "3389",
                        "ToPort": "3389",
                        "CidrIp": {
                            "Ref": "RDPLocation"
                        }
                    }
                ]
            }
        },
        "LogRole": {
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
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/AmazonSSMManagedInstanceCore"
                ],
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "LogRolePolicy",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": [
                                        "logs:Create*",
                                        "logs:PutLogEvents",
                                        "s3:GetObject"
                                    ],
                                    "Resource": [
                                        "arn:aws:logs:*:*:*",
                                        "arn:aws:s3:::*"
                                    ]
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "LogRoleInstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "Path": "/",
                "Roles": [
                    {
                        "Ref": "LogRole"
                    }
                ]
            }
        },
        "WebServerHost": {
            "Type": "AWS::EC2::Instance",
            "CreationPolicy": {
                "ResourceSignal": {
                    "Timeout": "PT15M"
                }
            },
            "Metadata": {
                "AWS::CloudFormation::Init": {
                    "configSets": {
                        "config": [
                            "00-ConfigureCWLogs",
                            "01-InstallWebServer",
                            "02-ConfigureApplication",
                            "03-Finalize"
                        ]
                    },
                    "00-ConfigureCWLogs": {
                        "files": {
                            "C:\\Program Files\\Amazon\\SSM\\Plugins\\awsCloudWatch\\AWS.EC2.Windows.CloudWatch.json": {
                                "content": {
                                    "Fn::Sub": "{\n  \"EngineConfiguration\": {\n      \"Components\": [\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"ApplicationEventLog\",\n              \"Parameters\": {\n                  \"Levels\": \"7\",\n                  \"LogName\": \"Application\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"SystemEventLog\",\n              \"Parameters\": {\n                  \"Levels\": \"7\",\n                  \"LogName\": \"System\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"SecurityEventLog\",\n              \"Parameters\": {\n                  \"Levels\": \"7\",\n                  \"LogName\": \"Security\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"EC2ConfigLog\",\n              \"Parameters\": {\n                  \"CultureName\": \"en-US\",\n                  \"Encoding\": \"ASCII\",\n                  \"Filter\": \"EC2ConfigLog.txt\",\n                  \"LogDirectoryPath\": \"C:\\\\Program Files\\\\Amazon\\\\Ec2ConfigService\\\\Logs\",\n                  \"TimeZoneKind\": \"UTC\",\n                  \"TimestampFormat\": \"yyyy-MM-ddTHH:mm:ss.fffZ:\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CfnInitLog\",\n              \"Parameters\": {\n                  \"CultureName\": \"en-US\",\n                  \"Encoding\": \"ASCII\",\n                  \"Filter\": \"cfn-init.log\",\n                  \"LogDirectoryPath\": \"C:\\\\cfn\\\\log\",\n                  \"TimeZoneKind\": \"Local\",\n                  \"TimestampFormat\": \"yyyy-MM-dd HH:mm:ss,fff\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"IISLogs\",\n              \"Parameters\": {\n                  \"CultureName\": \"en-US\",\n                  \"Encoding\": \"UTF-8\",\n                  \"Filter\": \"\",\n                  \"LineCount\": \"3\",\n                  \"LogDirectoryPath\": \"C:\\\\inetpub\\\\logs\\\\LogFiles\\\\W3SVC1\",\n                  \"TimeZoneKind\": \"UTC\",\n                  \"TimestampFormat\": \"yyyy-MM-dd HH:mm:ss\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.PerformanceCounterComponent.PerformanceCounterInputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"MemoryPerformanceCounter\",\n              \"Parameters\": {\n                  \"CategoryName\": \"Memory\",\n                  \"CounterName\": \"Available MBytes\",\n                  \"DimensionName\": \"\",\n                  \"DimensionValue\": \"\",\n                  \"InstanceName\": \"\",\n                  \"MetricName\": \"Memory\",\n                  \"Unit\": \"Megabytes\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchApplicationEventLog\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/ApplicationEventLog\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchSystemEventLog\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/SystemEventLog\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchSecurityEventLog\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/SecurityEventLog\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchEC2ConfigLog\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/EC2ConfigLog\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchCfnInitLog\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/CfnInitLog\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatchIISLogs\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"LogGroup\": \"${LogGroup}\",\n                  \"LogStream\": \"{instance_id}/IISLogs\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          },\n          {\n              \"FullName\": \"AWS.EC2.Windows.CloudWatch.CloudWatch.CloudWatchOutputComponent,AWS.EC2.Windows.CloudWatch\",\n              \"Id\": \"CloudWatch\",\n              \"Parameters\": {\n                  \"AccessKey\": \"\",\n                  \"NameSpace\": \"Windows/Default\",\n                  \"Region\": \"${AWS::Region}\",\n                  \"SecretKey\": \"\"\n              }\n          }\n      ],\n      \"Flows\": {\n          \"Flows\": [\n              \"ApplicationEventLog,CloudWatchApplicationEventLog\",\n              \"SystemEventLog,CloudWatchSystemEventLog\",\n              \"SecurityEventLog,CloudWatchSecurityEventLog\",\n              \"EC2ConfigLog,CloudWatchEC2ConfigLog\",\n              \"CfnInitLog,CloudWatchCfnInitLog\",\n              \"IISLogs,CloudWatchIISLogs\",\n              \"MemoryPerformanceCounter,CloudWatch\"\n          ]\n      },\n      \"PollInterval\": \"00:00:05\"\n  },\n  \"IsEnabled\": true\n}\n"
                                }
                            }
                        },
                        "commands": {
                            "0-enableSSM": {
                                "command": "powershell.exe -Command \"Set-Service -Name AmazonSSMAgent -StartupType Automatic\" ",
                                "waitAfterCompletion": "0"
                            },
                            "1-restartSSM": {
                                "command": "powershell.exe -Command \"Restart-Service AmazonSSMAgent \"",
                                "waitAfterCompletion": "30"
                            }
                        }
                    },
                    "01-InstallWebServer": {
                        "commands": {
                            "01_install_webserver": {
                                "command": "powershell.exe -Command \"Install-WindowsFeature Web-Server  -IncludeAllSubFeature\"",
                                "waitAfterCompletion": "0"
                            }
                        }
                    },
                    "02-ConfigureApplication": {
                        "files": {
                            "c:\\Inetpub\\wwwroot\\index.htm": {
                                "content": "<html> <head> <title>Test Application Page</title> </head> <body> <h1>Congratulations !! Your IIS server is configured.</h1> </body> </html>"
                            }
                        }
                    },
                    "03-Finalize": {
                        "commands": {
                            "00_signal_success": {
                                "command": {
                                    "Fn::Sub": "cfn-signal.exe -e 0 --resource WebServerHost --stack ${AWS::StackName} --region ${AWS::Region}"
                                },
                                "waitAfterCompletion": "0"
                            }
                        }
                    }
                }
            },
            "Properties": {
                "KeyName": {
                    "Ref": "KeyPair"
                },
                "ImageId": {
                    "Fn::FindInMap": [
                        "AWSAMIRegionMap",
                        {
                            "Ref": "AWS::Region"
                        },
                        "WS2012R2"
                    ]
                },
                "InstanceType": "t2.xlarge",
                "SecurityGroupIds": [
                    {
                        "Ref": "WebServerSecurityGroup"
                    }
                ],
                "IamInstanceProfile": {
                    "Ref": "LogRoleInstanceProfile"
                },
                "UserData": {
                    "Fn::Base64": {
                        "Fn::Sub": "<script>\nwmic product where \"description='Amazon SSM Agent' \" uninstall\nwmic product where \"description='aws-cfn-bootstrap' \" uninstall \nstart /wait c:\\\\Windows\\\\system32\\\\msiexec /passive /qn /i https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-win64-latest.msi\npowershell.exe -Command \"iwr https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/windows_amd64/AmazonSSMAgentSetup.exe  -UseBasicParsing -OutFile C:\\\\AmazonSSMAgentSetup.exe\"\nstart /wait C:\\\\AmazonSSMAgentSetup.exe /install /quiet\ncfn-init.exe -v -c config -s ${AWS::StackName} --resource WebServerHost --region ${AWS::Region} \n</script>\n"
                    }
                }
            }
        },
        "LogGroup": {
            "Type": "AWS::Logs::LogGroup",
            "Properties": {
                "RetentionInDays": 7
            }
        },
        "404MetricFilter": {
            "Type": "AWS::Logs::MetricFilter",
            "Properties": {
                "LogGroupName": {
                    "Ref": "LogGroup"
                },
                "FilterPattern": "[timestamps, serverip, method, uri, query, port, dash, clientip, useragent, status_code = 404, ...]",
                "MetricTransformations": [
                    {
                        "MetricValue": "1",
                        "MetricNamespace": "test/404s",
                        "MetricName": "test404Count"
                    }
                ]
            }
        },
        "404Alarm": {
            "Type": "AWS::CloudWatch::Alarm",
            "Properties": {
                "AlarmDescription": "The number of 404s is greater than 2 over 2 minutes",
                "MetricName": "test404Count",
                "Namespace": "test/404s",
                "Statistic": "Sum",
                "Period": "60",
                "EvaluationPeriods": "2",
                "Threshold": "2",
                "AlarmActions": [
                    {
                        "Ref": "AlarmNotificationTopic"
                    }
                ],
                "ComparisonOperator": "GreaterThanThreshold"
            }
        },
        "AlarmNotificationTopic": {
            "Type": "AWS::SNS::Topic",
            "Properties": {
                "Subscription": [
                    {
                        "Endpoint": {
                            "Ref": "OperatorEmail"
                        },
                        "Protocol": "email"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "InstanceId": {
            "Description": "The instance ID of the web server",
            "Value": {
                "Ref": "WebServerHost"
            }
        },
        "WebsiteURL": {
            "Value": {
                "Fn::Sub": "http://${WebServerHost.PublicDnsName}"
            },
            "Description": "URL for newly created IIS web server"
        },
        "PublicIP": {
            "Description": "Public IP address of the web server",
            "Value": {
                "Fn::GetAtt": [
                    "WebServerHost",
                    "PublicIp"
                ]
            }
        },
        "CloudWatchLogGroupName": {
            "Description": "The name of the CloudWatch log group",
            "Value": {
                "Ref": "LogGroup"
            }
        }
    }
}
```

### YAML<a name="quickref-cloudwatchlogs-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  Sample template that sets up and configures CloudWatch logs on Windows 2012R2
  instance instance.
Parameters:
  KeyPair:
    Description: Name of an existing EC2 KeyPair to enable RDP access to the instances
    Type: 'AWS::EC2::KeyPair::KeyName'
    ConstraintDescription: must be the name of an existing EC2 KeyPair.
  RDPLocation:
    Description: The IP address range that can be used to RDP to the EC2 instances
    Type: String
    MinLength: '9'
    MaxLength: '18'
    Default: 0.0.0.0/0
    AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  OperatorEmail:
    Description: Email address to notify if there are any scaling operations
    Type: String
Mappings:
  AWSAMIRegionMap:
    ap-northeast-1:
      WS2012R2: ami-09e7006451ad8bf4d
    ap-northeast-2:
      WS2012R2: ami-0754980e4d02153f9
    ap-south-1:
      WS2012R2: ami-00ad91b37d56c1d08
    ap-southeast-1:
      WS2012R2: ami-09e7006451ad8bf4d
    ap-southeast-2:
      WS2012R2: ami-000d23d3067008aea
    ca-central-1:
      WS2012R2: ami-0d8e70862465b9da0
    eu-central-1:
      WS2012R2: ami-0c0f322f5676ba254
    eu-west-1:
      WS2012R2: ami-0a46adf18f8875ad6
    eu-west-2:
      WS2012R2: ami-0651428174d9438e9
    sa-east-1:
      WS2012R2: ami-08ebd138109a6c223
    us-east-1:
      WS2012R2: ami-0ef6fb504535468b2
    us-east-2:
      WS2012R2: ami-0f466c6044f510bd3
    us-west-1:
      WS2012R2: ami-026f68ef6465e6c09
    us-west-2:
      WS2012R2: ami-0274ca53943a86543
Resources:
  WebServerSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable HTTP access via port 80 and RDP access via port 3389
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '80'
          ToPort: '80'
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: '3389'
          ToPort: '3389'
          CidrIp: !Ref RDPLocation
  LogRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - ec2.amazonaws.com
            Action:
              - 'sts:AssumeRole'
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/AmazonSSMManagedInstanceCore'
      Path: /
      Policies:
        - PolicyName: LogRolePolicy
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action:
                  - 'logs:Create*'
                  - 'logs:PutLogEvents'
                  - 's3:GetObject'
                Resource:
                  - 'arn:aws:logs:*:*:*'
                  - 'arn:aws:s3:::*'
  LogRoleInstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref LogRole
  WebServerHost:
    Type: 'AWS::EC2::Instance'
    CreationPolicy:
      ResourceSignal:
        Timeout: PT15M
    Metadata:
      'AWS::CloudFormation::Init':
        configSets:
          config:
            - 00-ConfigureCWLogs
            - 01-InstallWebServer
            - 02-ConfigureApplication
            - 03-Finalize
        00-ConfigureCWLogs:
          files:
            'C:\Program Files\Amazon\SSM\Plugins\awsCloudWatch\AWS.EC2.Windows.CloudWatch.json':
              content: !Sub |
                {
                  "EngineConfiguration": {
                      "Components": [
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "ApplicationEventLog",
                              "Parameters": {
                                  "Levels": "7",
                                  "LogName": "Application"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "SystemEventLog",
                              "Parameters": {
                                  "Levels": "7",
                                  "LogName": "System"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.EventLog.EventLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "SecurityEventLog",
                              "Parameters": {
                                  "Levels": "7",
                                  "LogName": "Security"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "EC2ConfigLog",
                              "Parameters": {
                                  "CultureName": "en-US",
                                  "Encoding": "ASCII",
                                  "Filter": "EC2ConfigLog.txt",
                                  "LogDirectoryPath": "C:\\Program Files\\Amazon\\Ec2ConfigService\\Logs",
                                  "TimeZoneKind": "UTC",
                                  "TimestampFormat": "yyyy-MM-ddTHH:mm:ss.fffZ:"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "CfnInitLog",
                              "Parameters": {
                                  "CultureName": "en-US",
                                  "Encoding": "ASCII",
                                  "Filter": "cfn-init.log",
                                  "LogDirectoryPath": "C:\\cfn\\log",
                                  "TimeZoneKind": "Local",
                                  "TimestampFormat": "yyyy-MM-dd HH:mm:ss,fff"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CustomLog.CustomLogInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "IISLogs",
                              "Parameters": {
                                  "CultureName": "en-US",
                                  "Encoding": "UTF-8",
                                  "Filter": "",
                                  "LineCount": "3",
                                  "LogDirectoryPath": "C:\\inetpub\\logs\\LogFiles\\W3SVC1",
                                  "TimeZoneKind": "UTC",
                                  "TimestampFormat": "yyyy-MM-dd HH:mm:ss"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.PerformanceCounterComponent.PerformanceCounterInputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "MemoryPerformanceCounter",
                              "Parameters": {
                                  "CategoryName": "Memory",
                                  "CounterName": "Available MBytes",
                                  "DimensionName": "",
                                  "DimensionValue": "",
                                  "InstanceName": "",
                                  "MetricName": "Memory",
                                  "Unit": "Megabytes"
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchApplicationEventLog",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/ApplicationEventLog",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchSystemEventLog",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/SystemEventLog",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchSecurityEventLog",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/SecurityEventLog",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchEC2ConfigLog",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/EC2ConfigLog",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchCfnInitLog",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/CfnInitLog",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatchLogsOutput,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatchIISLogs",
                              "Parameters": {
                                  "AccessKey": "",
                                  "LogGroup": "${LogGroup}",
                                  "LogStream": "{instance_id}/IISLogs",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          },
                          {
                              "FullName": "AWS.EC2.Windows.CloudWatch.CloudWatch.CloudWatchOutputComponent,AWS.EC2.Windows.CloudWatch",
                              "Id": "CloudWatch",
                              "Parameters": {
                                  "AccessKey": "",
                                  "NameSpace": "Windows/Default",
                                  "Region": "${AWS::Region}",
                                  "SecretKey": ""
                              }
                          }
                      ],
                      "Flows": {
                          "Flows": [
                              "ApplicationEventLog,CloudWatchApplicationEventLog",
                              "SystemEventLog,CloudWatchSystemEventLog",
                              "SecurityEventLog,CloudWatchSecurityEventLog",
                              "EC2ConfigLog,CloudWatchEC2ConfigLog",
                              "CfnInitLog,CloudWatchCfnInitLog",
                              "IISLogs,CloudWatchIISLogs",
                              "MemoryPerformanceCounter,CloudWatch"
                          ]
                      },
                      "PollInterval": "00:00:05"
                  },
                  "IsEnabled": true
                }
          commands:
            0-enableSSM:
              command: >-
                powershell.exe -Command "Set-Service -Name AmazonSSMAgent
                -StartupType Automatic" 
              waitAfterCompletion: '0'
            1-restartSSM:
              command: powershell.exe -Command "Restart-Service AmazonSSMAgent "
              waitAfterCompletion: '30'
        01-InstallWebServer:
          commands:
            01_install_webserver:
              command: >-
                powershell.exe -Command "Install-WindowsFeature Web-Server 
                -IncludeAllSubFeature"
              waitAfterCompletion: '0'
        02-ConfigureApplication:
          files:
            'c:\Inetpub\wwwroot\index.htm':
              content: >-
                <html> <head> <title>Test Application Page</title> </head>
                <body> <h1>Congratulations !! Your IIS server is
                configured.</h1> </body> </html>
        03-Finalize:
          commands:
            00_signal_success:
              command: !Sub >-
                cfn-signal.exe -e 0 --resource WebServerHost --stack
                ${AWS::StackName} --region ${AWS::Region}
              waitAfterCompletion: '0'
    Properties:
      KeyName: !Ref KeyPair
      ImageId: !FindInMap 
        - AWSAMIRegionMap
        - !Ref 'AWS::Region'
        - WS2012R2
      InstanceType: t2.xlarge
      SecurityGroupIds:
        - !Ref WebServerSecurityGroup
      IamInstanceProfile: !Ref LogRoleInstanceProfile
      UserData: !Base64 
        'Fn::Sub': >
          <script>

          wmic product where "description='Amazon SSM Agent' " uninstall

          wmic product where "description='aws-cfn-bootstrap' " uninstall 

          start /wait c:\\Windows\\system32\\msiexec /passive /qn /i
          https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-win64-latest.msi

          powershell.exe -Command "iwr
          https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/windows_amd64/AmazonSSMAgentSetup.exe 
          -UseBasicParsing -OutFile C:\\AmazonSSMAgentSetup.exe"

          start /wait C:\\AmazonSSMAgentSetup.exe /install /quiet

          cfn-init.exe -v -c config -s ${AWS::StackName} --resource
          WebServerHost --region ${AWS::Region} 

          </script>
  LogGroup:
    Type: 'AWS::Logs::LogGroup'
    Properties:
      RetentionInDays: 7
  404MetricFilter:
    Type: 'AWS::Logs::MetricFilter'
    Properties:
      LogGroupName: !Ref LogGroup
      FilterPattern: >-
        [timestamps, serverip, method, uri, query, port, dash, clientip,
        useragent, status_code = 404, ...]
      MetricTransformations:
        - MetricValue: '1'
          MetricNamespace: test/404s
          MetricName: test404Count
  404Alarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      AlarmDescription: The number of 404s is greater than 2 over 2 minutes
      MetricName: test404Count
      Namespace: test/404s
      Statistic: Sum
      Period: '60'
      EvaluationPeriods: '2'
      Threshold: '2'
      AlarmActions:
        - !Ref AlarmNotificationTopic
      ComparisonOperator: GreaterThanThreshold
  AlarmNotificationTopic:
    Type: 'AWS::SNS::Topic'
    Properties:
      Subscription:
        - Endpoint: !Ref OperatorEmail
          Protocol: email
Outputs:
  InstanceId:
    Description: The instance ID of the web server
    Value: !Ref WebServerHost
  WebsiteURL:
    Value: !Sub 'http://${WebServerHost.PublicDnsName}'
    Description: URL for newly created IIS web server
  PublicIP:
    Description: Public IP address of the web server
    Value: !GetAtt 
      - WebServerHost
      - PublicIp
  CloudWatchLogGroupName:
    Description: The name of the CloudWatch log group
    Value: !Ref LogGroup
```

## See also<a name="w2ab1c23c21c35c11"></a>

For more information about CloudWatch Logs resources, see [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html) or [AWS::Logs::MetricFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-metricfilter.html)\.