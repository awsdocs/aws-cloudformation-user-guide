# AWS::ECS::Service<a name="aws-resource-ecs-service"></a>

The `AWS::ECS::Service` resource creates an Amazon Elastic Container Service \(Amazon ECS\) service that runs and maintains the requested number of tasks and associated load balancers\.

## Syntax<a name="aws-resource-ecs-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-service-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::Service",
  "Properties" : {
      "[Cluster](#cfn-ecs-service-cluster)" : String,
      "[DeploymentConfiguration](#cfn-ecs-service-deploymentconfiguration)" : [DeploymentConfiguration](aws-properties-ecs-service-deploymentconfiguration.md),
      "[DesiredCount](#cfn-ecs-service-desiredcount)" : Integer,
      "[HealthCheckGracePeriodSeconds](#cfn-ecs-service-healthcheckgraceperiodseconds)" : Integer,
      "[LaunchType](#cfn-ecs-service-launchtype)" : String,
      "[LoadBalancers](#cfn-ecs-service-loadbalancers)" : [ [LoadBalancer](aws-properties-ecs-service-loadbalancers.md), ... ],
      "[NetworkConfiguration](#cfn-ecs-service-networkconfiguration)" : [NetworkConfiguration](aws-properties-ecs-service-networkconfiguration.md),
      "[PlacementConstraints](#cfn-ecs-service-placementconstraints)" : [ [PlacementConstraint](aws-properties-ecs-service-placementconstraint.md), ... ],
      "[PlacementStrategies](#cfn-ecs-service-placementstrategies)" : [ [PlacementStrategy](aws-properties-ecs-service-placementstrategy.md), ... ],
      "[PlatformVersion](#cfn-ecs-service-platformversion)" : String,
      "[Role](#cfn-ecs-service-role)" : String,
      "[SchedulingStrategy](#cfn-ecs-service-schedulingstrategy)" : String,
      "[ServiceName](#cfn-ecs-service-servicename)" : String,
      "[ServiceRegistries](#cfn-ecs-service-serviceregistries)" : [ [ServiceRegistry](aws-properties-ecs-service-serviceregistry.md), ... ],
      "[TaskDefinition](#cfn-ecs-service-taskdefinition)" : String
    }
}
```

### YAML<a name="aws-resource-ecs-service-syntax.yaml"></a>

```
Type: AWS::ECS::Service
Properties: 
  [Cluster](#cfn-ecs-service-cluster): String
  [DeploymentConfiguration](#cfn-ecs-service-deploymentconfiguration): 
    [DeploymentConfiguration](aws-properties-ecs-service-deploymentconfiguration.md)
  [DesiredCount](#cfn-ecs-service-desiredcount): Integer
  [HealthCheckGracePeriodSeconds](#cfn-ecs-service-healthcheckgraceperiodseconds): Integer
  [LaunchType](#cfn-ecs-service-launchtype): String
  [LoadBalancers](#cfn-ecs-service-loadbalancers): 
    - [LoadBalancer](aws-properties-ecs-service-loadbalancers.md)
  [NetworkConfiguration](#cfn-ecs-service-networkconfiguration): 
    [NetworkConfiguration](aws-properties-ecs-service-networkconfiguration.md)
  [PlacementConstraints](#cfn-ecs-service-placementconstraints): 
    - [PlacementConstraint](aws-properties-ecs-service-placementconstraint.md)
  [PlacementStrategies](#cfn-ecs-service-placementstrategies): 
    - [PlacementStrategy](aws-properties-ecs-service-placementstrategy.md)
  [PlatformVersion](#cfn-ecs-service-platformversion): String
  [Role](#cfn-ecs-service-role): String
  [SchedulingStrategy](#cfn-ecs-service-schedulingstrategy): String
  [ServiceName](#cfn-ecs-service-servicename): String
  [ServiceRegistries](#cfn-ecs-service-serviceregistries): 
    - [ServiceRegistry](aws-properties-ecs-service-serviceregistry.md)
  [TaskDefinition](#cfn-ecs-service-taskdefinition): String
```

## Properties<a name="aws-resource-ecs-service-properties"></a>

`Cluster`  <a name="cfn-ecs-service-cluster"></a>
The short name or full Amazon Resource Name \(ARN\) of the cluster on which to run your service\. If you do not specify a cluster, the default cluster is assumed\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentConfiguration`  <a name="cfn-ecs-service-deploymentconfiguration"></a>
Optional deployment parameters that control how many tasks run during the deployment and the ordering of stopping and starting tasks\.  
*Required*: No  
*Type*: [DeploymentConfiguration](aws-properties-ecs-service-deploymentconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredCount`  <a name="cfn-ecs-service-desiredcount"></a>
The number of instantiations of the specified task definition to place and keep running on your cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckGracePeriodSeconds`  <a name="cfn-ecs-service-healthcheckgraceperiodseconds"></a>
The period of time, in seconds, that the Amazon ECS service scheduler should ignore unhealthy Elastic Load Balancing target health checks after a task has first started\. This is only valid if your service is configured to use a load balancer\. If your service's tasks take a while to start and respond to Elastic Load Balancing health checks, you can specify a health check grace period of up to 2,147,483,647 seconds\. During that time, the ECS service scheduler ignores health check status\. This grace period can prevent the ECS service scheduler from marking tasks as unhealthy and stopping them before they have time to come up\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchType`  <a name="cfn-ecs-service-launchtype"></a>
The launch type on which to run your service\. For more information, see [Amazon ECS Launch Types](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/launch_types.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `EC2 | FARGATE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoadBalancers`  <a name="cfn-ecs-service-loadbalancers"></a>
A list of load balancer objects to associate with the cluster\. If you specify the `Role` property, `LoadBalancers` must be specified as well\. For information about the number of load balancers that you can specify per service, see [Service Load Balancing](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-load-balancing.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: List of [LoadBalancer](aws-properties-ecs-service-loadbalancers.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkConfiguration`  <a name="cfn-ecs-service-networkconfiguration"></a>
The network configuration for the service\. This parameter is required for task definitions that use the `awsvpc` network mode to receive their own elastic network interface, and it is not supported for other network modes\. For more information, see [Task Networking](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-networking.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-ecs-service-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementConstraints`  <a name="cfn-ecs-service-placementconstraints"></a>
An array of placement constraint objects to use for tasks in your service\. You can specify a maximum of 10 constraints per task \(this limit includes constraints in the task definition and those specified at runtime\)\.   
*Required*: No  
*Type*: List of [PlacementConstraint](aws-properties-ecs-service-placementconstraint.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlacementStrategies`  <a name="cfn-ecs-service-placementstrategies"></a>
The placement strategy objects to use for tasks in your service\. You can specify a maximum of five strategy rules per service\. For more information, see [Task Placement Strategies](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-strategies.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: List of [PlacementStrategy](aws-properties-ecs-service-placementstrategy.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PlatformVersion`  <a name="cfn-ecs-service-platformversion"></a>
The platform version that your tasks in the service are running on\. A platform version is specified only for tasks using the Fargate launch type\. If one isn't specified, the `LATEST` platform version is used by default\. For more information, see [AWS Fargate Platform Versions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/platform_versions.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Role`  <a name="cfn-ecs-service-role"></a>
The name or full Amazon Resource Name \(ARN\) of the IAM role that allows Amazon ECS to make calls to your load balancer on your behalf\. This parameter is only permitted if you are using a load balancer with your service and your task definition does not use the `awsvpc` network mode\. If you specify the `role` parameter, you must also specify a load balancer object with the `loadBalancers` parameter\.  
If your account has already created the Amazon ECS service\-linked role, that role is used by default for your service unless you specify a role here\. The service\-linked role is required if your task definition uses the `awsvpc` network mode, in which case you should not specify a role here\. For more information, see [Using Service\-Linked Roles for Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using-service-linked-roles.html) in the *Amazon Elastic Container Service Developer Guide*\.
If your specified role has a path other than `/`, then you must either specify the full role ARN \(this is recommended\) or prefix the role name with the path\. For example, if a role with the name `bar` has a path of `/foo/` then you would specify `/foo/bar` as the role name\. For more information, see [Friendly Names and Paths](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_identifiers.html#identifiers-friendly-names) in the *IAM User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchedulingStrategy`  <a name="cfn-ecs-service-schedulingstrategy"></a>
The scheduling strategy to use for the service\. For more information, see [Services](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs_services.html)\.  
There are two service scheduler strategies available:  
+  `REPLICA`\-The replica scheduling strategy places and maintains the desired number of tasks across your cluster\. By default, the service scheduler spreads tasks across Availability Zones\. You can use task placement strategies and constraints to customize task placement decisions\. This scheduler strategy is required if the service is using the `CODE_DEPLOY` or `EXTERNAL` deployment controller types\.
+  `DAEMON`\-The daemon scheduling strategy deploys exactly one task on each active container instance that meets all of the task placement constraints that you specify in your cluster\. When you're using this strategy, you don't need to specify a desired number of tasks, a task placement strategy, or use Service Auto Scaling policies\.
**Note**  
Tasks using the Fargate launch type or the `CODE_DEPLOY` or `EXTERNAL` deployment controller types don't support the `DAEMON` scheduling strategy\.
*Required*: No  
*Type*: String  
*Allowed Values*: `DAEMON | REPLICA`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceName`  <a name="cfn-ecs-service-servicename"></a>
The name of your service\. Up to 255 letters \(uppercase and lowercase\), numbers, and hyphens are allowed\. Service names must be unique within a cluster, but you can have similarly named services in multiple clusters within a Region or across multiple Regions\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceRegistries`  <a name="cfn-ecs-service-serviceregistries"></a>
The details of the service discovery registries to assign to this service\. For more information, see [Service Discovery](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-discovery.html)\.  
Service discovery is supported for Fargate tasks if you are using platform version v1\.1\.0 or later\. For more information, see [AWS Fargate Platform Versions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/platform_versions.html)\.
*Required*: No  
*Type*: List of [ServiceRegistry](aws-properties-ecs-service-serviceregistry.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TaskDefinition`  <a name="cfn-ecs-service-taskdefinition"></a>
The `family` and `revision` \(`family:revision`\) or full ARN of the task definition to run in your service\. If a `revision` is not specified, the latest `ACTIVE` revision is used\.  
A task definition must be specified if the service is using the `ECS` deployment controller\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ecs-service-return-values"></a>

### Ref<a name="aws-resource-ecs-service-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\)\.

In the following example, the `Ref` function returns the ARN of the `MyECSService` service, such as `arn:aws:ecs:us-west-2:123456789012:service/sample-webapp`\.

 `{ "Ref": "MyECSService" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecs-service-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecs-service-return-values-fn--getatt-fn--getatt"></a>

`Name`  <a name="Name-fn::getatt"></a>
The name of the Amazon ECS service, such as `sample-webapp`\.

## Examples<a name="aws-resource-ecs-service--examples"></a>

### Define a Basic Amazon ECS Service<a name="aws-resource-ecs-service--examples--Define_a_Basic_Amazon_ECS_Service"></a>

The following example defines an Amazon ECS service that uses a cluster and task definition that are declared elsewhere in the same template\.

#### JSON<a name="aws-resource-ecs-service--examples--Define_a_Basic_Amazon_ECS_Service--json"></a>

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

#### YAML<a name="aws-resource-ecs-service--examples--Define_a_Basic_Amazon_ECS_Service--yaml"></a>

```
WebApp: 
  Type: AWS::ECS::Service
  Properties: 
    Cluster: 
      Ref: "cluster"
    DesiredCount: 
      Ref: "desiredcount"
    TaskDefinition: 
      Ref: "taskdefinition"
```

### Associate an Application Load Balancer with a Service<a name="aws-resource-ecs-service--examples--Associate_an_Application_Load_Balancer_with_a_Service"></a>

The following example associates an Application Load Balancer with an Amazon ECS service by referencing an `AWS::ElasticLoadBalancingV2::TargetGroup` resource\.

**Note**  
The Amazon ECS service requires an explicit dependency on the Application Load Balancer listener rule and the Application Load Balancer listener\. This prevents the service from starting before the listener is ready\.

#### JSON<a name="aws-resource-ecs-service--examples--Associate_an_Application_Load_Balancer_with_a_Service--json"></a>

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

#### YAML<a name="aws-resource-ecs-service--examples--Associate_an_Application_Load_Balancer_with_a_Service--yaml"></a>

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

### Define a Service with a Health Check Grace Period<a name="aws-resource-ecs-service--examples--Define_a_Service_with_a_Health_Check_Grace_Period"></a>

The following example defines a service with a parameter that enables users to specify how many seconds that the Amazon ECS service scheduler should ignore unhealthy Elastic Load Balancing target health checks after a task has first started\.

#### JSON<a name="aws-resource-ecs-service--examples--Define_a_Service_with_a_Health_Check_Grace_Period--json"></a>

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

#### YAML<a name="aws-resource-ecs-service--examples--Define_a_Service_with_a_Health_Check_Grace_Period--yaml"></a>

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
    Type: AWS::ECS::Cluster
  taskdefinition:
    Type: AWS::ECS::TaskDefinition
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
    Type: AWS::ECS::Service
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
    Type: AWS::ElasticLoadBalancing::LoadBalancer
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
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/24
  Subnet1:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId: !Ref VPC
      CidrBlock: 10.0.0.0/25
  InternetGateway:
    Type: AWS::EC2::InternetGateway
  GatewayAttachment:
    Type: AWS::EC2::VPCGatewayAttachment
    Properties:
      InternetGatewayId: !Ref InternetGateway
      VpcId: !Ref VPC
  Role:
    Type: AWS::IAM::Role
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