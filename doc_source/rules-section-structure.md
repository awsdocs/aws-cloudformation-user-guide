# Rules<a name="rules-section-structure"></a>

The optional `Rules` section validates a parameter or a combination of parameters passed to a template during a stack creation or stack update\. To use template rules, explicitly declare `Rules` in your template followed by an assertion\. Use the rules section to validate parameter values before creating or updating resources\. 

## Working with rules<a name="w7739ab1c27c15c19b5"></a>

Each template rule consists of two properties:
+ *Rule condition* \(optional\) — determines when a rule takes effect\. 
+ *Assertions* \(required\) — describes what values users can specify for a particular parameter\. 

A rule can include a `RuleCondition` property and must include an `Assertions` property\. For each rule, you can define only one rule condition\. You can define one or more asserts within the `Assertions` property\. If you don't define a rule condition, the rule's assertions always take effect\. 

## Rule\-specific intrinsic functions<a name="rules-specific-intrinsic-section-structure"></a>

To define a rule condition and assertions, use *rule\-specific intrinsic functions*, which are functions that can only be used in the `Rules` section of a template\. You can nest functions, but the final result of a rule condition or assertion must be either true or false\. 

You can use the following rule\-specific intrinsic functions to define rule conditions and assertions:
+ `[Fn::And](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-and)`
+ `[Fn::Contains](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-Contains)`
+ `[Fn::EachMemberEquals](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-EachMemberEquals)`
+ `[Fn::EachMemberIn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-EachMemberIn)`
+ `[Fn::Equals](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-equals)`
+ `[Fn::If](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-if)`
+ `[Fn::Not](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-not)`
+ `[Fn::Or](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-or)`
+ `[Fn::RefAll](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-refall)`
+ `[Fn::ValueOf](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-valueof)`
+ `[Fn::ValueOfAll](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-rules.html#fn-valueofall)`

Rule\-specific intrinsic functions are used in the condition or assertions of a rule\. The condition property determines if AWS CloudFormation applies the assertions\. If the condition evaluates to `true`, AWS CloudFormation evaluates the assertions to verify whether a parameter value is valid when a provisioned product is created or updated\. If a parameter value is invalid, AWS CloudFormation does not create or update the stack\. If the condition evaluates to `false`, AWS CloudFormation doesn't check the parameter value and proceeds with the stack operation\.

## Syntax<a name="template-constraint-rules-syntax"></a>

### JSON<a name="rules-section-structure-syntax.json"></a>

The `Rules` section of a template consists of the key name `Rules`, followed by a single colon\. You must use braces to enclose all rule declarations\. If you declare multiple rules, they are delimited by commas\. For each rule, you declare a logical name in quotation marks followed by a colon and braces that enclose the rule condition and assertions\. 

```
{
    "Rules": {
        "Rule01": {
            "RuleCondition": {
                "rule-specific intrinsic function": "Value01"
            },
            "Assertions": [
                {
                    "Assert": {
                        "rule-specific intrinsic function": "Value02"
                    },
                    "AssertDescription": "Information about this assert"
                },
                {
                    "Assert": {
                        "rule-specific intrinsic function": "Value03"
                    },
                    "AssertDescription": "Information about this assert"
                }
            ]
        },
        "Rule02": {
            "Assertions": [
                {
                    "Assert": {
                        "rule-specific intrinsic function": "Value04"
                    },
                    "AssertDescription": "Information about this assert"
                }
            ]
        }
    }
}
```

### YAML<a name="rules-section-structure-syntax.yaml"></a>

```
Rules:
  Rule01:
    RuleCondition:
      rule-specific intrinsic function: Value01
    Assertions:
      - Assert:
          rule-specific intrinsic function: Value02
        AssertDescription: Information about this assert
      - Assert:
          rule-specific intrinsic function: Value03
        AssertDescription: Information about this assert
  Rule02:
    Assertions:
      - Assert:
          rule-specific intrinsic function: Value04
        AssertDescription: Information about this assert
```

## Examples<a name="template-constraint-rules-example"></a>

### Conditionally verify a parameter value<a name="template-constraint-rules-example-verify"></a>

In the following example, the two rules check the value of the `InstanceType` parameter\. Depending on the value of the environment parameter \(`test` or `prod`\), the user must specify `a1.medium` or `a1.large` for the `InstanceType` parameter\. The `InstanceType` and `Environment` parameters must be declared in the `Parameters` section of the same template\.

#### Example JSON<a name="rules-section-example-syntax.json"></a>

```
{
    "Rules": {
        "testInstanceType": {
            "RuleCondition": {
                "Fn::Equals": [
                    {
                        "Ref": "Environment"
                    },
                    "test"
                ]
            },
            "Assertions": [
                {
                    "Assert": {
                        "Fn::Contains": [
                            [
                                "a1.medium"
                            ],
                            {
                                "Ref": "InstanceType"
                            }
                        ]
                    },
                    "AssertDescription": "For a test environment, the instance type must be a1.medium"
                }
            ]
        },
        "prodInstanceType": {
            "RuleCondition": {
                "Fn::Equals": [
                    {
                        "Ref": "Environment"
                    },
                    "prod"
                ]
            },
            "Assertions": [
                {
                    "Assert": {
                        "Fn::Contains": [
                            [
                                "a1.large"
                            ],
                            {
                                "Ref": "InstanceType"
                            }
                        ]
                    },
                    "AssertDescription": "For a production environment, the instance type must be a1.large"
                }
            ]
        }
    }
}
```

#### Example YAML<a name="rules-section-example-syntax.yaml"></a>

```
Rules:
  testInstanceType:
    RuleCondition: !Equals 
      - !Ref Environment
      - test
    Assertions:
      - Assert:
          'Fn::Contains':
            - - a1.medium
            - !Ref InstanceType
        AssertDescription: 'For a test environment, the instance type must be a1.medium'
  prodInstanceType:
    RuleCondition: !Equals 
      - !Ref Environment
      - prod
    Assertions:
      - Assert:
          'Fn::Contains':
            - - a1.large
            - !Ref InstanceType
        AssertDescription: 'For a production environment, the instance type must be a1.large'
```

## Cross\-parameter validation<a name="template-cross-parameter-rules-example"></a>

The following template example, creates a sample web site that uses Amazon EC2 Auto Scaling and Elastic Load Balancing and is configured to use multiple Availability Zones\. The template also contains CloudWatch alarms that execute scaling policies to add or remove instances from the Auto Scaling group when the defined thresholds are exceeded\. This template creates one or more Amazon EC2 instances\. 

**Note**  
You will be billed for the AWS resources used if you create a stack from this template\.

### Example JSON<a name="rules-section-example-syntax.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation Sample Template for using Assertions: Create a load balanced, Auto Scaled sample website where the instances are locked down to only accept traffic from the load balancer. This example creates an Auto Scaling group behind a load balancer with a health check. The web site is available on port 80 or 443 based on the input."
    "Parameters": {
        "VpcId": {
            "Type": "AWS::EC2::VPC::Id",
            "Description": "VpcId of your existing Virtual Private Cloud (VPC)",
            "ConstraintDescription": "must be the VPC Id of an existing Virtual Private Cloud."
        },
        "Subnets": {
            "Type": "List<AWS::EC2::Subnet::Id>",
            "Description": "The list of SubnetIds in your Virtual Private Cloud (VPC)",
            "ConstraintDescription": "must be a list of at least two existing subnets associated with at least two different availability zones. They should be residing in the selected Virtual Private Cloud."
        },
        "InstanceType": {
            "Description": "WebServer EC2 instance type",
            "Type": "String",
            "Default": "t2.small",
            "AllowedValues": [
                "t2.nano",
                "t2.micro",
                "t2.small",
                "t2.medium",
                "t2.large",
                "m4.large",
                "m4.xlarge",
                "m4.2xlarge",
                "m4.4xlarge",
                "m4.10xlarge",
                "m3.medium",
                "m3.large",
                "m3.xlarge",
                "m3.2xlarge",
                "c4.large",
                "c4.xlarge",
                "c4.2xlarge",
                "c4.4xlarge",
                "c4.8xlarge",
                "c3.large",
                "c3.xlarge",
                "c3.2xlarge",
                "c3.4xlarge",
                "c3.8xlarge",
                "r3.large",
                "r3.xlarge"
            ],
            "ConstraintDescription": "must be a valid EC2 instance type."
        },
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
        "UseSSL": {
            "AllowedValues": [
                "Yes",
                "No"
            ],
            "ConstraintDescription": "Select Yes to create a HTTPS Listener",
            "Default": "No",
            "Description": "Select \"Yes\" to implement SSL, \"No\" to skip (default).",
            "Type": "String"
        },
        "ALBSSLCertificateARN": {
            "Default": "",
            "Description": "[Optional] The ARN of the SSL certificate to be used for the Application Load Balancer",
            "Type": "String"
        },
        "HostedZoneName": {
            "AllowedPattern": "^$|(([a-zA-Z0-9]|[a-zA-Z0-9][a-zA-Z0-9\\-]*[a-zA-Z0-9])\\.)*([A-Za-z0-9]|[A-Za-z0-9][A-Za-z0-9\\-]*[A-Za-z0-9])$",
            "Default": "",
            "Description": "[Optional] The domain name of a valid Hosted Zone on AWS.",
            "Type": "String"
        }
    },
    "Conditions": {
        "UseALBSSL": {
            "Fn::Not": [
                {
                    "Fn::Equals": [
                        {
                            "Ref": "UseSSL"
                        },
                        "Yes"
                    ]
                }
            ]
        }
    },
    "Rules": {
        "SubnetsInVPC": {
            "Assertions": [
                {
                    "Assert": {
                        "Fn::EachMemberIn": [
                            {
                                "Fn::ValueOfAll": [
                                    "AWS::EC2::Subnet::Id",
                                    "VpcId"
                                ]
                            },
                            {
                                "Fn::RefAll": "AWS::EC2::VPC::Id"
                            }
                        ]
                    },
                    "AssertDescription": "All subnets must in the VPC"
                }
            ]
        },
        "ValidateHostedZone": {
            "RuleCondition": {
                "Fn::Equals": [
                    {
                        "Ref": "UseSSL"
                    },
                    "Yes"
                ]
            },
            "Assertions": [
                {
                    "Assert": {
                        "Fn::Not": [
                            {
                                "Fn::Equals": [
                                    {
                                        "Ref": "ALBSSLCertificateARN"
                                    },
                                    ""
                                ]
                            }
                        ]
                    },
                    "AssertDescription": "ACM Certificate value cannot be empty if SSL is required"
                },
                {
                    "Assert": {
                        "Fn::Not": [
                            {
                                "Fn::Equals": [
                                    {
                                        "Ref": "HostedZoneName"
                                    },
                                    ""
                                ]
                            }
                        ]
                    },
                    "AssertDescription": "Route53 Hosted Zone Name is mandatory when SSL is required"
                }
            ]
        }
    },
    "Mappings": {
        "AWSAMIRegionMap": {
            "AMI": {
                "AMZNLINUXHVM": "amzn-ami-hvm-2017.09.1.20171120-x86_64-gp2"
            },
            "ap-northeast-1": {
                "AMZNLINUXHVM": "ami-da9e2cbc"
            },
            "ap-northeast-2": {
                "AMZNLINUXHVM": "ami-1196317f"
            },
            "ap-south-1": {
                "AMZNLINUXHVM": "ami-d5c18eba"
            },
            "ap-southeast-1": {
                "AMZNLINUXHVM": "ami-c63d6aa5"
            },
            "ap-southeast-2": {
                "AMZNLINUXHVM": "ami-ff4ea59d"
            },
            "ca-central-1": {
                "AMZNLINUXHVM": "ami-d29e25b6"
            },
            "eu-central-1": {
                "AMZNLINUXHVM": "ami-bf2ba8d0"
            },
            "eu-west-1": {
                "AMZNLINUXHVM": "ami-1a962263"
            },
            "eu-west-2": {
                "AMZNLINUXHVM": "ami-e7d6c983"
            },
            "sa-east-1": {
                "AMZNLINUXHVM": "ami-286f2a44"
            },
            "us-east-1": {
                "AMZNLINUXHVM": "ami-55ef662f"
            },
            "us-east-2": {
                "AMZNLINUXHVM": "ami-15e9c770"
            },
            "us-west-1": {
                "AMZNLINUXHVM": "ami-a51f27c5"
            },
            "us-west-2": {
                "AMZNLINUXHVM": "ami-bf4193c7"
            }
        }
    },
    "Resources": {
        "WebServerGroup": {
            "Type": "AWS::AutoScaling::AutoScalingGroup",
            "Properties": {
                "VPCZoneIdentifier": {
                    "Ref": "Subnets"
                },
                "LaunchConfigurationName": {
                    "Ref": "LaunchConfig"
                },
                "MinSize": "2",
                "MaxSize": "2",
                "TargetGroupARNs": [
                    {
                        "Ref": "ALBTargetGroup"
                    }
                ]
            },
            "CreationPolicy": {
                "ResourceSignal": {
                    "Timeout": "PT15M"
                }
            },
            "UpdatePolicy": {
                "AutoScalingRollingUpdate": {
                    "MinInstancesInService": "1",
                    "MaxBatchSize": "1",
                    "PauseTime": "PT15M",
                    "WaitOnResourceSignals": "true"
                }
            }
        },
        "LaunchConfig": {
            "Type": "AWS::AutoScaling::LaunchConfiguration",
            "Metadata": {
                "Comment": "Install a simple application",
                "AWS::CloudFormation::Init": {
                    "config": {
                        "packages": {
                            "yum": {
                                "httpd": []
                            }
                        },
                        "files": {
                            "/var/www/html/index.html": {
                                "content": {
                                    "Fn::Join": [
                                        "\n",
                                        [
                                            "<h1>Congratulations, you have successfully launched the AWS CloudFormation sample.<h1>"
                                        ]
                                    ]
                                },
                                "mode": "000644",
                                "owner": "root",
                                "group": "root"
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
                                            "path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init\n",
                                            "action=/opt/aws/bin/cfn-init -v ",
                                            "         --stack ",
                                            {
                                                "Ref": "AWS::StackName"
                                            },
                                            "         --resource LaunchConfig ",
                                            "         --region ",
                                            {
                                                "Ref": "AWS::Region"
                                            },
                                            "\n",
                                            "runas=root\n"
                                        ]
                                    ]
                                },
                                "mode": "000400",
                                "owner": "root",
                                "group": "root"
                            }
                        },
                        "services": {
                            "sysvinit": {
                                "httpd": {
                                    "enabled": "true",
                                    "ensureRunning": "true"
                                },
                                "cfn-hup": {
                                    "enabled": "true",
                                    "ensureRunning": "true",
                                    "files": [
                                        "/etc/cfn/cfn-hup.conf",
                                        "/etc/cfn/hooks.d/cfn-auto-reloader.conf"
                                    ]
                                }
                            }
                        }
                    }
                }
            },
            "Properties": {
                "ImageId": {
                    "Fn::FindInMap": [
                        "AWSAMIRegionMap",
                        {
                            "Ref": "AWS::Region"
                        },
                        "AMZNLINUXHVM"
                    ]
                },
                "SecurityGroups": [
                    {
                        "Ref": "InstanceSecurityGroup"
                    }
                ],
                "InstanceType": {
                    "Ref": "InstanceType"
                },
                "KeyName": {
                    "Ref": "KeyName"
                },
                "UserData": {
                    "Fn::Base64": {
                        "Fn::Join": [
                            "",
                            [
                                "#!/bin/bash -xe\n",
                                "yum update -y aws-cfn-bootstrap\n",
                                "/opt/aws/bin/cfn-init -v ",
                                "         --stack ",
                                {
                                    "Ref": "AWS::StackName"
                                },
                                "         --resource LaunchConfig ",
                                "         --region ",
                                {
                                    "Ref": "AWS::Region"
                                },
                                "\n",
                                "/opt/aws/bin/cfn-signal -e $? ",
                                "         --stack ",
                                {
                                    "Ref": "AWS::StackName"
                                },
                                "         --resource WebServerGroup ",
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
        "ELBSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Allow access to the ELB",
                "VpcId": {
                    "Ref": "VpcId"
                },
                "SecurityGroupIngress": [
                    {
                        "Fn::If": [
                            "UseALBSSL",
                            {
                                "IpProtocol": "tcp",
                                "FromPort": "443",
                                "ToPort": "443",
                                "CidrIp": "0.0.0.0/0"
                            },
                            {
                                "IpProtocol": "tcp",
                                "FromPort": "80",
                                "ToPort": "80",
                                "CidrIp": "0.0.0.0/0"
                            }
                        ]
                    }
                ]
            }
        },
        "ApplicationLoadBalancer": {
            "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
            "Properties": {
                "Subnets": {
                    "Ref": "Subnets"
                },
                "SecurityGroups": [
                    {
                        "Ref": "ELBSecurityGroup"
                    }
                ]
            }
        },
        "ALBListener": {
            "Type": "AWS::ElasticLoadBalancingV2::Listener",
            "Properties": {
                "DefaultActions": [
                    {
                        "Type": "forward",
                        "TargetGroupArn": {
                            "Ref": "ALBTargetGroup"
                        }
                    }
                ],
                "LoadBalancerArn": {
                    "Ref": "ApplicationLoadBalancer"
                },
                "Port": {
                    "Fn::If": [
                        "UseALBSSL",
                        443,
                        80
                    ]
                },
                "Protocol": {
                    "Fn::If": [
                        "UseALBSSL",
                        "HTTPS",
                        "HTTP"
                    ]
                },
                "Certificates": [
                    {
                        "Fn::If": [
                            "UseALBSSL",
                            {
                                "CertificateArn": {
                                    "Ref": "ALBSSLCertificateARN"
                                }
                            },
                            {
                                "Ref": "AWS::NoValue"
                            }
                        ]
                    }
                ]
            }
        },
        "ALBTargetGroup": {
            "Type": "AWS::ElasticLoadBalancingV2::TargetGroup",
            "Properties": {
                "HealthCheckIntervalSeconds": 30,
                "HealthCheckTimeoutSeconds": 5,
                "HealthyThresholdCount": 3,
                "Port": 80,
                "Protocol": "HTTP",
                "UnhealthyThresholdCount": 5,
                "VpcId": {
                    "Ref": "VpcId"
                }
            }
        },
        "InstanceSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access and HTTP access on the inbound port",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "80",
                        "ToPort": "80",
                        "SourceSecurityGroupId": {
                            "Fn::Select": [
                                0,
                                {
                                    "Fn::GetAtt": [
                                        "ApplicationLoadBalancer",
                                        "SecurityGroups"
                                    ]
                                }
                            ]
                        }
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "22",
                        "ToPort": "22",
                        "CidrIp": {
                            "Ref": "SSHLocation"
                        }
                    }
                ],
                "VpcId": {
                    "Ref": "VpcId"
                }
            }
        },
        "RecordSet": {
            "Type": "AWS::Route53::RecordSetGroup",
            "Condition": "UseALBSSL",
            "Properties": {
                "HostedZoneName": {
                    "Fn::Join": [
                        "",
                        [
                            {
                                "Ref": "HostedZoneName"
                            },
                            "."
                        ]
                    ]
                },
                "RecordSets": [
                    {
                        "Name": {
                            "Fn::Join": [
                                "",
                                [
                                    {
                                        "Fn::Select": [
                                            "0",
                                            {
                                                "Fn::Split": [
                                                    ".",
                                                    {
                                                        "Fn::GetAtt": [
                                                            "ApplicationLoadBalancer",
                                                            "DNSName"
                                                        ]
                                                    }
                                                ]
                                            }
                                        ]
                                    },
                                    ".",
                                    {
                                        "Ref": "HostedZoneName"
                                    },
                                    "."
                                ]
                            ]
                        },
                        "Type": "A",
                        "AliasTarget": {
                            "DNSName": {
                                "Fn::GetAtt": [
                                    "ApplicationLoadBalancer",
                                    "DNSName"
                                ]
                            },
                            "EvaluateTargetHealth": true,
                            "HostedZoneId": {
                                "Fn::GetAtt": [
                                    "ApplicationLoadBalancer",
                                    "CanonicalHostedZoneID"
                                ]
                            }
                        }
                    }
                ]
            }
        }
    },
    "Outputs": {
        "URL": {
            "Description": "URL of the website",
            "Value": {
                "Fn::Join": [
                    "",
                    [
                        {
                            "Fn::If": [
                                "UseALBSSL",
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "https://",
                                            {
                                                "Fn::Join": [
                                                    "",
                                                    [
                                                        {
                                                            "Fn::Select": [
                                                                "0",
                                                                {
                                                                    "Fn::Split": [
                                                                        ".",
                                                                        {
                                                                            "Fn::GetAtt": [
                                                                                "ApplicationLoadBalancer",
                                                                                "DNSName"
                                                                            ]
                                                                        }
                                                                    ]
                                                                }
                                                            ]
                                                        },
                                                        ".",
                                                        {
                                                            "Ref": "HostedZoneName"
                                                        },
                                                        "."
                                                    ]
                                                ]
                                            }
                                        ]
                                    ]
                                },
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "http://",
                                            {
                                                "Fn::GetAtt": [
                                                    "ApplicationLoadBalancer",
                                                    "DNSName"
                                                ]
                                            }
                                        ]
                                    ]
                                }
                            ]
                        }
                    ]
                ]
            }
        }
    }
}
```

### Example YAML<a name="rules-section-example-syntax.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  AWS CloudFormation Sample Template for using Assertions: Create a load balanced,
  Auto Scaled sample website where the instances are locked down to only accept 
  traffic from the load balancer. This example creates an Auto Scaling group 
  behind a load balancer with a health check. The web site is available on port 
  80 or 443 based on the input.
Parameters:
  VpcId:
    Type: 'AWS::EC2::VPC::Id'
    Description: VpcId of your existing Virtual Private Cloud (VPC)
    ConstraintDescription: must be the VPC Id of an existing Virtual Private Cloud.
  Subnets:
    Type: 'List <AWS::EC2::Subnet::Id>'
    Description: The list of SubnetIds in your Virtual Private Cloud (VPC)
    ConstraintDescription: >-
      must be a list of at least two existing subnets associated with at least
      two different availability zones. They should be residing in the selected
      Virtual Private Cloud.
  InstanceType:
    Description: WebServer EC2 instance type
    Type: String
    Default: t2.small
    AllowedValues:
      - t2.nano
      - t2.micro
      - t2.small
      - t2.medium
      - t2.large
      - m4.large
      - m4.xlarge
      - m4.2xlarge
      - m4.4xlarge
      - m4.10xlarge
      - m3.medium
      - m3.large
      - m3.xlarge
      - m3.2xlarge
      - c4.large
      - c4.xlarge
      - c4.2xlarge
      - c4.4xlarge
      - c4.8xlarge
      - c3.large
      - c3.xlarge
      - c3.2xlarge
      - c3.4xlarge
      - c3.8xlarge
      - r3.large
      - r3.xlarge
    ConstraintDescription: must be a valid EC2 instance type.
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
  UseSSL:
    AllowedValues:
      - 'Yes'
      - 'No'
    ConstraintDescription: Select Yes to create a HTTPS Listener
    Default: 'No'
    Description: 'Select "Yes" to implement SSL, "No" to skip (default).'
    Type: String
  ALBSSLCertificateARN:
    Default: ''
    Description: >-
      [Optional] The ARN of the SSL certificate to be used for the Application
      Load Balancer
    Type: String
  HostedZoneName:
    AllowedPattern: >-
      ^$|(([a-zA-Z0-9]|[a-zA-Z0-9][a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9]|[A-Za-z0-9][A-Za-z0-9\-]*[A-Za-z0-9])$
    Default: ''
    Description: '[Optional] The domain name of a valid Hosted Zone on AWS.'
    Type: String
Conditions:
  UseALBSSL: !Not 
    - !Equals 
      - !Ref UseSSL
      - 'Yes'
Rules:
  SubnetsInVPC:
    Assertions:
      - Assert:
          'Fn::EachMemberIn':
            - 'Fn::ValueOfAll':
                - 'AWS::EC2::Subnet::Id'
                - VpcId
            - 'Fn::RefAll': 'AWS::EC2::VPC::Id'
        AssertDescription: All subnets must in the VPC
  ValidateHostedZone:
    RuleCondition: !Equals 
      - !Ref UseSSL
      - 'Yes'
    Assertions:
      - Assert: !Not 
          - !Equals 
            - !Ref ALBSSLCertificateARN
            - ''
        AssertDescription: ACM Certificate value cannot be empty if SSL is required
      - Assert: !Not 
          - !Equals 
            - !Ref HostedZoneName
            - ''
        AssertDescription: Route53 Hosted Zone Name is mandatory when SSL is required
Mappings:
  AWSAMIRegionMap:
    AMI:
      AMZNLINUXHVM: amzn-ami-hvm-2017.09.1.20171120-x86_64-gp2
    ap-northeast-1:
      AMZNLINUXHVM: ami-da9e2cbc
    ap-northeast-2:
      AMZNLINUXHVM: ami-1196317f
    ap-south-1:
      AMZNLINUXHVM: ami-d5c18eba
    ap-southeast-1:
      AMZNLINUXHVM: ami-c63d6aa5
    ap-southeast-2:
      AMZNLINUXHVM: ami-ff4ea59d
    ca-central-1:
      AMZNLINUXHVM: ami-d29e25b6
    eu-central-1:
      AMZNLINUXHVM: ami-bf2ba8d0
    eu-west-1:
      AMZNLINUXHVM: ami-1a962263
    eu-west-2:
      AMZNLINUXHVM: ami-e7d6c983
    sa-east-1:
      AMZNLINUXHVM: ami-286f2a44
    us-east-1:
      AMZNLINUXHVM: ami-55ef662f
    us-east-2:
      AMZNLINUXHVM: ami-15e9c770
    us-west-1:
      AMZNLINUXHVM: ami-a51f27c5
    us-west-2:
      AMZNLINUXHVM: ami-bf4193c7
Resources:
  WebServerGroup:
    Type: 'AWS::AutoScaling::AutoScalingGroup'
    Properties:
      VPCZoneIdentifier: !Ref Subnets
      LaunchConfigurationName: !Ref LaunchConfig
      MinSize: '2'
      MaxSize: '2'
      TargetGroupARNs:
        - !Ref ALBTargetGroup
    CreationPolicy:
      ResourceSignal:
        Timeout: PT15M
    UpdatePolicy:
      AutoScalingRollingUpdate:
        MinInstancesInService: '1'
        MaxBatchSize: '1'
        PauseTime: PT15M
        WaitOnResourceSignals: 'true'
  LaunchConfig:
    Type: 'AWS::AutoScaling::LaunchConfiguration'
    Metadata:
      Comment: Install a simple application
      'AWS::CloudFormation::Init':
        config:
          packages:
            yum:
              httpd: []
          files:
            /var/www/html/index.html:
              content: !Join 
                - |+

                - - >-
                    <h1>Congratulations, you have successfully launched the AWS
                    CloudFormation sample.<h1>
              mode: '000644'
              owner: root
              group: root
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
                    path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init
                  - 'action=/opt/aws/bin/cfn-init -v '
                  - '         --stack '
                  - !Ref 'AWS::StackName'
                  - '         --resource LaunchConfig '
                  - '         --region '
                  - !Ref 'AWS::Region'
                  - |+

                  - |
                    runas=root
              mode: '000400'
              owner: root
              group: root
          services:
            sysvinit:
              httpd:
                enabled: 'true'
                ensureRunning: 'true'
              cfn-hup:
                enabled: 'true'
                ensureRunning: 'true'
                files:
                  - /etc/cfn/cfn-hup.conf
                  - /etc/cfn/hooks.d/cfn-auto-reloader.conf
    Properties:
      ImageId: !FindInMap 
        - AWSAMIRegionMap
        - !Ref 'AWS::Region'
        - AMZNLINUXHVM
      SecurityGroups:
        - !Ref InstanceSecurityGroup
      InstanceType: !Ref InstanceType
      KeyName: !Ref KeyName
      UserData: !Base64 
        'Fn::Join':
          - ''
          - - |
              #!/bin/bash -xe
            - |
              yum update -y aws-cfn-bootstrap
            - '/opt/aws/bin/cfn-init -v '
            - '         --stack '
            - !Ref 'AWS::StackName'
            - '         --resource LaunchConfig '
            - '         --region '
            - !Ref 'AWS::Region'
            - |+

            - '/opt/aws/bin/cfn-signal -e $? '
            - '         --stack '
            - !Ref 'AWS::StackName'
            - '         --resource WebServerGroup '
            - '         --region '
            - !Ref 'AWS::Region'
            - |+

  ELBSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Allow access to the ELB
      VpcId: !Ref VpcId
      SecurityGroupIngress:
        - !If 
          - UseALBSSL
          - IpProtocol: tcp
            FromPort: '443'
            ToPort: '443'
            CidrIp: 0.0.0.0/0
          - IpProtocol: tcp
            FromPort: '80'
            ToPort: '80'
            CidrIp: 0.0.0.0/0
  ApplicationLoadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Subnets: !Ref Subnets
      SecurityGroups:
        - !Ref ELBSecurityGroup
  ALBListener:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref ALBTargetGroup
      LoadBalancerArn: !Ref ApplicationLoadBalancer
      Port: !If 
        - UseALBSSL
        - 443
        - 80
      Protocol: !If 
        - UseALBSSL
        - HTTPS
        - HTTP
      Certificates:
        - !If 
          - UseALBSSL
          - CertificateArn: !Ref ALBSSLCertificateARN
          - !Ref 'AWS::NoValue'
  ALBTargetGroup:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      HealthCheckIntervalSeconds: 30
      HealthCheckTimeoutSeconds: 5
      HealthyThresholdCount: 3
      Port: 80
      Protocol: HTTP
      UnhealthyThresholdCount: 5
      VpcId: !Ref VpcId
  InstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access and HTTP access on the inbound port
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '80'
          ToPort: '80'
          SourceSecurityGroupId: !Select 
            - 0
            - !GetAtt 
              - ApplicationLoadBalancer
              - SecurityGroups
        - IpProtocol: tcp
          FromPort: '22'
          ToPort: '22'
          CidrIp: !Ref SSHLocation
      VpcId: !Ref VpcId
  RecordSet:
    Type: 'AWS::Route53::RecordSetGroup'
    Condition: UseALBSSL
    Properties:
      HostedZoneName: !Join 
        - ''
        - - !Ref HostedZoneName
          - .
      RecordSets:
        - Name: !Join 
            - ''
            - - !Select 
                - '0'
                - !Split 
                  - .
                  - !GetAtt 
                    - ApplicationLoadBalancer
                    - DNSName
              - .
              - !Ref HostedZoneName
              - .
          Type: A
          AliasTarget:
            DNSName: !GetAtt 
              - ApplicationLoadBalancer
              - DNSName
            EvaluateTargetHealth: true
            HostedZoneId: !GetAtt 
              - ApplicationLoadBalancer
              - CanonicalHostedZoneID
Outputs:
  URL:
    Description: URL of the website
    Value: !Join 
      - ''
      - - !If 
          - UseALBSSL
          - !Join 
            - ''
            - - 'https://'
              - !Join 
                - ''
                - - !Select 
                    - '0'
                    - !Split 
                      - .
                      - !GetAtt 
                        - ApplicationLoadBalancer
                        - DNSName
                  - .
                  - !Ref HostedZoneName
                  - .
          - !Join 
            - ''
            - - 'http://'
              - !GetAtt 
                - ApplicationLoadBalancer
                - DNSName
```