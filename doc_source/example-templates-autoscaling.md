# Walkthrough: Create a scalable, load\-balancing web server<a name="example-templates-autoscaling"></a>

This template creates a sample web site that uses Amazon EC2 Auto Scaling and Elastic Load Balancing and is configured to use multiple Availability Zones\. The template also contains CloudWatch alarms that execute scaling policies to add or remove instances from the Auto Scaling group when the defined thresholds are exceeded\.

This template creates one or more Amazon EC2 instances\. You will be billed for the AWS resources used if you create a stack from this template\.

**Note**  
The template assumes that your account supports the EC2\-VPC platform\. In other words, you have a default VPC that allows instances to access the Internet\. If you don't have a default VPC, you can create one\. For more information, see [Amazon EC2 and Amazon Virtual Private Cloud](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-vpc.html) in the *Amazon EC2 User Guide for Linux Instances*\.

You can get the latest version of this sample template at [https://s3\.amazonaws\.com/cloudformation\-templates\-us\-east\-1/AutoScalingMultiAZWithNotifications\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/AutoScalingMultiAZWithNotifications.template)\.

## Auto scaling multi\-AZ template<a name="example-templates-autoscaling-template"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "AWS CloudFormation Sample Template AutoScalingMultiAZWithNotifications: Create a multi-az, load balanced and auto-scaled sample web site running on an Apache Web Server. The application is configured to span all Availability Zones in the region and is auto-scaled based on the CPU utilization of the web servers. Notifications will be sent to the operator email address on scaling events. The instances are load balanced with a simple health check against the default web page. **WARNING** This template creates one or more Amazon EC2 instances and an Elastic Load Balancer. You will be billed for the AWS resources used if you create a stack from this template.",

  "Parameters" : {
    "InstanceType" : {
      "Description" : "WebServer EC2 instance type",
      "Type" : "String",
      "Default" : "t2.small",
      "AllowedValues" : [ 
        "t1.micro", 
        "t2.nano", 
        "t2.micro", 
        "t2.small", 
        "t2.medium", 
        "t2.large", 
        "m1.small", 
        "m1.medium", 
        "m1.large", 
        "m1.xlarge", 
        "m2.xlarge", 
        "m2.2xlarge", 
        "m2.4xlarge", 
        "m3.medium", 
        "m3.large", 
        "m3.xlarge", 
        "m3.2xlarge", 
        "m4.large", 
        "m4.xlarge", 
        "m4.2xlarge", 
        "m4.4xlarge", 
        "m4.10xlarge", 
        "c1.medium", 
        "c1.xlarge", 
        "c3.large", 
        "c3.xlarge", 
        "c3.2xlarge", 
        "c3.4xlarge", 
        "c3.8xlarge", 
        "c4.large", 
        "c4.xlarge", 
        "c4.2xlarge", 
        "c4.4xlarge", 
        "c4.8xlarge", 
        "g2.2xlarge", 
        "g2.8xlarge", 
        "r3.large", 
        "r3.xlarge", 
        "r3.2xlarge", 
        "r3.4xlarge", 
        "r3.8xlarge", 
        "i2.xlarge", 
        "i2.2xlarge", 
        "i2.4xlarge", 
        "i2.8xlarge", 
        "d2.xlarge", 
        "d2.2xlarge", 
        "d2.4xlarge", 
        "d2.8xlarge", 
        "hi1.4xlarge", 
        "hs1.8xlarge", 
        "cr1.8xlarge", 
        "cc2.8xlarge", 
        "cg1.4xlarge"
      ],
      "ConstraintDescription" : "must be a valid EC2 instance type."
    },

    "OperatorEMail": {
      "Description": "EMail address to notify if there are any scaling operations",
      "Type": "String",
      "AllowedPattern": "([a-zA-Z0-9_\\-\\.]+)@((\\[[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}\\.)|(([a-zA-Z0-9\\-]+\\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\\]?)",
      "ConstraintDescription": "must be a valid email address."
    },

    "KeyName" : {
      "Description" : "The EC2 Key Pair to allow SSH access to the instances",
      "Type" : "AWS::EC2::KeyPair::KeyName",
      "ConstraintDescription" : "must be the name of an existing EC2 KeyPair."
    },

    "SSHLocation" : {
      "Description" : "The IP address range that can be used to SSH to the EC2 instances",
      "Type": "String",
      "MinLength": "9",
      "MaxLength": "18",
      "Default": "0.0.0.0/0",
      "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
      "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
    }
  },

  "Mappings" : {
    "AWSInstanceType2Arch" : {
      "t1.micro"    : { "Arch" : "HVM64"  },
      "t2.nano"     : { "Arch" : "HVM64"  },
      "t2.micro"    : { "Arch" : "HVM64"  },
      "t2.small"    : { "Arch" : "HVM64"  },
      "t2.medium"   : { "Arch" : "HVM64"  },
      "t2.large"    : { "Arch" : "HVM64"  },
      "m1.small"    : { "Arch" : "HVM64"  },
      "m1.medium"   : { "Arch" : "HVM64"  },
      "m1.large"    : { "Arch" : "HVM64"  },
      "m1.xlarge"   : { "Arch" : "HVM64"  },
      "m2.xlarge"   : { "Arch" : "HVM64"  },
      "m2.2xlarge"  : { "Arch" : "HVM64"  },
      "m2.4xlarge"  : { "Arch" : "HVM64"  },
      "m3.medium"   : { "Arch" : "HVM64"  },
      "m3.large"    : { "Arch" : "HVM64"  },
      "m3.xlarge"   : { "Arch" : "HVM64"  },
      "m3.2xlarge"  : { "Arch" : "HVM64"  },
      "m4.large"    : { "Arch" : "HVM64"  },
      "m4.xlarge"   : { "Arch" : "HVM64"  },
      "m4.2xlarge"  : { "Arch" : "HVM64"  },
      "m4.4xlarge"  : { "Arch" : "HVM64"  },
      "m4.10xlarge" : { "Arch" : "HVM64"  },
      "c1.medium"   : { "Arch" : "HVM64"  },
      "c1.xlarge"   : { "Arch" : "HVM64"  },
      "c3.large"    : { "Arch" : "HVM64"  },
      "c3.xlarge"   : { "Arch" : "HVM64"  },
      "c3.2xlarge"  : { "Arch" : "HVM64"  },
      "c3.4xlarge"  : { "Arch" : "HVM64"  },
      "c3.8xlarge"  : { "Arch" : "HVM64"  },
      "c4.large"    : { "Arch" : "HVM64"  },
      "c4.xlarge"   : { "Arch" : "HVM64"  },
      "c4.2xlarge"  : { "Arch" : "HVM64"  },
      "c4.4xlarge"  : { "Arch" : "HVM64"  },
      "c4.8xlarge"  : { "Arch" : "HVM64"  },
      "g2.2xlarge"  : { "Arch" : "HVMG2"  },
      "g2.8xlarge"  : { "Arch" : "HVMG2"  },
      "r3.large"    : { "Arch" : "HVM64"  },
      "r3.xlarge"   : { "Arch" : "HVM64"  },
      "r3.2xlarge"  : { "Arch" : "HVM64"  },
      "r3.4xlarge"  : { "Arch" : "HVM64"  },
      "r3.8xlarge"  : { "Arch" : "HVM64"  },
      "i2.xlarge"   : { "Arch" : "HVM64"  },
      "i2.2xlarge"  : { "Arch" : "HVM64"  },
      "i2.4xlarge"  : { "Arch" : "HVM64"  },
      "i2.8xlarge"  : { "Arch" : "HVM64"  },
      "d2.xlarge"   : { "Arch" : "HVM64"  },
      "d2.2xlarge"  : { "Arch" : "HVM64"  },
      "d2.4xlarge"  : { "Arch" : "HVM64"  },
      "d2.8xlarge"  : { "Arch" : "HVM64"  },
      "hi1.4xlarge" : { "Arch" : "HVM64"  },
      "hs1.8xlarge" : { "Arch" : "HVM64"  },
      "cr1.8xlarge" : { "Arch" : "HVM64"  },
      "cc2.8xlarge" : { "Arch" : "HVM64"  }
    },

    "AWSInstanceType2NATArch" : {
      "t1.micro"    : { "Arch" : "NATHVM64"  },
      "t2.nano"     : { "Arch" : "NATHVM64"  },
      "t2.micro"    : { "Arch" : "NATHVM64"  },
      "t2.small"    : { "Arch" : "NATHVM64"  },
      "t2.medium"   : { "Arch" : "NATHVM64"  },
      "t2.large"    : { "Arch" : "NATHVM64"  },
      "m1.small"    : { "Arch" : "NATHVM64"  },
      "m1.medium"   : { "Arch" : "NATHVM64"  },
      "m1.large"    : { "Arch" : "NATHVM64"  },
      "m1.xlarge"   : { "Arch" : "NATHVM64"  },
      "m2.xlarge"   : { "Arch" : "NATHVM64"  },
      "m2.2xlarge"  : { "Arch" : "NATHVM64"  },
      "m2.4xlarge"  : { "Arch" : "NATHVM64"  },
      "m3.medium"   : { "Arch" : "NATHVM64"  },
      "m3.large"    : { "Arch" : "NATHVM64"  },
      "m3.xlarge"   : { "Arch" : "NATHVM64"  },
      "m3.2xlarge"  : { "Arch" : "NATHVM64"  },
      "m4.large"    : { "Arch" : "NATHVM64"  },
      "m4.xlarge"   : { "Arch" : "NATHVM64"  },
      "m4.2xlarge"  : { "Arch" : "NATHVM64"  },
      "m4.4xlarge"  : { "Arch" : "NATHVM64"  },
      "m4.10xlarge" : { "Arch" : "NATHVM64"  },
      "c1.medium"   : { "Arch" : "NATHVM64"  },
      "c1.xlarge"   : { "Arch" : "NATHVM64"  },
      "c3.large"    : { "Arch" : "NATHVM64"  },
      "c3.xlarge"   : { "Arch" : "NATHVM64"  },
      "c3.2xlarge"  : { "Arch" : "NATHVM64"  },
      "c3.4xlarge"  : { "Arch" : "NATHVM64"  },
      "c3.8xlarge"  : { "Arch" : "NATHVM64"  },
      "c4.large"    : { "Arch" : "NATHVM64"  },
      "c4.xlarge"   : { "Arch" : "NATHVM64"  },
      "c4.2xlarge"  : { "Arch" : "NATHVM64"  },
      "c4.4xlarge"  : { "Arch" : "NATHVM64"  },
      "c4.8xlarge"  : { "Arch" : "NATHVM64"  },
      "g2.2xlarge"  : { "Arch" : "NATHVMG2"  },
      "g2.8xlarge"  : { "Arch" : "NATHVMG2"  },
      "r3.large"    : { "Arch" : "NATHVM64"  },
      "r3.xlarge"   : { "Arch" : "NATHVM64"  },
      "r3.2xlarge"  : { "Arch" : "NATHVM64"  },
      "r3.4xlarge"  : { "Arch" : "NATHVM64"  },
      "r3.8xlarge"  : { "Arch" : "NATHVM64"  },
      "i2.xlarge"   : { "Arch" : "NATHVM64"  },
      "i2.2xlarge"  : { "Arch" : "NATHVM64"  },
      "i2.4xlarge"  : { "Arch" : "NATHVM64"  },
      "i2.8xlarge"  : { "Arch" : "NATHVM64"  },
      "d2.xlarge"   : { "Arch" : "NATHVM64"  },
      "d2.2xlarge"  : { "Arch" : "NATHVM64"  },
      "d2.4xlarge"  : { "Arch" : "NATHVM64"  },
      "d2.8xlarge"  : { "Arch" : "NATHVM64"  },
      "hi1.4xlarge" : { "Arch" : "NATHVM64"  },
      "hs1.8xlarge" : { "Arch" : "NATHVM64"  },
      "cr1.8xlarge" : { "Arch" : "NATHVM64"  },
      "cc2.8xlarge" : { "Arch" : "NATHVM64"  }
    }
,
    "AWSRegionArch2AMI" : {
      "us-east-1"        : {"HVM64" : "ami-0ff8a91507f77f867", "HVMG2" : "ami-0a584ac55a7631c0c"},
      "us-west-2"        : {"HVM64" : "ami-a0cfeed8", "HVMG2" : "ami-0e09505bc235aa82d"},
      "us-west-1"        : {"HVM64" : "ami-0bdb828fd58c52235", "HVMG2" : "ami-066ee5fd4a9ef77f1"},
      "eu-west-1"        : {"HVM64" : "ami-047bb4163c506cd98", "HVMG2" : "ami-0a7c483d527806435"},
      "eu-west-2"        : {"HVM64" : "ami-f976839e", "HVMG2" : "NOT_SUPPORTED"},
      "eu-west-3"        : {"HVM64" : "ami-0ebc281c20e89ba4b", "HVMG2" : "NOT_SUPPORTED"},
      "eu-central-1"     : {"HVM64" : "ami-0233214e13e500f77", "HVMG2" : "ami-06223d46a6d0661c7"},
      "ap-northeast-1"   : {"HVM64" : "ami-06cd52961ce9f0d85", "HVMG2" : "ami-053cdd503598e4a9d"},
      "ap-northeast-2"   : {"HVM64" : "ami-0a10b2721688ce9d2", "HVMG2" : "NOT_SUPPORTED"},
      "ap-northeast-3"   : {"HVM64" : "ami-0d98120a9fb693f07", "HVMG2" : "NOT_SUPPORTED"},
      "ap-southeast-1"   : {"HVM64" : "ami-08569b978cc4dfa10", "HVMG2" : "ami-0be9df32ae9f92309"},
      "ap-southeast-2"   : {"HVM64" : "ami-09b42976632b27e9b", "HVMG2" : "ami-0a9ce9fecc3d1daf8"},
      "ap-south-1"       : {"HVM64" : "ami-0912f71e06545ad88", "HVMG2" : "ami-097b15e89dbdcfcf4"},
      "us-east-2"        : {"HVM64" : "ami-0b59bfac6be064b78", "HVMG2" : "NOT_SUPPORTED"},
      "ca-central-1"     : {"HVM64" : "ami-0b18956f", "HVMG2" : "NOT_SUPPORTED"},
      "sa-east-1"        : {"HVM64" : "ami-07b14488da8ea02a0", "HVMG2" : "NOT_SUPPORTED"},
      "cn-north-1"       : {"HVM64" : "ami-0a4eaf6c4454eda75", "HVMG2" : "NOT_SUPPORTED"},
      "cn-northwest-1"   : {"HVM64" : "ami-6b6a7d09", "HVMG2" : "NOT_SUPPORTED"}
    }

  },
 
  "Resources" : {
    "NotificationTopic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {
        "Subscription": [ { "Endpoint": { "Ref": "OperatorEMail" }, "Protocol": "email" } ]
      }
    },

    "WebServerGroup" : {
      "Type" : "AWS::AutoScaling::AutoScalingGroup",
      "Properties" : {
        "AvailabilityZones" : { "Fn::GetAZs" : ""},
        "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
        "MinSize" : "1",
        "MaxSize" : "3",
        "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ],
        "NotificationConfiguration" : {
          "TopicARN" : { "Ref" : "NotificationTopic" },
          "NotificationTypes" : [ "autoscaling:EC2_INSTANCE_LAUNCH",
                                  "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
                                  "autoscaling:EC2_INSTANCE_TERMINATE",
                                  "autoscaling:EC2_INSTANCE_TERMINATE_ERROR"]
        }
      },
      "CreationPolicy" : {
        "ResourceSignal" : {
          "Timeout" : "PT15M",
          "Count"   : "1"
        }
      },
      "UpdatePolicy": {
        "AutoScalingRollingUpdate": {
          "MinInstancesInService": "1",
          "MaxBatchSize": "1",
          "PauseTime" : "PT15M",
          "WaitOnResourceSignals": "true"
        }
      }
    },

    "LaunchConfig" : {
      "Type" : "AWS::AutoScaling::LaunchConfiguration",
      "Metadata" : {
        "Comment" : "Install a simple application",
        "AWS::CloudFormation::Init" : {
          "config" : {
            "packages" : {
              "yum" : {
                "httpd" : []
              }
            },

            "files" : {
              "/var/www/html/index.html" : {
                "content" : { "Fn::Join" : ["\n", [
                  "<img src=\"", {"Fn::FindInMap" : ["Region2Examples", {"Ref" : "AWS::Region"}, "Examples"]}, "/cloudformation_graphic.png\" alt=\"AWS CloudFormation Logo\"/>",
                  "<h1>Congratulations, you have successfully launched the AWS CloudFormation sample.</h1>"
                ]]},
                "mode"    : "000644",
                "owner"   : "root",
                "group"   : "root"
              },

              "/etc/cfn/cfn-hup.conf" : {
                "content" : { "Fn::Join" : ["", [
                  "[main]\n",
                  "stack=", { "Ref" : "AWS::StackId" }, "\n",
                  "region=", { "Ref" : "AWS::Region" }, "\n"
                ]]},
                "mode"    : "000400",
                "owner"   : "root",
                "group"   : "root"
              },

              "/etc/cfn/hooks.d/cfn-auto-reloader.conf" : {
                "content": { "Fn::Join" : ["", [
                  "[cfn-auto-reloader-hook]\n",
                  "triggers=post.update\n",
                  "path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init\n",
                  "action=/opt/aws/bin/cfn-init -v ",
                  "         --stack ", { "Ref" : "AWS::StackName" },
                  "         --resource LaunchConfig ",
                  "         --region ", { "Ref" : "AWS::Region" }, "\n",
                  "runas=root\n"
                ]]}
              }
            },

            "services" : {
              "sysvinit" : {
                "httpd"    : { "enabled" : "true", "ensureRunning" : "true" },
                "cfn-hup" : { "enabled" : "true", "ensureRunning" : "true",
                              "files" : ["/etc/cfn/cfn-hup.conf", "/etc/cfn/hooks.d/cfn-auto-reloader.conf"]}
              }
            }
          }
        }
      },
      "Properties" : {
        "KeyName" : { "Ref" : "KeyName" },
        "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" },
                                          { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
        "SecurityGroups" : [ { "Ref" : "InstanceSecurityGroup" } ],
        "InstanceType" : { "Ref" : "InstanceType" },
        "UserData"       : { "Fn::Base64" : { "Fn::Join" : ["", [
             "#!/bin/bash -xe\n",
             "yum update -y aws-cfn-bootstrap\n",

             "/opt/aws/bin/cfn-init -v ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource LaunchConfig ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n",

             "/opt/aws/bin/cfn-signal -e $? ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource WebServerGroup ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n"
        ]]}}
      }
    },

    "WebServerScaleUpPolicy" : {
      "Type" : "AWS::AutoScaling::ScalingPolicy",
      "Properties" : {
        "AdjustmentType" : "ChangeInCapacity",
        "AutoScalingGroupName" : { "Ref" : "WebServerGroup" },
        "Cooldown" : "60",
        "ScalingAdjustment" : "1"
      }
    },
    "WebServerScaleDownPolicy" : {
      "Type" : "AWS::AutoScaling::ScalingPolicy",
      "Properties" : {
        "AdjustmentType" : "ChangeInCapacity",
        "AutoScalingGroupName" : { "Ref" : "WebServerGroup" },
        "Cooldown" : "60",
        "ScalingAdjustment" : "-1"
      }
    },

    "CPUAlarmHigh": {
     "Type": "AWS::CloudWatch::Alarm",
     "Properties": {
        "AlarmDescription": "Scale-up if CPU > 90% for 10 minutes",
        "MetricName": "CPUUtilization",
        "Namespace": "AWS/EC2",
        "Statistic": "Average",
        "Period": "300",
        "EvaluationPeriods": "2",
        "Threshold": "90",
        "AlarmActions": [ { "Ref": "WebServerScaleUpPolicy" } ],
        "Dimensions": [
          {
            "Name": "AutoScalingGroupName",
            "Value": { "Ref": "WebServerGroup" }
          }
        ],
        "ComparisonOperator": "GreaterThanThreshold"
      }
    },
    "CPUAlarmLow": {
     "Type": "AWS::CloudWatch::Alarm",
     "Properties": {
        "AlarmDescription": "Scale-down if CPU < 70% for 10 minutes",
        "MetricName": "CPUUtilization",
        "Namespace": "AWS/EC2",
        "Statistic": "Average",
        "Period": "300",
        "EvaluationPeriods": "2",
        "Threshold": "70",
        "AlarmActions": [ { "Ref": "WebServerScaleDownPolicy" } ],
        "Dimensions": [
          {
            "Name": "AutoScalingGroupName",
            "Value": { "Ref": "WebServerGroup" }
          }
        ],
        "ComparisonOperator": "LessThanThreshold"
      }
    },

    "ElasticLoadBalancer" : {
      "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties" : {
        "AvailabilityZones" : { "Fn::GetAZs" : "" },
        "CrossZone" : "true",
        "Listeners" : [ {
          "LoadBalancerPort" : "80",
          "InstancePort" : "80",
          "Protocol" : "HTTP"
        } ],
        "HealthCheck" : {
          "Target" : "HTTP:80/",
          "HealthyThreshold" : "3",
          "UnhealthyThreshold" : "5",
          "Interval" : "30",
          "Timeout" : "5"
        }
      }
    },

    "InstanceSecurityGroup" : {
      "Type" : "AWS::EC2::SecurityGroup",
      "Properties" : {
        "GroupDescription" : "Enable SSH access and HTTP from the load balancer only",
        "SecurityGroupIngress" : [ {
          "IpProtocol" : "tcp",
          "FromPort" : "22",
          "ToPort" : "22",
          "CidrIp" : { "Ref" : "SSHLocation"}
        },
        {
          "IpProtocol" : "tcp",
          "FromPort" : "80",
          "ToPort" : "80",
          "SourceSecurityGroupOwnerId" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.OwnerAlias"]},
          "SourceSecurityGroupName" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.GroupName"]}
        } ]
      }
    }
  },

  "Outputs" : {
    "URL" : {
      "Description" : "The URL of the website",
      "Value" :  { "Fn::Join" : [ "", [ "http://", { "Fn::GetAtt" : [ "ElasticLoadBalancer", "DNSName" ]}]]}
    }
  }
}
```

## Template walkthrough<a name="example-templates-autoscaling-description"></a>

The example template contains an Auto Scaling group with a LoadBalancer, a security group that defines ingress rules, CloudWatch alarms, and scaling policies\.

The template has three input parameters: InstanceType is the type of EC2 instance to use for the Auto Scaling group and has a default of m1\.small; WebServerPort is the TCP port for the web server and has a default of 8888; KeyName is the name of an EC2 key pair to be used for the Auto Scaling group\. KeyName must be specified at stack creation \(parameters with no default value must be specified at stack creation\)\.

The [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource WebServerGroup declares the following Auto Scaling group configuration:
+ *AvailabilityZones* specifies the Availability Zones where the Auto Scaling group's EC2 instances will be created\. The [Fn::GetAZs](intrinsic-function-reference-getavailabilityzones.md) function call `{ "Fn::GetAZs" : "" }` specifies all Availability Zones for the region in which the stack is created\.
+ *MinSize* and *MaxSize* set the minimum and maximum number of EC2 instances in the Auto Scaling group\.
+ *LoadBalancerNames* lists the LoadBalancers used to route traffic to the Auto Scaling group\. The LoadBalancer for this group is the ElasticLoadBalancer resource\.

The [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource LaunchConfig declares the following configurations to use for the EC2 instances in the WebServerGroup Auto Scaling group:
+ *KeyName* takes the value of the KeyName input parameter as the EC2 key pair to use\.
+ *UserData* is the Base64 encoded value of the WebServerPort parameter, which is passed to an application \.
+ *SecurityGroups* is a list of EC2 security groups that contain the firewall ingress rules for EC2 instances in the Auto Scaling group\. In this example, there is only one security group and it is declared as a [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource: InstanceSecurityGroup\. This security group contains two ingress rules: 1\) a TCP ingress rule that allows access from all IP addresses \("CidrIp" : "0\.0\.0\.0/0"\) for port 22 \(for SSH access\) and 2\) a TCP ingress rule that allows access from the ElasticLoadBalancer resource for the WebServerPort port by specifying the LoadBalancer's source security group\. The [GetAtt](intrinsic-function-reference-getatt.md) function is used to get the SourceSecurityGroup\.OwnerAlias and SourceSecurityGroup\.GroupName properties from the ElasticLoadBalancer resource\. For more information about the Elastic Load Balancing security groups, see [Manage security groups in Amazon EC2\-Classic](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/using-elb-security-groups.html) or [Manage security groups in Amazon VPC](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/USVPC_ApplySG.html)\.
+ *ImageId* is the evaluated value of a set of nested maps\. We added the maps so that the template contained the logic for choosing the right image ID\. That logic is based on the instance type that was specified with the InstanceType parameter \(AWSInstanceType2Arch maps the instance type to an architecture 32 or 64\) and the region where the stack is created \(AWSRegionArch2AMI maps the region and architecture to a image ID\):

  ```
  { "Fn::FindInMap" : [ "AWSRegionArch2AMI",
     { "Ref" : "AWS::Region" },
     { "Fn::FindInMap" : [ "AWSInstanceType2Arch",
        { "Ref" : "InstanceType" },
        "Arch" ]
     }
     ]}
  ```

  For example, if you use this template to create a stack in the `us-east-2` region and specify m1\.small as InstanceType, AWS CloudFormation would evaluate the inner map for AWSInstanceType2Arch as the following:

  ```
  { "Fn::FindInMap" : [ "AWSInstanceType2Arch", "m1.small", "Arch" ] }
  ```

  In the AWSInstanceType2Arch mapping, the Arch value for the m1\.small key maps to 32, which is used as the value for the outer map\. The key is the evaluated result of the AWS::Region pseudo parameter which is the region where the stack is being created\. For this example, AWS::Region is us\-east\-1; therefore, the outer map is evaluated as follows:

  ```
  Fn::FindInMap" : [ "AWSRegionArch2AMI", "us-east-1", "32"]
  ```

  In the AWSRegionArch2AMI mapping, the value 32 for the key us\-east\-1 maps to ami\-6411e20d\. This means that ImageId would be ami\-6411e20d\.

The [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html) resource ElasticLoadBalancer declares the following LoadBalancer configuration:
+ *AvailabilityZones* is a list of Availability Zones where the LoadBalancer will distribute traffic\. In this example, the Fn::GetAZs function call `{ "Fn::GetAZs" : "" }` specifies all Availability Zones for the region in which the stack is created\.
+ *Listeners* is a list of load balancing routing configurations that specify the port that the LoadBalancer accepts requests, the port on the registered EC2 instances where the LoadBalancer forwards requests, and the protocol used to route requests\.
+ *HealthCheck* is the configuration that Elastic Load Balancing uses to check the health of the EC2 instances that the LoadBalancer routes traffic to\. In this example, the HealthCheck targets the root address of the EC2 instances using the port specified by WebServerPort over the HTTP protocol\. If the WebServerPort is 8888, the `{ "Fn::Join" : [ "", ["HTTP:", { "Ref" : "WebServerPort" }, "/"]]}` function call is evaluated as the string `HTTP:8888/`\. It also specifies that the EC2 instances have an interval of 30 seconds between health checks \(Interval\)\. The Timeout is defined as the length of time Elastic Load Balancing waits for a response from the health check target \(5 seconds in this example\)\. After the Timeout period lapses, Elastic Load Balancing marks that EC2 instance's health check as unhealthy\. When an EC2 instance fails 5 consecutive health checks \(UnhealthyThreshold\), Elastic Load Balancing stops routing traffic to that EC2 instance until that instance has 3 consecutive healthy health checks at which point Elastic Load Balancing considers the EC2 instance healthy and begins routing traffic to that instance again\.

The [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) resource WebServerScaleUpPolicy is a simple scaling policy that scales up the Auto Scaling group WebServerGroup\. The `AdjustmentType` property is set to ChangeInCapacity\. This means that the `ScalingAdjustment` represents the number of instances to add \(if `ScalingAdjustment` is positive, instances are added; if negative, instances are deleted\)\. In this example, `ScalingAdjustment` is 1; therefore, the scaling policy increments the number of EC2 instances in the group by 1 when the policy is executed\. The Cooldown property specifies that Amazon EC2 Auto Scaling waits 60 seconds before starting any other scaling activities due to simple scaling policies\.

The [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html) resource CPUAlarmHigh specifies the simple scaling policy WebServerScaleUpPolicy as the action to execute when the alarm is in an `ALARM` state \(AlarmActions\)\. The alarm monitors the EC2 instances in the WebServerGroup Auto Scaling group \(Dimensions\)\. The alarm measures the average \(Statistic\) EC2 instance CPU utilization \(Namespace and MetricName\) of the instances in the WebServerGroup \(Dimensions\) over a 300 second interval \(Period\)\. When this value \(average CPU utilization over 300 seconds\) remains greater than 90 percent \(ComparisonOperator and Threshold\) for 2 consecutive periods \(EvaluationPeriod\), the alarm will go into an `ALARM` state and CloudWatch will execute the WebServerScaleUpPolicy policy \(AlarmActions\) described above scale up the WebServerGroup\.

The CPUAlarmLow alarm measures the same metrics but has an alarm that triggers when CPU utilization is less than 75 percent \(ComparisonOperator and Threshold\) and executes the WebServerScaleDownPolicy policy to remove 1 EC2 instance from the Auto Scaling group WebServerGroup\.