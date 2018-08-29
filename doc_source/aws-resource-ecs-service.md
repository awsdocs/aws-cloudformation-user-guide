# AWS::ECS::Service<a name="aws-resource-ecs-service"></a>

The `AWS::ECS::Service` resource creates an Amazon Elastic Container Service \(Amazon ECS\) service that runs and maintains the requested number of tasks and associated load balancers\.

**Topics**
+ [Syntax](#aws-resource-ecs-service-syntax)
+ [Properties](#w3ab2c21c10d563b9)
+ [Return Values](#w3ab2c21c10d563c11)
+ [Examples](#w3ab2c21c10d563c13)
+ [More Info](#w3ab2c21c10d563c15)

## Syntax<a name="aws-resource-ecs-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-service-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::Service",
  "Properties" : {
    "[Cluster](#cfn-ecs-service-cluster)" : String,
    "[DeploymentConfiguration](#cfn-ecs-service-deploymentconfiguration)" : DeploymentConfiguration,
    "[DesiredCount](#cfn-ecs-service-desiredcount)" : Integer,
    "[HealthCheckGracePeriodSeconds](#cfn-ecs-service-healthcheckgraceperiodseconds)" : Integer,
    "[LaunchType](#cfn-ecs-service-launchtype)" : String,
    "[LoadBalancers](#cfn-ecs-service-loadbalancers)" : [ Load Balancer Objects, ... ],
    "[NetworkConfiguration](#cfn-ecs-service-networkconfiguration)" : [*NetworkConfiguration*](aws-properties-ecs-service-networkconfiguration.md),
    "[PlacementConstraints](#cfn-ecs-service-placementconstraints)" : [ PlacementConstraints, ... ],
    "[Role](#cfn-ecs-service-role)" : String,
    "[PlacementStrategies](#cfn-ecs-service-placementstrategies)" : [ PlacementStrategies, ... ],
    "[PlatformVersion](#cfn-ecs-service-platformversion)" : String,
    "[ServiceName](#cfn-ecs-service-servicename)" : String,
    "[ServiceRegistries](#cfn-ecs-service-serviceregistries)" : [ [*ServiceRegistry*](aws-properties-ecs-service-serviceregistry.md), ... ,
    "[TaskDefinition](#cfn-ecs-service-taskdefinition)" : String
  }
}
```

### YAML<a name="aws-resource-ecs-service-syntax.yaml"></a>

```
Type: "AWS::ECS::Service"
Properties: 
  [Cluster](#cfn-ecs-service-cluster): String
  [DeploymentConfiguration](#cfn-ecs-service-deploymentconfiguration):
    DeploymentConfiguration
  [DesiredCount](#cfn-ecs-service-desiredcount): Integer
  [HealthCheckGracePeriodSeconds](#cfn-ecs-service-healthcheckgraceperiodseconds): Integer
  [LaunchType](#cfn-ecs-service-launchtype): String
  [LoadBalancers](#cfn-ecs-service-loadbalancers):
    - Load Balancer Objects, ...
  [NetworkConfiguration](#cfn-ecs-service-networkconfiguration): 
    [*NetworkConfiguration*](aws-properties-ecs-service-networkconfiguration.md)
  [PlacementConstraints](#cfn-ecs-service-placementconstraints): 
   - PlacementConstraints, ...
  [PlacementStrategies](#cfn-ecs-service-placementstrategies): 
   - PlacementStrategies, ...
  [PlatformVersion](#cfn-ecs-service-platformversion): String
  [Role](#cfn-ecs-service-role): String
  [ServiceName](#cfn-ecs-service-servicename): String
  [ServiceRegistries](#cfn-ecs-service-serviceregistries): 
   - [*ServiceRegistry*](aws-properties-ecs-service-serviceregistry.md)
  [TaskDefinition](#cfn-ecs-service-taskdefinition): String
```

## Properties<a name="w3ab2c21c10d563b9"></a>

For more information on properties and valid parameters, see [CreateService](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_CreateService.html)in the *Amazon Elastic Container Service API Reference*\.

**Note**  
When you use Auto Scaling or Amazon Elastic Compute Cloud \(Amazon EC2\) to create container instances for an Amazon ECS cluster, the Amazon ECS service resource must have a dependency on the Auto Scaling group or the Amazon EC2 instances\. This makes the container instances available and associates them with the Amazon ECS cluster before AWS CloudFormation creates the Amazon ECS service\.

`Cluster`  <a name="cfn-ecs-service-cluster"></a>
The name or Amazon Resource Name \(ARN\) of the cluster that you want to run your Amazon ECS service on\. If you do not specify a cluster, Amazon ECS uses the default cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DeploymentConfiguration`  <a name="cfn-ecs-service-deploymentconfiguration"></a>
Configures how many tasks run during a deployment\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service Service DeploymentConfiguration](aws-properties-ecs-service-deploymentconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DesiredCount`  <a name="cfn-ecs-service-desiredcount"></a>
The number of simultaneous tasks that you want to run on the cluster\. Specify the tasks with the `TaskDefinition` property\.  
*Required*: Conditional\. Required only when creating an Amazon ECS Service\.  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckGracePeriodSeconds`  <a name="cfn-ecs-service-healthcheckgraceperiodseconds"></a>
The period of time, in seconds, that the Amazon ECS service scheduler ignores unhealthy Elastic Load Balancing target health checks after a task has first started\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LaunchType`  <a name="cfn-ecs-service-launchtype"></a>
The launch type on which to run your service\. If one is not specified, `EC2` will be used by default\. Valid values include `EC2` and `FARGATE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LoadBalancers`  <a name="cfn-ecs-service-loadbalancers"></a>
A list of load balancer objects to associate with the cluster\. If you specify the `Role` property, `LoadBalancers` must be specified as well\. For information about the number of load balancers that you can specify per service, see [Service Load Balancing](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-load-balancing.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: Conditional  
*Type*: List of [Amazon Elastic Container Service Service LoadBalancers](aws-properties-ecs-service-loadbalancers.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NetworkConfiguration`  <a name="cfn-ecs-service-networkconfiguration"></a>
The network configuration for the service\. This parameter is required for task definitions that use the `awsvpc` network mode to receive their own Elastic Network Interface, and it is not supported for other network modes\. For more information, see [Task Networking](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/developerguidetask-networking.html) in the *Amazon Elastic Container Service Developer Guide*\.  
 *Required*: No  
 *Type*: [Amazon ECS Service NetworkConfiguration](aws-properties-ecs-service-networkconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PlacementConstraints`  <a name="cfn-ecs-service-placementconstraints"></a>
The placement constraints for the tasks in the service\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service Service PlacementConstraint](aws-properties-ecs-service-placementconstraints-placementconstraint.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PlacementStrategies`  <a name="cfn-ecs-service-placementstrategies"></a>
The placement strategies that determine how tasks for the service are placed\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service Service PlacementStrategies](aws-properties-ecs-service-placementstrategies-placementstrategy.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PlatformVersion`  <a name="cfn-ecs-service-platformversion"></a>
The platform version on which to run your service\. If one is not specified, the latest version will be used by default\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Role`  <a name="cfn-ecs-service-role"></a>
The name or ARN of an AWS Identity and Access Management \(IAM\) role that allows your Amazon ECS container agent to make calls to your load balancer\.  
In some cases, you might need to add a dependency on the service role's policy\. For more information, see IAM role policy in [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required*: Conditional\. Required only if you specify the `LoadBalancers` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceName`  <a name="cfn-ecs-service-servicename"></a>
The name of your service\. The name is limited to 255 letters \(uppercase and lowercase\), numbers, hyphens, and underscores\. Service names must be unique within a cluster, but you can have similarly named services in multiple clusters within a region or across multiple regions\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceRegistries`  <a name="cfn-ecs-service-serviceregistries"></a>
Details of the service registry\.  
*Required*: No  
*Type*: [Amazon ECS Service ServiceRegistry](aws-properties-ecs-service-serviceregistry.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TaskDefinition`  <a name="cfn-ecs-service-taskdefinition"></a>
The ARN of the task definition \(including the revision number\) that you want to run on the cluster, such as `arn:aws:ecs:us-east-1:123456789012:task-definition/mytask:3`\. You can't use `:latest` to specify a revision because it's ambiguous\. For example, if AWS CloudFormation needed to roll back an update, it wouldn't know which revision to roll back to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

## Return Values<a name="w3ab2c21c10d563c11"></a>

### Ref<a name="w3ab2c21c10d563c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN\.

In the following sample, the `Ref` function returns the ARN of the `MyECSService` service, such as `arn:aws:ecs:us-west-2:123456789012:service/sample-webapp`\.

```
{ "Ref": "MyECSService" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d563c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
The name of the Amazon ECS service, such as `sample-webapp`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d563c13"></a>

### Define a Basic Amazon ECS Service<a name="w3ab2c21c10d563c13b2"></a>

The following examples define an Amazon ECS service that uses a cluster and task definition that are declared elsewhere in the same template\.

#### JSON<a name="aws-resource-ecs-service-example.json"></a>

```
"WebApp": {
  "Type": "AWS::ECS::Service",
  "Properties" : {
    "Cluster": { "Ref": "cluster" },
    "DesiredCount": { "Ref": "desiredcount" },
    "TaskDefinition" : { "Ref": "taskdefinition" }
  }
}
```

#### YAML<a name="aws-resource-ecs-service-example.yaml"></a>

```
WebApp: 
  Type: "AWS::ECS::Service"
  Properties: 
    Cluster: 
      Ref: "cluster"
    DesiredCount: 
      Ref: "desiredcount"
    TaskDefinition: 
      Ref: "taskdefinition"
```

### Associate an Application Load Balancer with a Service<a name="w3ab2c21c10d563c13b4"></a>

The following example associates an Application Load Balancer with an Amazon ECS service by referencing an `AWS::ElasticLoadBalancingV2::TargetGroup` resource\. 

**Note**  
The Amazon ECS service requires an explicit dependency on the Application load balancer listener rule and the Application load balancer listener\. This prevents the service from starting before the listener is ready\.

#### JSON<a name="aws-resource-ecs-service-example-2.json"></a>

```
"service" : {
  "Type" : "AWS::ECS::Service",
  "DependsOn": ["Listener"],
  "Properties" : {
    "Role" : { "Ref" : "ECSServiceRole" },
    "TaskDefinition" : { "Ref" : "taskdefinition" },
    "DesiredCount" : "1",
    "LoadBalancers" : [{
      "TargetGroupArn" : { "Ref" : "TargetGroup" },
      "ContainerPort" : "80",
      "ContainerName" : "sample-app"
    }],
    "Cluster" : { "Ref" : "ECSCluster" }
  }
}
```

#### YAML<a name="aws-resource-ecs-service-example-2.yaml"></a>

```
service:
  Type: AWS::ECS::Service
  DependsOn:
  - Listener
  Properties:
    Role:
      Ref: ECSServiceRole
    TaskDefinition:
      Ref: taskdefinition
    DesiredCount: 1
    LoadBalancers:
    - TargetGroupArn:
        Ref: TargetGroup
      ContainerPort: 80
      ContainerName: sample-app
    Cluster:
      Ref: ECSCluster
```

### Define a Service with a Health Check Grace Period<a name="w3ab2c21c10d563c13b6"></a>

The following example defines a service with a parameter that enables users to specify how many seconds that the Amazon ECS service scheduler should ignore unhealthy Elastic Load Balancing target health checks after a task has first started\.

#### JSON<a name="aws-resource-ecs-service-example3.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Description" : "Creating ECS service",
  "Parameters": {
    "AppName": {
      "Type":"String",
      "Description": "Name of app requiring ELB exposure",
      "Default": "simple-app"
    },
    "AppContainerPort": {
      "Type":"Number",
      "Description": "Container port of app requiring ELB exposure",
      "Default": "80"
    },
    "AppHostPort": {
      "Type":"Number",
      "Description": "Host port of app requiring ELB exposure",
      "Default": "80"
    },
    "ServiceName": {
      "Type": "String"
    },
    "LoadBalancerName": {
      "Type": "String"
    },
    "HealthCheckGracePeriodSeconds": {
      "Type": "String"
    }
  },
  "Resources": {
    "cluster": {
      "Type": "AWS::ECS::Cluster"
    },
    "taskdefinition": {
      "Type": "AWS::ECS::TaskDefinition",
      "Properties" : {
        "ContainerDefinitions" : [
          {
            "Name": {"Ref": "AppName"},
            "MountPoints": [
              {
                "SourceVolume": "my-vol",
                "ContainerPath": "/var/www/my-vol"
              }
            ],
            "Image":"amazon/amazon-ecs-sample",
            "Cpu": "10",
            "PortMappings":[
              {
                "ContainerPort": {"Ref":"AppContainerPort"},
                "HostPort": {"Ref":"AppHostPort"}
              }
            ],
            "EntryPoint": [
              "/usr/sbin/apache2",
              "-D",
              "FOREGROUND"
            ],
            "Memory":"500",
            "Essential": "true"
          },
          {
            "Name": "busybox",
            "Image": "busybox",
            "Cpu": "10",
            "EntryPoint": [
              "sh",
              "-c"
            ],
            "Memory": "500",
            "Command": [
              "/bin/sh -c \"while true; do /bin/date > /var/www/my-vol/date; sleep 1; done\""
            ],
            "Essential" : "false",
            "VolumesFrom": [
              {
                "SourceContainer": {"Ref":"AppName"}
              }
            ]
          }
        ],
        "Volumes": [
          {
            "Host": {
              "SourcePath": "/var/lib/docker/vfs/dir/"
            },
            "Name": "my-vol"
          }
        ]
      }
    },
    "service": {
      "Type": "AWS::ECS::Service",
      "Properties" : {
        "Cluster": {"Ref": "cluster"},
        "DeploymentConfiguration": {
          "MaximumPercent": 200,
          "MinimumHealthyPercent": 100
        },
        "DesiredCount": 0,
        "HealthCheckGracePeriodSeconds": {"Ref": "HealthCheckGracePeriodSeconds"},
        "LoadBalancers": [{
          "ContainerName": {"Ref" : "AppName"},
          "ContainerPort": {"Ref":"AppContainerPort"},
          "LoadBalancerName": {"Ref": "elb"}
        }],
        "PlacementStrategies": [{
          "Type" : "binpack",
          "Field": "memory"
        }, {
          "Type": "spread",
          "Field": "host"
        }],
        "PlacementConstraints": [{
          "Type": "memberOf",
          "Expression": "attribute:ecs.availability-zone != us-east-1d"
        }, {
          "Type": "distinctInstance"
        }],
        "TaskDefinition" : {"Ref":"taskdefinition"},
        "ServiceName": {"Ref": "ServiceName"},
        "Role": {"Ref": "Role"}
      }
    },
    "elb": {
      "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties": {
        "LoadBalancerName": {"Ref": "LoadBalancerName"},
        "Listeners": [{
          "InstancePort": {"Ref": "AppHostPort"},
          "LoadBalancerPort": "80",
          "Protocol": "HTTP"
        }],
        "Subnets": [{"Ref":"Subnet1"}]
      },
      "DependsOn": "GatewayAttachment"
    },
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "10.0.0.0/24"
      }
    },
    "Subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": { "Ref": "VPC" },
        "CidrBlock": "10.0.0.0/25"
      }
    },
    "InternetGateway": {
      "Type": "AWS::EC2::InternetGateway"
    },
    "GatewayAttachment": {
      "Type": "AWS::EC2::VPCGatewayAttachment",
      "Properties": {
        "InternetGatewayId": {"Ref": "InternetGateway"},
        "VpcId": {"Ref": "VPC"}
      }
    },
    "Role": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": "ecs.amazonaws.com"
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonEC2ContainerServiceRole"]
      }
    }
  },
  "Outputs" : {
    "Cluster": {
      "Value": {"Ref" : "cluster"}
    }
  }
}
```

#### YAML<a name="aws-resource-ecs-service-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Creating ECS service
Parameters:
  AppName:
    Type: String
    Description: Name of app requiring ELB exposure
    Default: simple-app
  AppContainerPort:
    Type: Number
    Description: Container port of app requiring ELB exposure
    Default: '80'
  AppHostPort:
    Type: Number
    Description: Host port of app requiring ELB exposure
    Default: '80'
  ServiceName:
    Type: String
  LoadBalancerName:
    Type: String
  HealthCheckGracePeriodSeconds:
    Type: String
Resources:
  cluster:
    Type: 'AWS::ECS::Cluster'
  taskdefinition:
    Type: 'AWS::ECS::TaskDefinition'
    Properties:
      ContainerDefinitions:
        - Name: !Ref AppName
          MountPoints:
            - SourceVolume: my-vol
              ContainerPath: /var/www/my-vol
          Image: amazon/amazon-ecs-sample
          Cpu: '10'
          PortMappings:
            - ContainerPort: !Ref AppContainerPort
              HostPort: !Ref AppHostPort
          EntryPoint:
            - /usr/sbin/apache2
            - '-D'
            - FOREGROUND
          Memory: '500'
          Essential: 'true'
        - Name: busybox
          Image: busybox
          Cpu: '10'
          EntryPoint:
            - sh
            - '-c'
          Memory: '500'
          Command:
            - >-
              /bin/sh -c "while true; do /bin/date > /var/www/my-vol/date; sleep
              1; done"
          Essential: 'false'
          VolumesFrom:
            - SourceContainer: !Ref AppName
      Volumes:
        - Host:
            SourcePath: /var/lib/docker/vfs/dir/
          Name: my-vol
  service:
    Type: 'AWS::ECS::Service'
    Properties:
      Cluster: !Ref cluster
      DeploymentConfiguration:
        MaximumPercent: 200
        MinimumHealthyPercent: 100
      DesiredCount: 0
      HealthCheckGracePeriodSeconds: !Ref HealthCheckGracePeriodSeconds
      LoadBalancers:
        - ContainerName: !Ref AppName
          ContainerPort: !Ref AppContainerPort
          LoadBalancerName: !Ref elb
      PlacementStrategies:
        - Type: binpack
          Field: memory
        - Type: spread
          Field: host
      PlacementConstraints:
        - Type: memberOf
          Expression: 'attribute:ecs.availability-zone != us-east-1d'
        - Type: distinctInstance
      TaskDefinition: !Ref taskdefinition
      ServiceName: !Ref ServiceName
      Role: !Ref Role
  elb:
    Type: 'AWS::ElasticLoadBalancing::LoadBalancer'
    Properties:
      LoadBalancerName: !Ref LoadBalancerName
      Listeners:
        - InstancePort: !Ref AppHostPort
          LoadBalancerPort: '80'
          Protocol: HTTP
      Subnets:
        - !Ref Subnet1
    DependsOn: GatewayAttachment
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/24
  Subnet1:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      CidrBlock: 10.0.0.0/25
  InternetGateway:
    Type: 'AWS::EC2::InternetGateway'
  GatewayAttachment:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      InternetGatewayId: !Ref InternetGateway
      VpcId: !Ref VPC
  Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2008-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: ecs.amazonaws.com
            Action: 'sts:AssumeRole'
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonEC2ContainerServiceRole'
Outputs:
  Cluster:
    Value: !Ref cluster
```

## More Info<a name="w3ab2c21c10d563c15"></a>
+ To use Application Auto Scaling to scale an Amazon ECS service in response to Amazon CloudWatch alarms, use the [AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md) and [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resources\.
+ To use an Application Load Balancer to distribute incoming application traffic across multiple targets, use the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md), [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md), [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md), and [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md) resources\.
+ For a complete sample template that shows how you can create an Amazon ECS cluster and service, see [Amazon Elastic Container Service Template Snippets](quickref-ecs.md)\.