# Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation<a name="blue-green"></a>

You can use CloudFormation to perform ECS blue/green deployments through CodeDeploy\. Blue/green deployments are a safe deployment strategy provided by AWS CodeDeploy for minimizing interruptions caused by changing application versions\. This is accomplished by creating your new application environment, referred to as *green*, alongside your current application that is serving your live traffic, referred to as *blue*\. This allows for a period of time for monitoring and testing of the green environment before your live traffic is routed from blue to green and subsequently turning off the blue resources\.

When using CloudFormation to perform ECS blue/green deployments, you start by creating a stack template that defines the resources for both your blue and green application environments, including specifying the traffic routing and stabilization settings to use\. Next, you create a stack from that template; this generates your blue \(current\) application\. CloudFormation only creates the blue resources during stack creation\. Resources for a green deployment are not created until they are required\. 

Then, if in a future stack update you update the task definition or task set resources in your blue application, CloudFormation does the following: 
+ Generates all the necessary green application environment resources
+ Shifts the traffic based on the specified traffic routing parameters
+ Deletes the blue resources

If an error occurs at any point before the green deployment is successful and finalized, CloudFormation rolls the stack back to its state before the entire green deployment was initiated\.

To enable CloudFormation to perform blue/green deployments on a stack, include the following information in its stack template:
+ A `Transform` section in your template that invokes the `AWS::CodeDeployBlueGreen` transform, as well as a `Hook` section that invokes the `AWS::CodeDeploy::BlueGreen` hook\.
+ At least one of the ECS resources that will trigger a blue/green deployment if replaced during a stack update\. Currently, those resources are `[AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)` and `[AWS::ECS::TaskSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskset.html)`\.

Then, if you initiate a stack update that updates any properties of the above resources that requires CloudFormation to replace the resource, CloudFormation performs a blue/green deployment as described above\. For more information on resource update behavior, see [Update behaviors of stack resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html)\.

In many cases, you'll want to set up your stack template to enable blue/green deployments *before* you create the stack\. However, you can also add the ability to have CloudFormation perform blue/green deployments to an existing stack\. To do so, add the necessary information to the stack's existing template\.

In addition, we recommend you have CloudFormation generate a [change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html) for the green deployment, prior to initiating the stack update\. This enables you to review the actual changes that will be made to the stack\.

## Modeling your blue/green deployment using CloudFormation resources<a name="blue-green-required"></a>

In order to perform ECS blue/green deployment using CodeDeploy through CloudFormation, your template needs to include the resources that model your deployment, such as an Amazon ECS service and load balancer\. For more details on what these resources represent, see [Before you begin an Amazon ECS deployment](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-steps-ecs.html#deployment-steps-prerequisites-ecs) in the *AWS CodeDeploy User Guide*\.


****  

| Requirement | Resource | Required/Optional | Triggers blue/green deployment if replaced | 
| --- | --- | --- | --- | 
| Amazon ECS cluster | [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html) | Optional\. The default cluster can be used\. | No | 
| Amazon ECS service | [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html) | Required\. | No | 
| Application or Network Load Balancer | [AWS::ECS::Service LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-service-loadbalancer.html) | Required\. | No | 
| Production listener | [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html) | Required\. | No | 
| Test listener  | [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html) | Optional\. | No | 
| Two target groups | [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html) | Required\. | No | 
| Amazon ECS task definition  | [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html) | Required\. | Yes | 
| Container for your Amazon ECS application | [AWS::ECS::TaskDefinition ContainerDefinition Name](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html#cfn-ecs-taskdefinition-containerdefinition-name.html) | Required\. | No | 
| Port for your replacement task set | [AWS::ECS::TaskDefinition PortMapping ContainerPort](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions-portmappings.html#cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport.html) | Required\. | No | 

## Resource updates that trigger green deployments<a name="blue-green-resources"></a>

If you perform a stack update that updates any property that requires [replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html) for the following ECS resources, CloudFormation initiates a green deployment:
+ `[AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)`
+ `[AWS::ECS::TaskSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskset.html)` 

Updating properties in these resources that do not require resource replacement does not trigger a green deployment\.

You cannot include updates to the above resources with updates to other resources in the same stack update\. If you need to update resources in the list above as well as other resources in the same stack, do one of the following:
+ Perform two seperate stack update operations: one that includes only the updates to the above resources, and a separate stack update that includes changes to any other resources\.
+ Remove the `Transform` and `Hook` sections from your template and then perform the stack update\. In this case, CloudFormation will not perform a green deployment\.

## Considerations when managing ECS blue/green deployments using CloudFormation<a name="blue-green-considerations"></a>

You should consider the following when defining your blue/green deployment using CloudFormation:
+ Only updates to certain resources will trigger a green deployment, as discussed in [Resource updates that trigger ECS blue/green deployments](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html#blue-green-resources)\.
+ You cannot include updates to resources that trigger green deployments and updates to other resources in the same stack update, as discussed in [Resource updates that trigger ECS blue/green deployments](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html#blue-green-resources)\.
+ You can only specify a single ECS service as the deployment target\.
+ Parameters whose values are obfuscated by CloudFormation cannot be updated by the CodeDeploy service during a green deployment, and will lead to an error and stack update failure\. These include:
  + Parameters defined with the `NoEcho` attribute\.
  + Parameters that use dynamic references to retrieve their values from external services\. For more information, see [Using dynamic references to specify template values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\.
+ To cancel a green deployment that is still in progress, cancel the stack update in CloudFormation, not CodeDeploy or ECS\. For more information, see [Canceling a stack update](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn--stack-update-cancel.html)\. \(After an update has finished, you cannot cancel it\. You can, however, update a stack again with any previous settings\.\)
+ Declaring [output values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) or [importing values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-importvalue.html) from other stacks is not currently supported for templates defining blue/green ECS deployments\.
+ [Importing existing resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html) is not currently supported for templates defining blue/green ECS deployments\.
+ You cannot use the `AWS::CodeDeploy::BlueGreen` hook in a template that includes nested stack resources\.
+ You cannot use the `AWS::CodeDeploy::BlueGreen` hook in a [nested stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-nested-stacks.html)\.

For information on how using CloudFormation to perform your ECS blue/green deployments through CodeDeploy differs from a standard Amazon ECS deployment using just CodeDeploy, see [Differences between Amazon ECS Blue/Green deployments through AWS CloudFormation and standard Amazon ECS deployments](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployments-create-prerequisites.html) in the *AWS CodeDeploy User Guide*\.

## Preparing your template to perform ECS blue/green deployments<a name="blue-green-setup"></a>

To enable blue/green deployments on your stack, include the following sections in your stack template prior to performing a stack update\. 
+ Add a reference to the `AWS::CodeDeployBlueGreen` transform to your template:

  ```
      "Transform": [
          "AWS::CodeDeployBlueGreen"
      ],
  ```
+ Add a `Hook` section that invokes the `AWS::CodeDeploy::BlueGreen` hook and specifies the properties for your deployment\. Use the template reference below as a guide\.
+ In the `Resources` section, define the blue and green resources for your deployment\.

You can add these sections when you first create the template \(that is, prior to creating the stack itself\), or you can add them to an existing template before performing a stack update\. If you specify the blue/green deployment for a new stack, CloudFormation only creates the blue resources during stack creation—resources for the green deployment are not created until they are required during a stack update\.

## Reviewing the change sets for your blue/green deployment<a name="blue-green-changesets"></a>

We strongly recommend that you create a change set prior to performing a stack update that will initiate a green deployment\. This enables you to see the actual changes that will be made to your stack prior to performing stack update\. Be aware that resource changes may not be listed in the order in which they will be performed during the stack update\. For more information, see [Updating stacks using change sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html)\.

## Viewing stack events for your blue/green deployment<a name="blue-green-events"></a>

You can view the stack events generated at each step of the ECS deployment on the **Events** tab of the **Stack** page, and using the AWS CLI\. For more information, see [Monitoring the progress of a stack update](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-monitor-stack.html)\.

## Template reference<a name="blue-green-template-reference"></a>

```
"Hooks": {
      "Logical ID": {
        "Properties": {
            "TrafficRoutingConfig": {
                "Type": "Traffic routing type"
                "TimeBasedCanary": {
                    "StepPercentage": Integer,
                    "BakeTimeMins": Integer
                }
                "TimeBasedLinear": {
                    "StepPercentage": Integer,
                    "BakeTimeMins": Integer
                }
            },
              "AdditionalOptions": {
                "TerminationWaitTimeInMinutes": Integer
              },
            "LifecycleEventHooks": {
                "BeforeInstall": "FunctionName",
                "AfterInstall": "FunctionName",
                "AfterAllowTestTraffic": "FunctionName",
                "BeforeAllowTraffic": "FunctionName",
                "AfterAllowTraffic": "FunctionName"
            },
            "ServiceRole": "CodeDeployServiceRoleName",
            "Applications": [{
                "Target": {
                    "Type": "AWS::ECS::Service",
                    "LogicalID": "Resource Logical ID"
                },
                "ECSAttributes": {
                  "TaskDefinitions": ["AWS::ECS::TaskDefinition Resource Logical ID (Blue)", "AWS::ECS::TaskDefinition Resource Logical ID (Green)"],
                  "TaskSets": ["AWS::ECS::TaskSet Resource Logical ID (Blue)", "AWS::ECS::TaskSet Resource Logical ID (Green)"],
                  "TrafficRouting": {
                    "ProdTrafficRoute": {
                      "Type": "AWS::ElasticLoadBalancingV2::Listener",
                      "LogicalID": "Resource Logical ID (Production)"
                    },
                    "TestTrafficRoute": {
                      "Type": "AWS::ElasticLoadBalancingV2::Listener",                
                      "LogicalID": "Resource Logical ID (Test)"             
                    },
                    "TargetGroups": [
                      "AWS::ElasticLoadBalancingV2::TargetGroup Resource Logical ID (Blue)",
                      "AWS::ElasticLoadBalancingV2::TargetGroup Resource Logical ID (Green)"
                    ]
                  }
                }
              }
        ]
      },
        "Type": "AWS::CodeDeploy::BlueGreen"
    }
```

### Properties<a name="blue-green-template-reference-props"></a>

`Logical ID`  
The logical ID must be alphanumeric \(A\-Za\-z0\-9\) and unique within the template\.  
*Required*: Yes    
`Properties`  
Properties of the hook\.  
*Required*: Yes    
`TrafficRoutingConfig`  
Traffic routing configuration settings\.  
*Required*: No  
The default configuration is time\-based canary traffic shifting, with a 15% step percentage and a five minute bake time\.    
`Type`  
The type of traffic shifting used by the deployment configuration\.  
Valid values: AllAtOnce \| TimeBasedCanary \| TimeBasedLinear  
*Required*: Yes    
`TimeBasedCanary`  
Specifies a configuration that shifts traffic from one version of the deployment to another in two increments\.   
*Required*: Conditional: If you specify `TimeBasedCanary` as the traffic routing type, you must include the `TimeBasedCanary` parameter\.    
`StepPercentage`  
The percentage of traffic to shift in the first increment of a `TimeBasedCanary` deployment\. The step percentage must be 14% or greater\.  
*Required*: No  
`BakeTimeMins`  
The number of minutes between the first and second traffic shifts of a `TimeBasedCanary` deployment\.  
*Required*: No  
`TimeBasedLinear`  
Specifies a configuration that shifts traffic from one version of the deployment to another in equal increments, with an equal number of minutes between each increment\.  
*Required*: Conditional: If you specify `TimeBasedLinear` as the traffic routing type, you must include the `TimeBasedLinear` parameter\.    
`StepPercentage`  
The percentage of traffic that is shifted at the start of each increment of a `TimeBasedLinear` deployment\. The step percentage must be 14% or greater\.  
*Required*: No  
`BakeTimeMins`  
The number of minutes between each incremental traffic shift of a `TimeBasedLinear` deployment\.  
*Required*: No  
`AdditionalOptions`  
Additional options for the blue/green deployment\.  
*Required*: No    
`TerminationWaitTimeInMinutes`  
Specifies time to wait, in minutes, before terminating the blue resources\.  
*Required*: No  
`LifecycleEventHooks`  
Use lifecycle event hooks to specify a Lambda function that CodeDeploy can call to validate a deployment\. You can use the same function or a different one for deployment lifecyle events\. Following completion of the validation tests, the Lambda AfterAllowTraffic function calls back CodeDeploy and delivers a result of `Succeeded` or `Failed`\.  
For more information, see [AppSpec 'hooks' section](https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html) in the *AWS CodeDeploy User Guide\.*  
*Required*: No    
`BeforeInstall`  
Function to use to run tasks before the replacement task set is created\.  
*Required*: No  
`AfterInstall`  
Function to use to run tasks after the replacement task set is created and one of the target groups is associated with it\.   
*Required*: No  
`AfterAllowTestTraffic`  
Function to use to run tasks after the test listener serves traffic to the replacement task set\.   
*Required*: No  
`BeforeAllowTraffic`  
Function to use to run tasks after the second target group is associated with the replacement task set, but before traffic is shifted to the replacement task set\.   
*Required*: No  
`AfterAllowTraffic`  
Function to use to run tasks after the second target group serves traffic to the replacement task set\.   
*Required*: No  
`ServiceRole`  
The execution role for CloudFormation to use to perform the blue\-green deployments\. For a list of the necessary permissions, see [IAM permissions necessary for blue\-green deployments](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html#blue-green-iam)  
*Required*: Yes  
`Applications`  
Specifies properties of the Amazon ECS application\.  
*Required*: Yes    
`Target`  
  
*Required*: Yes    
`Type`  
The type of the resource\.  
*Required*: Yes  
`LogicalID`  
The logical id of the resource\.  
*Required*: Yes  
`ECSAttributes`  
The resources that represent the various requirements of your Amazon ECS application deployment\.  
*Required*: Yes    
`TaskDefinitions`  
The logical ID of the `[AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)` resource to run the Docker container that contains your Amazon ECS application\.   
*Required*: Yes  
`TaskSets`  
The logical IDs of the `AWS::ECS::TaskSet` resources to use as task sets for the application\.  
*Required*: Yes  
`TrafficRouting`  
Specifies resources used for traffic routing\.  
*Required*: Yes    
`ProdTrafficRoute`  
The listener to be used by your load balancer to direct traffic to your target groups\.  
*Required*: Yes    
`Type`  
The type of the resource\. AWS::ElasticLoadBalancingV2::Listener  
*Required*: Yes  
`LogicalID`  
The logical ID of the resource\.  
*Required*: Yes  
`TestTrafficRoute`  
The listener to be used by your load balancer to direct traffic to your target groups\.  
*Required*: Yes    
`Type`  
The type of the resource\. AWS::ElasticLoadBalancingV2::Listener  
*Required*: Yes  
`LogicalID`  
The logical ID of the resource\.  
*Required*: No  
`TargetGroups`  
Logical ID of resources to use as target groups to route traffic to the registered target\.  
*Required*: Yes

`Type`  
The type of hook\. AWS::CodeDeploy::BlueGreen  
*Required*: Yes

## IAM permissions necessary for blue/green deployments<a name="blue-green-iam"></a>

In order for CloudFormation to successfully perform the blue\-green deployments, you must have the following CodeDeploy permissions:
+ `codedeploy:Get*`
+ `codedeploy:CreateCloudFormationDeployment`

For more information, see [Actions, resources, and condition keys for AWS CodeDeploy](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_awscodedeploy.html) in the *AWS Identity and Access Management User Guide*\.

## Template example<a name="blue-green-template-example"></a>

The following example sets up an ECS blue/green deployment through CodeDeploy, with a traffic routing progress of 15 percent per step, with a stabilization period of 5 minutes between each step\. Creating a stack with the template would provision the initial configuration of the deployment\.

If you then made any changes to properties in the `"BlueTaskSet"` resource that require that resource be replaced, CloudFormation would then inititiate a green deployment as part of the stack update\.

### JSON<a name="blue-green-template-example.json"></a>

```
{
    "Parameters": {
        "Vpc": {
            "Type": "AWS::EC2::VPC::Id"
        },
        "Subnet1": {
            "Type": "AWS::EC2::Subnet::Id"
        },
        "Subnet2": {
            "Type": "AWS::EC2::Subnet::Id"
        }
    },
    "Transform": [
        "AWS::CodeDeployBlueGreen"
    ],
    "Hooks": {
        "CodeDeployBlueGreenHook": {
            "Properties": {
                "TrafficRoutingConfig": {
                    "Type": "TimeBasedCanary",
                    "TimeBasedCanary": {
                        "StepPercentage": 15,
                        "BakeTimeMins": 5
                    }
                },
                "Applications": [
                    {
                        "Target": {
                            "Type": "AWS::ECS::Service",
                            "LogicalID": "ECSDemoService"
                        },
                        "ECSAttributes": {
                            "TaskDefinitions": [
                                "BlueTaskDefinition",
                                "GreenTaskDefinition"
                            ],
                            "TaskSets": [
                                "BlueTaskSet",
                                "GreenTaskSet"
                            ],
                            "TrafficRouting": {
                                "ProdTrafficRoute": {
                                    "Type": "AWS::ElasticLoadBalancingV2::Listener",
                                    "LogicalID": "ALBListenerProdTraffic"
                                },
                                "TargetGroups": [
                                    "ALBTargetGroupBlue",
                                    "ALBTargetGroupGreen"
                                ]
                            }
                        }
                    }
                ]
            },
            "Type": "AWS::CodeDeploy::BlueGreen"
        }
    },
    "Resources": {
        "ExampleSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Security group for ec2 access",
                "VpcId": {
                    "Ref": "Vpc"
                },
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 80,
                        "ToPort": 80,
                        "CidrIp": "0.0.0.0/0"
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 8080,
                        "ToPort": 8080,
                        "CidrIp": "0.0.0.0/0"
                    },
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 22,
                        "ToPort": 22,
                        "CidrIp": "0.0.0.0/0"
                    }
                ]
            }
        },
        "ALBTargetGroupBlue": {
            "Type": "AWS::ElasticLoadBalancingV2::TargetGroup",
            "Properties": {
                "HealthCheckIntervalSeconds": 5,
                "HealthCheckPath": "/",
                "HealthCheckPort": "80",
                "HealthCheckProtocol": "HTTP",
                "HealthCheckTimeoutSeconds": 2,
                "HealthyThresholdCount": 2,
                "Matcher": {
                    "HttpCode": "200"
                },
                "Port": 80,
                "Protocol": "HTTP",
                "Tags": [
                    {
                        "Key": "Group",
                        "Value": "Example"
                    }
                ],
                "TargetType": "ip",
                "UnhealthyThresholdCount": 4,
                "VpcId": {
                    "Ref": "Vpc"
                }
            }
        },
        "ALBTargetGroupGreen": {
            "Type": "AWS::ElasticLoadBalancingV2::TargetGroup",
            "Properties": {
                "HealthCheckIntervalSeconds": 5,
                "HealthCheckPath": "/",
                "HealthCheckPort": "80",
                "HealthCheckProtocol": "HTTP",
                "HealthCheckTimeoutSeconds": 2,
                "HealthyThresholdCount": 2,
                "Matcher": {
                    "HttpCode": "200"
                },
                "Port": 80,
                "Protocol": "HTTP",
                "Tags": [
                    {
                        "Key": "Group",
                        "Value": "Example"
                    }
                ],
                "TargetType": "ip",
                "UnhealthyThresholdCount": 4,
                "VpcId": {
                    "Ref": "Vpc"
                }
            }
        },
        "ExampleALB": {
            "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
            "Properties": {
                "Scheme": "internet-facing",
                "SecurityGroups": [
                    {
                        "Ref": "ExampleSecurityGroup"
                    }
                ],
                "Subnets": [
                    {
                        "Ref": "Subnet1"
                    },
                    {
                        "Ref": "Subnet2"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Group",
                        "Value": "Example"
                    }
                ],
                "Type": "application",
                "IpAddressType": "ipv4"
            }
        },
        "ALBListenerProdTraffic": {
            "Type": "AWS::ElasticLoadBalancingV2::Listener",
            "Properties": {
                "DefaultActions": [
                    {
                        "Type": "forward",
                        "ForwardConfig": {
                            "TargetGroups": [
                                {
                                    "TargetGroupArn": {
                                        "Ref": "ALBTargetGroupBlue"
                                    },
                                    "Weight": 1
                                }
                            ]
                        }
                    }
                ],
                "LoadBalancerArn": {
                    "Ref": "ExampleALB"
                },
                "Port": 80,
                "Protocol": "HTTP"
            }
        },
        "ALBListenerProdRule": {
            "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
            "Properties": {
                "Actions": [
                    {
                        "Type": "forward",
                        "ForwardConfig": {
                            "TargetGroups": [
                                {
                                    "TargetGroupArn": {
                                        "Ref": "ALBTargetGroupBlue"
                                    },
                                    "Weight": 1
                                }
                            ]
                        }
                    }
                ],
                "Conditions": [
                    {
                        "Field": "http-header",
                        "HttpHeaderConfig": {
                            "HttpHeaderName": "User-Agent",
                            "Values": [
                                "Mozilla"
                            ]
                        }
                    }
                ],
                "ListenerArn": {
                    "Ref": "ALBListenerProdTraffic"
                },
                "Priority": 1
            }
        },
        "ECSTaskExecutionRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Sid": "",
                            "Effect": "Allow",
                            "Principal": {
                                "Service": "ecs-tasks.amazonaws.com"
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/service-role/AmazonECSTaskExecutionRolePolicy"
                ]
            }
        },
        "BlueTaskDefinition": {
            "Type": "AWS::ECS::TaskDefinition",
            "Properties": {
                "ExecutionRoleArn": {
                    "Fn::GetAtt": [
                        "ECSTaskExecutionRole",
                        "Arn"
                    ]
                },
                "ContainerDefinitions": [
                    {
                        "Name": "DemoApp",
                        "Image": "nginxdemos/hello:latest",
                        "Essential": true,
                        "PortMappings": [
                            {
                                "HostPort": 80,
                                "Protocol": "tcp",
                                "ContainerPort": 80
                            }
                        ]
                    }
                ],
                "RequiresCompatibilities": [
                    "FARGATE"
                ],
                "NetworkMode": "awsvpc",
                "Cpu": "256",
                "Memory": "512",
                "Family": "ecs-demo"
            }
        },
        "ECSDemoCluster": {
            "Type": "AWS::ECS::Cluster",
            "Properties": {}
        },
        "ECSDemoService": {
            "Type": "AWS::ECS::Service",
            "Properties": {
                "Cluster": {
                    "Ref": "ECSDemoCluster"
                },
                "DesiredCount": 1,
                "DeploymentController": {
                    "Type": "EXTERNAL"
                }
            }
        },
        "BlueTaskSet": {
            "Type": "AWS::ECS::TaskSet",
            "Properties": {
                "Cluster": {
                    "Ref": "ECSDemoCluster"
                },
                "LaunchType": "FARGATE",
                "NetworkConfiguration": {
                    "AwsVpcConfiguration": {
                        "AssignPublicIp": "ENABLED",
                        "SecurityGroups": [
                            {
                                "Ref": "ExampleSecurityGroup"
                            }
                        ],
                        "Subnets": [
                            {
                                "Ref": "Subnet1"
                            },
                            {
                                "Ref": "Subnet2"
                            }
                        ]
                    }
                },
                "PlatformVersion": "1.3.0",
                "Scale": {
                    "Unit": "PERCENT",
                    "Value": 1
                },
                "Service": {
                    "Ref": "ECSDemoService"
                },
                "TaskDefinition": {
                    "Ref": "BlueTaskDefinition"
                },
                "LoadBalancers": [
                    {
                        "ContainerName": "DemoApp",
                        "ContainerPort": 80,
                        "TargetGroupArn": {
                            "Ref": "ALBTargetGroupBlue"
                        }
                    }
                ]
            }
        },
        "PrimaryTaskSet": {
            "Type": "AWS::ECS::PrimaryTaskSet",
            "Properties": {
                "Cluster": {
                    "Ref": "ECSDemoCluster"
                },
                "Service": {
                    "Ref": "ECSDemoService"
                },
                "TaskSetId": {
                    "Fn::GetAtt": [
                        "BlueTaskSet",
                        "Id"
                    ]
                }
            }
        }
    }
}
```

### YAML<a name="blue-green-template-example.yaml"></a>

```
Parameters:
  Vpc:
    Type: 'AWS::EC2::VPC::Id'
  Subnet1:
    Type: 'AWS::EC2::Subnet::Id'
  Subnet2:
    Type: 'AWS::EC2::Subnet::Id'
Transform:
  - 'AWS::CodeDeployBlueGreen'
Hooks:
  CodeDeployBlueGreenHook:
    Properties:
      TrafficRoutingConfig:
        Type: TimeBasedCanary
        TimeBasedCanary:
          StepPercentage: 15
          BakeTimeMins: 5
      Applications:
        - Target:
            Type: 'AWS::ECS::Service'
            LogicalID: ECSDemoService
          ECSAttributes:
            TaskDefinitions:
              - BlueTaskDefinition
              - GreenTaskDefinition
            TaskSets:
              - BlueTaskSet
              - GreenTaskSet
            TrafficRouting:
              ProdTrafficRoute:
                Type: 'AWS::ElasticLoadBalancingV2::Listener'
                LogicalID: ALBListenerProdTraffic
              TargetGroups:
                - ALBTargetGroupBlue
                - ALBTargetGroupGreen
    Type: 'AWS::CodeDeploy::BlueGreen'
Resources:
  ExampleSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Security group for ec2 access
      VpcId: !Ref Vpc
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: 8080
          ToPort: 8080
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: 0.0.0.0/0
  ALBTargetGroupBlue:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      HealthCheckIntervalSeconds: 5
      HealthCheckPath: /
      HealthCheckPort: '80'
      HealthCheckProtocol: HTTP
      HealthCheckTimeoutSeconds: 2
      HealthyThresholdCount: 2
      Matcher:
        HttpCode: '200'
      Port: 80
      Protocol: HTTP
      Tags:
        - Key: Group
          Value: Example
      TargetType: ip
      UnhealthyThresholdCount: 4
      VpcId: !Ref Vpc
  ALBTargetGroupGreen:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      HealthCheckIntervalSeconds: 5
      HealthCheckPath: /
      HealthCheckPort: '80'
      HealthCheckProtocol: HTTP
      HealthCheckTimeoutSeconds: 2
      HealthyThresholdCount: 2
      Matcher:
        HttpCode: '200'
      Port: 80
      Protocol: HTTP
      Tags:
        - Key: Group
          Value: Example
      TargetType: ip
      UnhealthyThresholdCount: 4
      VpcId: !Ref Vpc
  ExampleALB:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Scheme: internet-facing
      SecurityGroups:
        - !Ref ExampleSecurityGroup
      Subnets:
        - !Ref Subnet1
        - !Ref Subnet2
      Tags:
        - Key: Group
          Value: Example
      Type: application
      IpAddressType: ipv4
  ALBListenerProdTraffic:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          ForwardConfig:
            TargetGroups:
              - TargetGroupArn: !Ref ALBTargetGroupBlue
                Weight: 1
      LoadBalancerArn: !Ref ExampleALB
      Port: 80
      Protocol: HTTP
  ALBListenerProdRule:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          ForwardConfig:
            TargetGroups:
              - TargetGroupArn: !Ref ALBTargetGroupBlue
                Weight: 1
      Conditions:
        - Field: http-header
          HttpHeaderConfig:
            HttpHeaderName: User-Agent
            Values:
              - Mozilla
      ListenerArn: !Ref ALBListenerProdTraffic
      Priority: 1
  ECSTaskExecutionRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: ecs-tasks.amazonaws.com
            Action: 'sts:AssumeRole'
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonECSTaskExecutionRolePolicy'
  BlueTaskDefinition:
    Type: 'AWS::ECS::TaskDefinition'
    Properties:
      ExecutionRoleArn: !GetAtt 
        - ECSTaskExecutionRole
        - Arn
      ContainerDefinitions:
        - Name: DemoApp
          Image: 'nginxdemos/hello:latest'
          Essential: true
          PortMappings:
            - HostPort: 80
              Protocol: tcp
              ContainerPort: 80
      RequiresCompatibilities:
        - FARGATE
      NetworkMode: awsvpc
      Cpu: '256'
      Memory: '512'
      Family: ecs-demo
  ECSDemoCluster:
    Type: 'AWS::ECS::Cluster'
    Properties: {}
  ECSDemoService:
    Type: 'AWS::ECS::Service'
    Properties:
      Cluster: !Ref ECSDemoCluster
      DesiredCount: 1
      DeploymentController:
        Type: EXTERNAL
  BlueTaskSet:
    Type: 'AWS::ECS::TaskSet'
    Properties:
      Cluster: !Ref ECSDemoCluster
      LaunchType: FARGATE
      NetworkConfiguration:
        AwsVpcConfiguration:
          AssignPublicIp: ENABLED
          SecurityGroups:
            - !Ref ExampleSecurityGroup
          Subnets:
            - !Ref Subnet1
            - !Ref Subnet2
      PlatformVersion: 1.3.0
      Scale:
        Unit: PERCENT
        Value: 1
      Service: !Ref ECSDemoService
      TaskDefinition: !Ref BlueTaskDefinition
      LoadBalancers:
        - ContainerName: DemoApp
          ContainerPort: 80
          TargetGroupArn: !Ref ALBTargetGroupBlue
  PrimaryTaskSet:
    Type: 'AWS::ECS::PrimaryTaskSet'
    Properties:
      Cluster: !Ref ECSDemoCluster
      Service: !Ref ECSDemoService
      TaskSetId: !GetAtt 
        - BlueTaskSet
        - Id
```