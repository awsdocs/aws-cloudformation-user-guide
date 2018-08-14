# Amazon Elastic Container Service Service LoadBalancers<a name="aws-properties-ecs-service-loadbalancers"></a>

`LoadBalancers` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the load balancer to associate with an Amazon Elastic Container Service \(Amazon ECS\) service\.

## Syntax<a name="w3ab2c21c14d853b5"></a>

### JSON<a name="aws-properties-ecs-service-loadbalancers-syntax.json"></a>

```
{
  "[ContainerName](#cfn-ecs-service-loadbalancers-containername)" : String,
  "[ContainerPort](#cfn-ecs-service-loadbalancers-containerport)" : Integer,
  "[LoadBalancerName](#cfn-ecs-service-loadbalancers-loadbalancername)" : String,
  "[TargetGroupArn](#cfn-ecs-service-loadbalancers-targetgrouparn)" : String
}
```

### YAML<a name="aws-properties-ecs-service-loadbalancers-syntax.yaml"></a>

```
[ContainerName](#cfn-ecs-service-loadbalancers-containername): String
[ContainerPort](#cfn-ecs-service-loadbalancers-containerport): Integer
[LoadBalancerName](#cfn-ecs-service-loadbalancers-loadbalancername): String
[TargetGroupArn](#cfn-ecs-service-loadbalancers-targetgrouparn): String
```

## Properties<a name="w3ab2c21c14d853b7"></a>

`ContainerName`  <a name="cfn-ecs-service-loadbalancers-containername"></a>
The name of a container to use with the load balancer\.  
*Required*: Yes  
*Type*: String

`ContainerPort`  <a name="cfn-ecs-service-loadbalancers-containerport"></a>
The port number on the container to direct load balancer traffic to\. Your container instances must allow ingress traffic on this port\.  
*Required*: Yes  
*Type*: Integer

`LoadBalancerName`  <a name="cfn-ecs-service-loadbalancers-loadbalancername"></a>
The name of a Classic Load Balancer to associate with the Amazon ECS service\.  
*Required*: No  
*Type*: String

`TargetGroupArn`  <a name="cfn-ecs-service-loadbalancers-targetgrouparn"></a>
An Application load balancer target group Amazon Resource Name \(ARN\) to associate with the Amazon ECS service\.  
*Required*: No  
*Type*: String