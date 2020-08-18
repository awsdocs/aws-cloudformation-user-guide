# Walkthrough: Peer with an Amazon VPC in another AWS account<a name="peer-with-vpc-in-another-account"></a>

You can peer with a virtual private cloud \(VPC\) in another AWS account by using [AWS::EC2::VPCPeeringConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcpeeringconnection.html)\. This creates a networking connection between two VPCs that enables you to route traffic between them so they can communicate as if they were within the same network\. A VPC peering connection can help facilitate data access and data transfer\.

To establish a VPC peering connection, you need to authorize two separate AWS accounts within a single AWS CloudFormation stack\.

For more information about VPC peering and its limitations, see [VPC peering overview](https://docs.aws.amazon.com/vpc/latest/peering/vpc-peering-overview.html) in the *Amazon VPC Peering Guide*\.

## Prerequisites<a name="peer-with-vpc-in-another-account-prerequisites"></a>

1. You need a peer VPC ID, a peer AWS account ID, and a [cross\-account access role](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_permissions-to-switch.html) for the peering connection\.
**Note**  
This walkthrough refers to two accounts: First is an account that allows cross\-account peering \(the *accepter account*\)\. Second is an account that requests the peering connection \(the *requester account*\)\.

1. To accept the VPC peering connection, the cross\-account access role must be assumable by you\. The resource behaves the same way as a VPC peering connection resource in the same account\.

## Step 1: Create a VPC and a cross\-account role<a name="step-1-create-vpc-and-cross-account-role"></a>

 **Create a VPC and a cross\-account access role \(example\)** 

In this step, you'll create the VPC and role in the *accepter account*\.

1. In the AWS Management Console, choose **AWS CloudFormation**\.

1. Choose **Create stack**\.

1. You have several options\. To use AWS CloudFormation Designer to create a new, blank template, choose **Create template in Designer**\.

   If you are creating the template in another text editor, choose **Template is ready** and then **Amazon S3 URL** or **Upload a template file**, as appropriate\.

1. Use the following example template to create the VPC and the cross\-account role allowing another account to achieve peering\.  
**Example JSON**  

   ```
   {
     "AWSTemplateFormatVersion": "2010-09-09",
     "Description": "Create a VPC and an assumable role for cross account VPC peering.",
     "Parameters": {
       "PeerRequesterAccountId": {
         "Type": "String"
       }
     },
     "Resources": {
       "vpc": {
         "Type": "AWS::EC2::VPC",
         "Properties": {
           "CidrBlock": "10.1.0.0/16",
           "EnableDnsSupport": false,
           "EnableDnsHostnames": false,
           "InstanceTenancy": "default"
         }
       },
       "peerRole": {
         "Type": "AWS::IAM::Role",
         "Properties": {
           "AssumeRolePolicyDocument": {
             "Statement": [
               {
                 "Principal": {
                   "AWS": {
                     "Ref": "PeerRequesterAccountId"
                   }
                 },
                 "Action": [
                   "sts:AssumeRole"
                 ],
                 "Effect": "Allow"
               }
             ]
           },
           "Path": "/",
           "Policies": [
             {
               "PolicyName": "root",
               "PolicyDocument": {
                 "Version": "2012-10-17",
                 "Statement": [
                   {
                     "Effect": "Allow",
                     "Action": "ec2:AcceptVpcPeeringConnection",
                     "Resource": "*"
                   }
                 ]
               }
             }
           ]
         }
       }
     },
     "Outputs": {
       "VPCId": {
         "Value": {
           "Ref": "vpc"
         }
       },
       "RoleARN": {
         "Value": {
           "Fn::GetAtt": [
             "peerRole",
             "Arn"
           ]
         }
       }
     }
   }
   ```  
**Example YAML**  

   ```
   AWSTemplateFormatVersion: 2010-09-09
   Description: Create a VPC and an assumable role for cross account VPC peering.
   Parameters:
     PeerRequesterAccountId:
       Type: String
   Resources:
     vpc:
       Type: 'AWS::EC2::VPC'
       Properties:
         CidrBlock: 10.1.0.0/16
         EnableDnsSupport: false
         EnableDnsHostnames: false
         InstanceTenancy: default
     peerRole:
       Type: 'AWS::IAM::Role'
       Properties:
         AssumeRolePolicyDocument:
           Statement:
             - Principal:
                 AWS: !Ref PeerRequesterAccountId
               Action:
                 - 'sts:AssumeRole'
               Effect: Allow
         Path: /
         Policies:
           - PolicyName: root
             PolicyDocument:
               Version: 2012-10-17
               Statement:
                 - Effect: Allow
                   Action: 'ec2:AcceptVpcPeeringConnection'
                   Resource: '*'
   Outputs:
     VPCId:
       Value: !Ref vpc
     RoleARN:
       Value: !GetAtt 
         - peerRole
         - Arn
   ```

1. Choose **Next**\.

1. Give the stack a name \(for example, **VPC\-owner**\), and then type the AWS account ID of the *requester account* in the **PeerRequesterAccountId** field\.

1. Accept the defaults, and then choose **Next**\.

1. Choose **I acknowledge that AWS CloudFormation might create IAM resources**, and then choose **Create stack**\.

## Step 2: Create a template that includes AWS::EC2::VPCPeeringConnection<a name="step-2-create-template-for-vpc-peering-connection-owner"></a>

Now that you've created the VPC and cross\-account role, you can peer with the VPC using another AWS account \(the *requester account*\)\.

 **To create a template that includes the [AWS::EC2::VPCPeeringConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcpeeringconnection.html) resource \(example\)** 

1. Go back to the AWS CloudFormation console home page\. 

1. Choose **Create stack**\.

1. Choose **Create template in Designer** to use AWS CloudFormation Designer to create a new, blank template\.

   If you are creating the template in another text editor, choose **Template is ready** and then **Amazon S3 URL** or **Upload a template file**, as appropriate\.

1. Use the following example template to create a VPC and a VPC peering connection using the peer role you created in Step 1\.  
**Example JSON**  

   ```
   {
     "AWSTemplateFormatVersion": "2010-09-09",
     "Description": "Create a VPC and a VPC Peering connection using the PeerRole to accept.",
     "Parameters": {
       "PeerVPCAccountId": {
         "Type": "String"
       },
       "PeerVPCId": {
         "Type": "String"
       },
       "PeerRoleArn": {
         "Type": "String"
       }
     },
     "Resources": {
       "vpc": {
         "Type": "AWS::EC2::VPC",
         "Properties": {
           "CidrBlock": "10.2.0.0/16",
           "EnableDnsSupport": false,
           "EnableDnsHostnames": false,
           "InstanceTenancy": "default"
         }
       },
       "vpcPeeringConnection": {
         "Type": "AWS::EC2::VPCPeeringConnection",
         "Properties": {
           "VpcId": {
             "Ref": "vpc"
           },
           "PeerVpcId": {
             "Ref": "PeerVPCId"
           },
           "PeerOwnerId": {
             "Ref": "PeerVPCAccountId"
           },
           "PeerRoleArn": {
             "Ref": "PeerRoleArn"
           }
         }
       }
     },
     "Outputs": {
       "VPCId": {
         "Value": {
           "Ref": "vpc"
         }
       },
       "VPCPeeringConnectionId": {
         "Value": {
           "Ref": "vpcPeeringConnection"
         }
       }
     }
   }
   ```  
**Example YAML**  

   ```
   AWSTemplateFormatVersion: 2010-09-09
   Description: Create a VPC and a VPC Peering connection using the PeerRole to accept.
   Parameters:
     PeerVPCAccountId:
       Type: String
     PeerVPCId:
       Type: String
     PeerRoleArn:
       Type: String
   Resources:
     vpc:
       Type: 'AWS::EC2::VPC'
       Properties:
         CidrBlock: 10.2.0.0/16
         EnableDnsSupport: false
         EnableDnsHostnames: false
         InstanceTenancy: default
     vpcPeeringConnection:
       Type: 'AWS::EC2::VPCPeeringConnection'
       Properties:
         VpcId: !Ref vpc
         PeerVpcId: !Ref PeerVPCId
         PeerOwnerId: !Ref PeerVPCAccountId
         PeerRoleArn: !Ref PeerRoleArn
   Outputs:
     VPCId:
       Value: !Ref vpc
     VPCPeeringConnectionId:
       Value: !Ref vpcPeeringConnection
   ```

1. Choose **Next**\.

1. Give the stack a name \(for example, **VPC\-peering\-connection**\)\.

1. Accept the defaults, and then choose **Next**\.

1. Choose **I acknowledge that AWS CloudFormation might create IAM resources**, and then choose **Create stack**\.

## Creating a template with a highly restrictive policy<a name="create-template-with-highly-restrictive-policy"></a>

You might want to create a highly restrictive policy for peering your VPC with another AWS account\.

The following example template shows how to change the VPC peer owner template \(the *accepter account* created in Step 1 above\) so that it is more restrictive\.

**Example JSON**  

```
    {
        "AWSTemplateFormatVersion": "2010-09-09",
        "Description": "Create a VPC and an assumable role for cross account VPC peering.",
        
        "Parameters": {
            "PeerRequesterAccountId": {
                "Type": "String"
            }
        },
        "Resources": {
            "peerRole": {
                "Properties": {
                    "AssumeRolePolicyDocument": {
                        "Statement": [
                            {
                                "Action": [
                                    "sts:AssumeRole"
                                ],
                                "Effect": "Allow",
                                "Principal": {
                                    "AWS": {
                                        "Ref": "PeerRequesterAccountId"
                                    }
                                }
                            }
                        ]
                    },
                    "Path": "/",
                    "Policies": [
                        {
                            "PolicyDocument": {
                                "Statement": [
                                    {
                                        "Action": "ec2:acceptVpcPeeringConnection",
                                        "Effect": "Allow",
                                        "Resource": {
                                            "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}"
                                        }
                                    },
                                    {
                                        "Action": "ec2:acceptVpcPeeringConnection",
                                        "Condition": {
                                            "StringEquals": {
                                                "ec2:AccepterVpc": {
                                                    "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}"
                                                }
                                            }
                                        },
                                        "Effect": "Allow",
                                        "Resource": {
                                            "Fn::Sub": "arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc-peering-connection/*"
                                        }
                                    }
                                ],
                                "Version": "2012-10-17"
                            },
                            "PolicyName": "root"
                        }
                    ]
                },
                "Type": "AWS::IAM::Role"
            },
            "vpc": {
                "Properties": {
                    "CidrBlock": "10.1.0.0/16",
                    "EnableDnsHostnames": false,
                    "EnableDnsSupport": false,
                    "InstanceTenancy": "default"
                },
                "Type": "AWS::EC2::VPC"
            }
        },
        "Outputs": {
            "RoleARN": {
                "Value": {
                    "Fn::GetAtt": [
                        "peerRole",
                        "Arn"
                    ]
                }
            },
            "VPCId": {
                "Value": {
                    "Ref": "vpc"
                }
            }
        }
    }
```

**Example YAML**  

```
AWSTemplateFormatVersion: 2010-09-09
Description: Create a VPC and an assumable role for cross account VPC peering.
Parameters:
  PeerRequesterAccountId:
    Type: String
Resources:
  peerRole:
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Action:
              - 'sts:AssumeRole'
            Effect: Allow
            Principal:
              AWS:
                Ref: PeerRequesterAccountId
      Path: /
      Policies:
        - PolicyDocument:
            Statement:
              - Action: 'ec2:acceptVpcPeeringConnection'
                Effect: Allow
                Resource:
                  'Fn::Sub': 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}'
              - Action: 'ec2:acceptVpcPeeringConnection'
                Condition:
                  StringEquals:
                    'ec2:AccepterVpc':
                      'Fn::Sub': 'arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc/${vpc}'
                Effect: Allow
                Resource:
                  'Fn::Sub': >-
                    arn:aws:ec2:${AWS::Region}:${AWS::AccountId}:vpc-peering-connection/*
            Version: 2012-10-17
          PolicyName: root
    Type: 'AWS::IAM::Role'
  vpc:
    Properties:
      CidrBlock: 10.1.0.0/16
      EnableDnsHostnames: false
      EnableDnsSupport: false
      InstanceTenancy: default
    Type: 'AWS::EC2::VPC'
Outputs:
  RoleARN:
    Value:
      'Fn::GetAtt':
        - peerRole
        - Arn
  VPCId:
    Value:
      Ref: vpc
```

To access the VPC, you can use the same requester template as in Step 2 above\.