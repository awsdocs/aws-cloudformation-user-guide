# AWS::ECS::ClusterCapacityProviderAssociations<a name="aws-resource-ecs-clustercapacityproviderassociations"></a>

The `AWS::ECS::ClusterCapacityProviderAssociations` resource associates one or more capacity providers and a default capacity provider strategy with a cluster\.

## Syntax<a name="aws-resource-ecs-clustercapacityproviderassociations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-clustercapacityproviderassociations-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::ClusterCapacityProviderAssociations",
  "Properties" : {
      "[CapacityProviders](#cfn-ecs-clustercapacityproviderassociations-capacityproviders)" : [ String, ... ],
      "[Cluster](#cfn-ecs-clustercapacityproviderassociations-cluster)" : String,
      "[DefaultCapacityProviderStrategy](#cfn-ecs-clustercapacityproviderassociations-defaultcapacityproviderstrategy)" : [ CapacityProviderStrategy, ... ]
    }
}
```

### YAML<a name="aws-resource-ecs-clustercapacityproviderassociations-syntax.yaml"></a>

```
Type: AWS::ECS::ClusterCapacityProviderAssociations
Properties: 
  [CapacityProviders](#cfn-ecs-clustercapacityproviderassociations-capacityproviders): 
    - String
  [Cluster](#cfn-ecs-clustercapacityproviderassociations-cluster): String
  [DefaultCapacityProviderStrategy](#cfn-ecs-clustercapacityproviderassociations-defaultcapacityproviderstrategy): 
    - CapacityProviderStrategy
```

## Properties<a name="aws-resource-ecs-clustercapacityproviderassociations-properties"></a>

`CapacityProviders`  <a name="cfn-ecs-clustercapacityproviderassociations-capacityproviders"></a>
The capacity providers to associate with the cluster\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cluster`  <a name="cfn-ecs-clustercapacityproviderassociations-cluster"></a>
The cluster the capacity provider association is the target of\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultCapacityProviderStrategy`  <a name="cfn-ecs-clustercapacityproviderassociations-defaultcapacityproviderstrategy"></a>
The default capacity provider strategy to associate with the cluster\.  
*Required*: Yes  
*Type*: List of [CapacityProviderStrategy](aws-properties-ecs-clustercapacityproviderassociations-capacityproviderstrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecs-clustercapacityproviderassociations-return-values"></a>

### Ref<a name="aws-resource-ecs-clustercapacityproviderassociations-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the cluster name\.

## Examples<a name="aws-resource-ecs-clustercapacityproviderassociations--examples"></a>



### Creating a cluster capacity provider association using an Auto Scaling group capacity provider\.<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an_Auto_Scaling_group_capacity_provider."></a>

The following example creates a cluster, two Auto Scaling group capacity providers, and the cluster capacity provider association that facilitates the association between them\. The Auto Scaling groups the capacity providers use must already be created and the Amazon Resource Name \(ARN\) of each Auto Scaling group must be specified as parameters\.

#### JSON<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an_Auto_Scaling_group_capacity_provider.--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "AutoScalingGroupArn1": {
            "Type": "String"
        },
        "AutoScalingGroupArn2": {
            "Type": "String"
        }
    },
    "Resources": {
        "CapacityProvider1": {
            "Type": "AWS::ECS::CapacityProvider",
            "Properties": {
                "AutoScalingGroupProvider": {
                    "AutoScalingGroupArn": {
                        "Ref": "AutoScalingGroupArn1"
                    },
                    "ManagedScaling": {
                        "Status": "ENABLED"
                    },
                    "ManagedTerminationProtection": "DISABLED"
                }
            }
        },
        "CapacityProvider2": {
            "Type": "AWS::ECS::CapacityProvider",
            "Properties": {
                "AutoScalingGroupProvider": {
                    "AutoScalingGroupArn": {
                        "Ref": "AutoScalingGroupArn2"
                    },
                    "ManagedScaling": {
                        "Status": "ENABLED"
                    },
                    "ManagedTerminationProtection": "DISABLED"
                }
            }
        },
        "Cluster": {
            "Type": "AWS::ECS::Cluster"
        },
        "ClusterCPAssociation": {
            "Type": "AWS::ECS::ClusterCapacityProviderAssociations",
            "Properties": {
                "Cluster": {
                    "Ref": "Cluster"
                },
                "CapacityProviders": [
                    {
                        "Ref": "CapacityProvider1"
                    },
                    {
                        "Ref": "CapacityProvider2"
                    }
                ],
                "DefaultCapacityProviderStrategy": [
                    {
                        "Base": 2,
                        "Weight": 6,
                        "CapacityProvider": {
                            "Ref": "CapacityProvider1"
                        }
                    },
                    {
                        "Base": 0,
                        "Weight": 10,
                        "CapacityProvider": {
                            "Ref": "CapacityProvider2"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an_Auto_Scaling_group_capacity_provider.--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  AutoScalingGroupArn1:  
    Type: String
  AutoScalingGroupArn2:  
    Type: String
Resources:
  CapacityProvider1:
    Type: "AWS::ECS::CapacityProvider"
    Properties:
      AutoScalingGroupProvider:
        AutoScalingGroupArn: !Ref AutoScalingGroupArn1
        ManagedScaling:
          Status: ENABLED
        ManagedTerminationProtection: DISABLED
  CapacityProvider2:
    Type: "AWS::ECS::CapacityProvider"
    Properties:
      AutoScalingGroupProvider:
        AutoScalingGroupArn: !Ref AutoScalingGroupArn2
        ManagedScaling:
          Status: ENABLED
        ManagedTerminationProtection: DISABLED
  Cluster:
    Type: 'AWS::ECS::Cluster'
  ClusterCPAssociation:
    Type: "AWS::ECS::ClusterCapacityProviderAssociations"
    Properties:
      Cluster: !Ref Cluster
      CapacityProviders:
        - !Ref CapacityProvider1
        - !Ref CapacityProvider2
      DefaultCapacityProviderStrategy:
        - Base: 2
          Weight: 6
          CapacityProvider: !Ref CapacityProvider1
        - Base: 0
          Weight: 10
          CapacityProvider: !Ref CapacityProvider2
```

### Creating a cluster capacity provider association using an AWS Fargate capacity provider\.<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an__capacity_provider."></a>

The following example associates the `FARGATE` and `FARGATE_SPOT` capacity providers to an existing cluster\. The cluster name must be specified as a parameter\.

#### JSON<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an__capacity_provider.--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "ClusterName": {
            "Type": "String"
        }
    },
    "Resources": {
        "ClusterCPAssociation": {
            "Type": "AWS::ECS::ClusterCapacityProviderAssociations",
            "Properties": {
                "Cluster": {
                    "Ref": "ClusterName"
                },
                "CapacityProviders": [
                    "FARGATE",
                    "FARGATE_SPOT"
                ],
                "DefaultCapacityProviderStrategy": [
                    {
                        "Base": 2,
                        "Weight": 1,
                        "CapacityProvider": "FARGATE"
                    },
                    {
                        "Base": 0,
                        "Weight": 1,
                        "CapacityProvider": "FARGATE_SPOT"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_using_an__capacity_provider.--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  ClusterName:  
    Type: String
Resources:
  ClusterCPAssociation:
    Type: "AWS::ECS::ClusterCapacityProviderAssociations"
    Properties:
      Cluster: !Ref ClusterName
      CapacityProviders:
        - "FARGATE"
        - "FARGATE_SPOT"
      DefaultCapacityProviderStrategy:
        - Base: 2
          Weight: 1
          CapacityProvider: "FARGATE"
        - Base: 0
          Weight: 1
          CapacityProvider: "FARGATE_SPOT"
```

### Creating a cluster capacity provider association and Auto Scaling group capacity provider\.<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_and_Auto_Scaling_group_capacity_provider."></a>

The following is an example of how you could use a Lambda function to create an Auto Scaling group, retrieve the Amazon Resource Name \(ARN\) of the Auto Scaling group, and then use the ARN to create an Auto Scaling group capacity provider, cluster, and the capacity provider association that facilitates the association between them\.

#### JSON<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_and_Auto_Scaling_group_capacity_provider.--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "LatestAmiId": {
            "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>",
            "Default": "/aws/service/ecs/optimized-ami/amazon-linux-2/recommended/image_id"
        }
    },
    "Resources": {
        "AutoScalingReadAccessForLambdaRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "lambda.amazonaws.com"
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
                        "PolicyName": "LambdaReadAsgPolicy",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": "autoscaling:DescribeAutoScalingGroups",
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "AsgArnLambda": {
            "Type": "AWS::Lambda::Function",
            "Properties": {
                "Runtime": "python2.7",
                "Handler": "index.handler",
                "Role": {
                    "Fn::GetAtt": [
                        "AutoScalingReadAccessForLambdaRole",
                        "Arn"
                    ]
                },
                "Timeout": 50,
                "Code": {
                    "ZipFile": "import cfnresponse\nimport json\nimport boto3\nclient = boto3.client('autoscaling')\ndef handler(event, context):\n  response_data = {}\n  try:\n    autoScalingGroupName = event['ResourceProperties']['AsgName']\n    asg_arn = client.describe_auto_scaling_groups(AutoScalingGroupNames=[autoScalingGroupName])['AutoScalingGroups'][0]['AutoScalingGroupARN']\n    response_data['arn'] = asg_arn\n    cfnresponse.send(event, context, cfnresponse.SUCCESS, response_data, 'AsgArnString')\n  except Exception as e:\n    response_data['exception'] = e\n    cfnresponse.send(event, context, cfnresponse.FAILED, response_data, 'AsgArnString')\n"
                }
            }
        },
        "LaunchConfig": {
            "Type": "AWS::AutoScaling::LaunchConfiguration",
            "Properties": {
                "ImageId": {
                    "Ref": "LatestAmiId"
                },
                "InstanceType": "t3.micro",
                "UserData": {
                    "Fn::Base64": {
                        "Fn::Sub": "#!/bin/bash -xe\necho ECS_CLUSTER=${Cluster} >> /etc/ecs/ecs.config\n"
                    }
                }
            }
        },
        "AutoScalingGroup": {
            "Type": "AWS::AutoScaling::AutoScalingGroup",
            "Properties": {
                "AvailabilityZones": {
                    "Fn::GetAZs": {
                        "Ref": "AWS::Region"
                    }
                },
                "HealthCheckGracePeriod": 60,
                "LaunchConfigurationName": {
                    "Ref": "LaunchConfig"
                },
                "MaxSize": "0",
                "MinSize": "0"
            }
        },
        "AsgArn": {
            "Type": "AWS::CloudFormation::CustomResource",
            "Properties": {
                "ServiceToken": {
                    "Fn::GetAtt": [
                        "AsgArnLambda",
                        "Arn"
                    ]
                },
                "AsgName": {
                    "Ref": "AutoScalingGroup"
                }
            }
        },
        "CapacityProvider": {
            "Type": "AWS::ECS::CapacityProvider",
            "Properties": {
                "AutoScalingGroupProvider": {
                    "AutoScalingGroupArn": {
                        "Fn::GetAtt": [
                            "AsgArn",
                            "arn"
                        ]
                    },
                    "ManagedScaling": {
                        "Status": "ENABLED"
                    },
                    "ManagedTerminationProtection": "DISABLED"
                }
            }
        },
        "Cluster": {
            "Type": "AWS::ECS::Cluster"
        },
        "ClusterCPAssoc": {
            "Type": "AWS::ECS::ClusterCapacityProviderAssociations",
            "Properties": {
                "Cluster": {
                    "Ref": "Cluster"
                },
                "CapacityProviders": [
                    {
                        "Ref": "CapacityProvider"
                    }
                ],
                "DefaultCapacityProviderStrategy": [
                    {
                        "Base": 0,
                        "Weight": 1,
                        "CapacityProvider": {
                            "Ref": "CapacityProvider"
                        }
                    }
                ]
            }
        }
    },
    "Outputs": {
        "ClusterArn": {
            "Value": {
                "Fn::GetAtt": [
                    "Cluster",
                    "Arn"
                ]
            }
        },
        "ClusterName": {
            "Value": {
                "Ref": "Cluster"
            }
        },
        "CapacityProviderName": {
            "Value": {
                "Ref": "CapacityProvider"
            }
        },
        "AsgArn": {
            "Value": {
                "Fn::GetAtt": [
                    "AsgArn",
                    "arn"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecs-clustercapacityproviderassociations--examples--Creating_a_cluster_capacity_provider_association_and_Auto_Scaling_group_capacity_provider.--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:  
  LatestAmiId:
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
    Default: '/aws/service/ecs/optimized-ami/amazon-linux-2/recommended/image_id'
Resources:
  # Custom resources to retrieve the Auto Scaling group ARN
  AutoScalingReadAccessForLambdaRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - "lambda.amazonaws.com"
            Action:
              - "sts:AssumeRole"
      Policies:
        - PolicyName: LambdaReadAsgPolicy
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              - Effect: Allow
                Action: "autoscaling:DescribeAutoScalingGroups"
                Resource: "*"
  AsgArnLambda:
    Type: "AWS::Lambda::Function"
    Properties:
      Runtime: "python2.7"
      Handler: "index.handler"
      Role:
        !GetAtt [ AutoScalingReadAccessForLambdaRole, Arn ]
      Timeout: 50
      Code:
        ZipFile: |
          import cfnresponse
          import json
          import boto3
          client = boto3.client('autoscaling')
          def handler(event, context):
            response_data = {}
            try:
              autoScalingGroupName = event['ResourceProperties']['AsgName']
              asg_arn = client.describe_auto_scaling_groups(AutoScalingGroupNames=[autoScalingGroupName])['AutoScalingGroups'][0]['AutoScalingGroupARN']
              response_data['arn'] = asg_arn
              cfnresponse.send(event, context, cfnresponse.SUCCESS, response_data, 'AsgArnString')
            except Exception as e:
              response_data['exception'] = e
              cfnresponse.send(event, context, cfnresponse.FAILED, response_data, 'AsgArnString')
  # Main resources
  LaunchConfig:
    Type: AWS::AutoScaling::LaunchConfiguration
    Properties:
      ImageId: !Ref LatestAmiId
      InstanceType: "t3.micro"
      UserData:
        Fn::Base64: !Sub |
          #!/bin/bash -xe
          echo ECS_CLUSTER=${Cluster} >> /etc/ecs/ecs.config
  AutoScalingGroup:
    Type: "AWS::AutoScaling::AutoScalingGroup"
    Properties:
      AvailabilityZones:
        Fn::GetAZs: !Ref "AWS::Region"
      HealthCheckGracePeriod: 60
      LaunchConfigurationName: !Ref LaunchConfig
      MaxSize: "0"
      MinSize: "0"
  AsgArn:
    Type: "AWS::CloudFormation::CustomResource"
    Properties:
      ServiceToken: !GetAtt [ AsgArnLambda, Arn ]
      AsgName: !Ref AutoScalingGroup
  CapacityProvider:
    Type: "AWS::ECS::CapacityProvider"
    Properties:
      AutoScalingGroupProvider:
        AutoScalingGroupArn: !GetAtt [ AsgArn, arn ]
        ManagedScaling:
          Status: ENABLED
        ManagedTerminationProtection: DISABLED
  Cluster:
    Type: 'AWS::ECS::Cluster'
  ClusterCPAssoc:
    Type: "AWS::ECS::ClusterCapacityProviderAssociations"
    Properties:
      Cluster: !Ref Cluster
      CapacityProviders:
        - !Ref CapacityProvider
      DefaultCapacityProviderStrategy:
        - Base: 0
          Weight: 1
          CapacityProvider: !Ref CapacityProvider
Outputs:
  ClusterArn:
    Value: !GetAtt
      - Cluster
      - Arn
  ClusterName:
    Value: !Ref Cluster
  CapacityProviderName:
    Value: !Ref CapacityProvider
  AsgArn:
    Value: !GetAtt [ AsgArn, arn ]
```