# Walkthrough: Create a scaled and load\-balanced application<a name="example-templates-autoscaling"></a>

For this walkthrough, you create a stack that helps you set up a scaled and load\-balanced application\. The walkthrough provides a sample template that you use to create the stack\. The example template provisions an Auto Scaling group, an Application Load Balancer, security groups that control traffic to the load balancer and to the Auto Scaling group, and an Amazon SNS notification configuration to publish notifications about scaling activities\. 

This template creates one or more Amazon EC2 instances and an Application Load Balancer\. You will be billed for the AWS resources used if you create a stack from this template\. 

## Full stack template<a name="example-templates-autoscaling-full-stack-template"></a>

Let's start with the template\.

**YAML**

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  InstanceType:
    Description: The EC2 instance type
    Type: String
    Default: t3.micro
    AllowedValues:
      - t3.micro
      - t3.small
      - t3.medium
  KeyName:
    Description: Name of an existing EC2 key pair to allow SSH access to the instances
    Type: 'AWS::EC2::KeyPair::KeyName'
  LatestAmiId:
    Description: The latest Amazon Linux 2 AMI from the Parameter Store
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2'
  OperatorEmail:
    Description: The email address to notify when there are any scaling activities
    Type: String
  SSHLocation:
    Description: The IP address range that can be used to SSH to the EC2 instances
    Type: String
    MinLength: 9
    MaxLength: 18
    Default: 0.0.0.0/0
    ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
  Subnets:
    Type: 'List<AWS::EC2::Subnet::Id>'
    Description: At least two public subnets in different Availability Zones in the selected VPC
  VPC:
    Type: 'AWS::EC2::VPC::Id'
    Description: A virtual private cloud (VPC) that enables resources in public subnets to connect to the internet
Resources:
  ELBSecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: ELB Security Group
      VpcId: !Ref VPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: 80
        ToPort: 80
        CidrIp: 0.0.0.0/0
  EC2SecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: EC2 Security Group
      VpcId: !Ref VPC
      SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: 80
        ToPort: 80
        SourceSecurityGroupId:
          Fn::GetAtt:
          - ELBSecurityGroup
          - GroupId
      - IpProtocol: tcp
        FromPort: 22
        ToPort: 22
        CidrIp: !Ref SSHLocation
  EC2TargetGroup:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      HealthCheckIntervalSeconds: 30
      HealthCheckProtocol: HTTP
      HealthCheckTimeoutSeconds: 15
      HealthyThresholdCount: 5
      Matcher:
        HttpCode: '200'
      Name: EC2TargetGroup
      Port: 80
      Protocol: HTTP
      TargetGroupAttributes:
      - Key: deregistration_delay.timeout_seconds
        Value: '20'
      UnhealthyThresholdCount: 3
      VpcId: !Ref VPC
  ALBListener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref EC2TargetGroup
      LoadBalancerArn: !Ref ApplicationLoadBalancer
      Port: 80
      Protocol: HTTP
  ApplicationLoadBalancer:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Scheme: internet-facing
      Subnets: !Ref Subnets
      SecurityGroups:
        - !GetAtt ELBSecurityGroup.GroupId
  LaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
      LaunchTemplateData:
        ImageId: !Ref LatestAmiId
        InstanceType: !Ref InstanceType
        KeyName: !Ref KeyName
        SecurityGroupIds: 
          - !Ref EC2SecurityGroup
        UserData:
          Fn::Base64: !Sub |
            #!/bin/bash
            yum update -y
            yum install -y httpd
            systemctl start httpd
            systemctl enable httpd
            echo "<h1>Hello World!</h1>" > /var/www/html/index.html
  NotificationTopic:
    Type: AWS::SNS::Topic
    Properties:
      Subscription:
        - Endpoint: !Ref OperatorEmail
          Protocol: email
  WebServerGroup:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      LaunchTemplate:
        LaunchTemplateId: !Ref LaunchTemplate
        Version: !GetAtt LaunchTemplate.LatestVersionNumber
      MaxSize: '3'
      MinSize: '1'
      NotificationConfigurations:
        - TopicARN: !Ref NotificationTopic
          NotificationTypes: ['autoscaling:EC2_INSTANCE_LAUNCH', 'autoscaling:EC2_INSTANCE_LAUNCH_ERROR', 'autoscaling:EC2_INSTANCE_TERMINATE', 'autoscaling:EC2_INSTANCE_TERMINATE_ERROR']
      TargetGroupARNs:
        - !Ref EC2TargetGroup
      VPCZoneIdentifier: !Ref Subnets
```

**JSON**

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "InstanceType":{
      "Description":"The EC2 instance type",
      "Type":"String",
      "Default":"t3.micro",
      "AllowedValues":[
        "t3.micro",
        "t3.small",
        "t3.medium"
      ]
    },
    "KeyName":{
      "Description":"Name of an existing EC2 key pair to allow SSH access to the instances",
      "Type":"AWS::EC2::KeyPair::KeyName"
    },
    "LatestAmiId":{
      "Description":"The latest Amazon Linux 2 AMI from the Parameter Store",
      "Type":"AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
      "Default":"/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2"
    },
    "OperatorEmail":{
      "Description":"The email address to notify when there are any scaling activities",
      "Type":"String"
    },
    "SSHLocation":{
      "Description":"The IP address range that can be used to SSH to the EC2 instances",
      "Type":"String",
      "MinLength":9,
      "MaxLength":18,
      "Default":"0.0.0.0/0",
      "ConstraintDescription":"Must be a valid IP CIDR range of the form x.x.x.x/x."
    },
    "Subnets":{
      "Type":"List<AWS::EC2::Subnet::Id>",
      "Description":"At least two public subnets in different Availability Zones in the selected VPC"
    },
    "VPC":{
      "Type":"AWS::EC2::VPC::Id",
      "Description":"A virtual private cloud (VPC) that enables resources in public subnets to connect to the internet"
    }
  },
  "Resources":{
    "ELBSecurityGroup":{
      "Type":"AWS::EC2::SecurityGroup",
      "Properties":{
        "GroupDescription":"ELB Security Group",
        "VpcId":{
          "Ref":"VPC"
        },
        "SecurityGroupIngress":[
          {
            "IpProtocol":"tcp",
            "FromPort":80,
            "ToPort":80,
            "CidrIp":"0.0.0.0/0"
          }
        ]
      }
    },
    "EC2SecurityGroup":{
      "Type":"AWS::EC2::SecurityGroup",
      "Properties":{
        "GroupDescription":"EC2 Security Group",
        "VpcId":{
          "Ref":"VPC"
        },
        "SecurityGroupIngress":[
          {
            "IpProtocol":"tcp",
            "FromPort":80,
            "ToPort":80,
            "SourceSecurityGroupId":{
              "Fn::GetAtt":[
                "ELBSecurityGroup",
                "GroupId"
              ]
            }
          },
          {
            "IpProtocol":"tcp",
            "FromPort":22,
            "ToPort":22,
            "CidrIp":{
              "Ref":"SSHLocation"
            }
          }
        ]
      }
    },
    "EC2TargetGroup":{
      "Type":"AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties":{
        "HealthCheckIntervalSeconds":30,
        "HealthCheckProtocol":"HTTP",
        "HealthCheckTimeoutSeconds":15,
        "HealthyThresholdCount":5,
        "Matcher":{
          "HttpCode":"200"
        },
        "Name":"EC2TargetGroup",
        "Port":80,
        "Protocol":"HTTP",
        "TargetGroupAttributes":[
          {
            "Key":"deregistration_delay.timeout_seconds",
            "Value":"20"
          }
        ],
        "UnhealthyThresholdCount":3,
        "VpcId":{
          "Ref":"VPC"
        }
      }
    },
    "ALBListener":{
      "Type":"AWS::ElasticLoadBalancingV2::Listener",
      "Properties":{
        "DefaultActions":[
          {
            "Type":"forward",
            "TargetGroupArn":{
              "Ref":"EC2TargetGroup"
            }
          }
        ],
        "LoadBalancerArn":{
          "Ref":"ApplicationLoadBalancer"
        },
        "Port":80,
        "Protocol":"HTTP"
      }
    },
    "ApplicationLoadBalancer":{
      "Type":"AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties":{
        "Scheme":"internet-facing",
        "Subnets":{
          "Ref":"Subnets"
        },
        "SecurityGroups":[
          {
            "Fn::GetAtt":[
              "ELBSecurityGroup",
              "GroupId"
            ]
          }
        ]
      }
    },
    "LaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateName":{
          "Fn::Sub":"${AWS::StackName}-launch-template"
        },
        "LaunchTemplateData":{
          "ImageId":{
            "Ref":"LatestAmiId"
          },
          "InstanceType":{
            "Ref":"InstanceType"
          },
          "KeyName":{
            "Ref":"KeyName"
          },
          "SecurityGroupIds":[
            {
              "Ref":"EC2SecurityGroup"
            }
          ],
          "UserData":{
            "Fn::Base64":{
              "Fn::Join":[
                "",
                [
                  "#!/bin/bash\n",
                  "yum update -y\n",
                  "yum install -y httpd\n",
                  "systemctl start httpd\n",
                  "systemctl enable httpd\n",
                  "echo \"<h1>Hello World!</h1>\" > /var/www/html/index.html"
                ]
              ]
            }
          }
        }
      }
    },
    "NotificationTopic":{
      "Type":"AWS::SNS::Topic",
      "Properties":{
        "Subscription":[
          {
            "Endpoint":{
              "Ref":"OperatorEmail"
            },
            "Protocol":"email"
          }
        ]
      }
    },
    "WebServerGroup":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "LaunchTemplate":{
          "LaunchTemplateId":{
            "Ref":"LaunchTemplate"
          },
          "Version":{
            "Fn::GetAtt":[
              "LaunchTemplate",
              "LatestVersionNumber"
            ]
          }
        },
        "MaxSize":"3",
        "MinSize":"1",
        "NotificationConfigurations":[
          {
            "TopicARN":{
              "Ref":"NotificationTopic"
            },
            "NotificationTypes":[
              "autoscaling:EC2_INSTANCE_LAUNCH",
              "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
              "autoscaling:EC2_INSTANCE_TERMINATE",
              "autoscaling:EC2_INSTANCE_TERMINATE_ERROR"
            ]
          }
        ],
        "TargetGroupARNs":[
          {
            "Ref":"EC2TargetGroup"
          }
        ],
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        }
      }
    }
  }
}
```

## Template walkthrough<a name="example-templates-autoscaling-description"></a>

The first part of this template specifies the `Parameters`\. Each parameter must be assigned a value at runtime for AWS CloudFormation to successfully provision the stack\. Resources specified later in the template reference these values and use the data\.
+ `InstanceType`: The type of EC2 instance that Amazon EC2 Auto Scaling provisions\. If not specified, a default of `t3.micro` is used\.
+ `KeyName`: An existing EC2 key pair to allow SSH access to the instances\.
+ `LatestAmiId`: The Amazon Machine Image \(AMI\) for the instances\. If not specified, your instances are launched with an Amazon Linux 2 AMI, using an AWS Systems Manager public parameter maintained by AWS\. For more information, see [Finding public parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/parameter-store-finding-public-parameters.html) in the *AWS Systems Manager User Guide*\.
+ `OperatorEmail`: The email address where you want to send scaling activity notifications\.
+ `SSHLocation`: The IP address range that can be used to SSH to the instances\.
+ `Subnets`: At least two public subnets in different Availability Zones\. 
+ `VPC`: A virtual private cloud \(VPC\) in your account that enables resources in public subnets to connect to the internet\. 
**Note**  
You can use the default VPC and default subnets to allow instances to access the internet\. If using your own VPC, make sure that it has a subnet mapped to each Availability Zone of the Region you are working in\. At minimum, you must have two public subnets available to create the load balancer\.

The next part of this template specifies the `Resources`\. This section specifies the stack resources and their properties\.

[AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource `ELBSecurityGroup` 
+ `SecurityGroupIngress` contains a TCP ingress rule that allows access from *all IP addresses* \("CidrIp" : "0\.0\.0\.0/0"\) on port 80\.

[AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource `EC2SecurityGroup` 
+ `SecurityGroupIngress` contains two ingress rules: 1\) a TCP ingress rule that allows SSH access \(port 22\) from the IP address range that you provide for the `SSHLocation` input parameter and 2\) a TCP ingress rule that allows access from the load balancer by specifying the load balancer's security group\. The [GetAtt](intrinsic-function-reference-getatt.md) function is used to get the ID of the security group with the logical name `ELBSecurityGroup`\.

[AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html) resource `EC2TargetGroup`
+ `Port`, `Protocol`, and `HealthCheckProtocol` specify the EC2 instance port \(80\) and protocol \(HTTP\) that the `ApplicationLoadBalancer` routes traffic to and that Elastic Load Balancing uses to check the health of the EC2 instances\.
+ `HealthCheckIntervalSeconds` specifies that the EC2 instances have an interval of 30 seconds between health checks\. The `HealthCheckTimeoutSeconds` is defined as the length of time Elastic Load Balancing waits for a response from the health check target \(15 seconds in this example\)\. After the timeout period lapses, Elastic Load Balancing marks that EC2 instance's health check as unhealthy\. When an EC2 instance fails three consecutive health checks \(`UnhealthyThresholdCount`\), Elastic Load Balancing stops routing traffic to that EC2 instance until that instance has five consecutive healthy health checks \(`HealthyThresholdCount`\)\. At that point, Elastic Load Balancing considers the instance healthy and begins routing traffic to the instance again\.
+ `TargetGroupAttributes` updates the deregistration delay value of the target group to 20 seconds\. By default, Elastic Load Balancing waits 300 seconds before completing the deregistration process\.

[AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html) resource `ALBListener`
+ `DefaultActions` specifies the port that the load balancer listens to, the target group where the load balancer forwards requests, and the protocol used to route requests\.

[AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html) resource `ApplicationLoadBalancer`
+ `Subnets` takes the value of the `Subnets` input parameter as the list of public subnets where the load balancer nodes will be created\.
+ `SecurityGroup` gets the ID of the security group that acts as a virtual firewall for your load balancer nodes to control incoming traffic\. The [GetAtt](intrinsic-function-reference-getatt.md) function is used to get the ID of the security group with the logical name `ELBSecurityGroup`\.

[AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource `LaunchTemplate`
+ `ImageId` takes the value of the `LatestAmiId` input parameter as the AMI to use\.
+ `KeyName` takes the value of the `KeyName` input parameter as the EC2 key pair to use\.
+ `SecurityGroupIds` gets the ID of the security group with the logical name `EC2SecurityGroup` that acts as a virtual firewall for your EC2 instances to control incoming traffic\.
+ `UserData` is a configuration script that runs after the instance is up and running\. In this example, the script installs Apache and creates an index\.html file\.

[AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-topic.html) resource `NotificationTopic`
+ `Subscription` takes the value of the `OperatorEmail` input parameter as the email address for the recipient of the notifications when there are any scaling activities\. 

[AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource `WebServerGroup`
+ `MinSize` and `MaxSize` set the minimum and maximum number of EC2 instances in the Auto Scaling group\.
+ `TargetGroupARNs` takes the ARN of the target group with the logical name `EC2TargetGroup`\. As this Auto Scaling group scales, it automatically registers and deregisters instances with this target group\.
+ `VPCZoneIdentifier` takes the value of the `Subnets` input parameter as the list of public subnets where the EC2 instances can be created\.

## Step 1: Launch the stack<a name="example-templates-autoscaling-launch-stack"></a>

Before you launch the stack, check that you have AWS Identity and Access Management \(IAM\) permissions to use all of the following services: Amazon EC2, Amazon EC2 Auto Scaling, AWS Systems Manager, Elastic Load Balancing, Amazon SNS, and AWS CloudFormation\. 

The following procedure involves uploading the sample stack template from a file\. Open a text editor on your local machine and add one of the templates\. Save the file with the name `sampleloadbalancedappstack.template`\.

**To launch the stack template**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Choose **Create stack**, **With new resources \(standard\)**\.

1. Under **Specify template**, choose **Upload a template file**, **Choose file** to upload the `sampleloadbalancedappstack.template` file\. 

1. Choose **Next**\.

1. On the **Specify stack details** page, type the stack name \(for example, **SampleLoadBalancedAppStack**\)\.

1. Under **Parameters**, review the parameters for the stack and provide values for all parameters that don't have default values, including **OperatorEmail**, **SSHLocation**, **KeyName**, **VPC**, and **Subnets**\.

1. Choose **Next** twice\.

1. On the **Review** page, review and confirm the settings\.

1. Choose **Submit**\.

   You can view the status of the stack in the AWS CloudFormation console in the **Status** column\. When AWS CloudFormation has successfully created the stack, you receive a status of **CREATE\_COMPLETE**\.
**Note**  
After you create the stack, you must confirm the subscription before the email address can start to receive notifications\. For more information, see [Get Amazon SNS notifications when your Auto Scaling group scales](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-sns-notifications.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Step 2: Clean up your sample resources<a name="example-templates-autoscaling-clean-up"></a>

To make sure that you aren't charged for unused sample resources, delete the stack\.

**To delete the stack**

1. In the AWS CloudFormation console, select the **SampleLoadBalancedAppStack** stack\.

1. Choose **Delete**\.

1. In the confirmation message, choose **Delete stack**\.

   The status for **SampleLoadBalancedAppStack** changes to **DELETE\_IN\_PROGRESS**\. When AWS CloudFormation completes the deletion of the stack, it removes the stack from the list\.

Use the sample template from this walkthrough to build your own stack templates\. For more information, see [Tutorial: Set up a scaled and load\-balanced application](https://docs.aws.amazon.com/autoscaling/ec2/userguide/tutorial-ec2-auto-scaling-load-balancer.html) in the *Amazon EC2 Auto Scaling User Guide*\.