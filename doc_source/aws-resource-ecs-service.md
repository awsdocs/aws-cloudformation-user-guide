# AWS::ECS::Service<a name="aws-resource-ecs-service"></a>

The `AWS::ECS::Service` resource creates an Amazon Elastic Container Service \(Amazon ECS\) service that runs and maintains the requested number of tasks and associated load balancers\.


+ [Syntax](#aws-resource-ecs-service-syntax)
+ [Properties](#w3ab2c21c10d522b9)
+ [Return Values](#w3ab2c21c10d522c11)
+ [Examples](#w3ab2c21c10d522c13)
+ [More Info](#w3ab2c21c10d522c15)

## Syntax<a name="aws-resource-ecs-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-service-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::Service",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-cluster)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-deploymentconfiguration)" : DeploymentConfiguration,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-desiredcount)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-launchtype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers)" : [ Load Balancer Objects, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-networkconfiguration)" : NetworkConfiguration,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-placementconstraints)" : [ PlacementConstraints, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-role)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-placementstrategies)" : [ PlacementStrategies, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-platformversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-servicename)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-taskdefinition)" : String
  }
}
```

### YAML<a name="aws-resource-ecs-service-syntax.yaml"></a>

```
Type: "AWS::ECS::Service"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-cluster): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-deploymentconfiguration):
    DeploymentConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-desiredcount): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-launchtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers):
    - Load Balancer Objects, ...
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-networkconfiguration): 
    NetworkConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-placementconstraints): 
   - PlacementConstraints, ...
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-placementstrategies): 
   - PlacementStrategies, ...
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-platformversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-role): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-servicename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-taskdefinition): String
```

## Properties<a name="w3ab2c21c10d522b9"></a>

For more information on properties and valid parameters, see [CreateService](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_CreateService.html)in the *Amazon Elastic Container Service API Reference*\.

**Note**  
When you use Auto Scaling or Amazon Elastic Compute Cloud \(Amazon EC2\) to create container instances for an Amazon ECS cluster, the Amazon ECS service resource must have a dependency on the Auto Scaling group or the Amazon EC2 instances\. This makes the container instances available and associates them with the Amazon ECS cluster before AWS CloudFormation creates the Amazon ECS service\.

`Cluster`  
The name or Amazon Resource Name \(ARN\) of the cluster that you want to run your Amazon ECS service on\. If you do not specify a cluster, Amazon ECS uses the default cluster\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`DeploymentConfiguration`  
Configures how many tasks run during a deployment\.  
*Required: *No  
*Type*: [Amazon Elastic Container Service Service DeploymentConfiguration](aws-properties-ecs-service-deploymentconfiguration.md)  
*Update requires*: No interruption

`DesiredCount`  
The number of simultaneous tasks that you want to run on the cluster\. Specify the tasks with the `TaskDefinition` property\.  
*Required: *Conditional\. Required only when creating an Amazon ECS Service\.  
*Type*: Integer  
*Update requires*: No interruption

`LaunchType`  
The launch type on which to run your service\. If one is not specified, `EC2` will be used by default\. Valid values include `EC2` and `FARGATE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`LoadBalancers`  
A list of load balancer objects to associate with the cluster\. If you specify the `Role` property, `LoadBalancers` must be specified as well\. For information about the number of load balancers that you can specify per service, see [Service Load Balancing](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-load-balancing.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required: *Conditional  
*Type*: List of [Amazon Elastic Container Service Service LoadBalancers](aws-properties-ecs-service-loadbalancers.md)  
*Update requires*: Replacement

`NetworkConfiguration`  
The network configuration for the service\. This parameter is required for task definitions that use the `awsvpc` network mode to receive their own Elastic Network Interface, and it is not supported for other network modes\. For more information, see [Task Networking](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/developerguidetask-networking.html) in the *Amazon Elastic Container Service Developer Guide*\.  
 *Required*: No  
 *Type*: [Amazon ECS Service NetworkConfiguration](aws-properties-ecs-service-networkconfiguration.md)  
 *Update requires*: No interruption 

`PlacementConstraints`  
The placement constraints for the tasks in the service\.  
*Required: *No  
*Type*: [Amazon Elastic Container Service Service PlacementConstraint](aws-properties-ecs-service-placementconstraints-placementconstraint.md)  
*Update requires*: Replacement

`PlacementStrategies`  
The placement strategies that determine how tasks for the service are placed\.  
*Required: *No  
*Type*: [Amazon Elastic Container Service Service PlacementStrategies](aws-properties-ecs-service-placementstrategies-placementstrategy.md)  
*Update requires*: Replacement

`PlatformVersion`  
The platform version on which to run your service\. If one is not specified, the latest version will be used by default\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`Role`  
The name or ARN of an AWS Identity and Access Management \(IAM\) role that allows your Amazon ECS container agent to make calls to your load balancer\.  
In some cases, you might need to add a dependency on the service role's policy\. For more information, see IAM role policy in [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required: *Conditional\. Required only if you specify the `LoadBalancers` property\.  
*Type*: String  
*Update requires*: Replacement

`ServiceName`  
The name of your service\. The name is limited to 255 letters \(uppercase and lowercase\), numbers, hyphens, and underscores\. Service names must be unique within a cluster, but you can have similarly named services in multiple clusters within a region or across multiple regions\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`TaskDefinition`  
The ARN of the task definition \(including the revision number\) that you want to run on the cluster, such as `arn:aws:ecs:us-east-1:123456789012:task-definition/mytask:3`\. You can't use `:latest` to specify a revision because it's ambiguous\. For example, if AWS CloudFormation needed to roll back an update, it wouldn't know which revision to roll back to\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Some interruptions

## Return Values<a name="w3ab2c21c10d522c11"></a>

### Ref<a name="w3ab2c21c10d522c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN\.

In the following sample, the `Ref` function returns the ARN of the `MyECSService` service, such as `arn:aws:ecs:us-west-2:123456789012:service/sample-webapp`\.

```
{ "Ref": "MyECSService" }
```

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d522c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
The name of the Amazon ECS service, such as `sample-webapp`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="w3ab2c21c10d522c13"></a>

### Define a Basic Amazon ECS Service<a name="w3ab2c21c10d522c13b2"></a>

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

### Associate an Application Load Balancer with a Service<a name="w3ab2c21c10d522c13b4"></a>

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

## More Info<a name="w3ab2c21c10d522c15"></a>

+ To use Application Auto Scaling to scale an Amazon ECS service in response to Amazon CloudWatch alarms, use the [AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md) and [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) resources\.

+ To use an Application Load Balancer to distribute incoming application traffic across multiple targets, use the [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md), [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md), [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md), and [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md) resources\.

+ For a complete sample template that shows how you can create an Amazon ECS cluster and service, see [Amazon Elastic Container Service Template Snippets](quickref-ecs.md)\.