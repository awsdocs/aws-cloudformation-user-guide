# Amazon Elastic Container Service Service LoadBalancers<a name="aws-properties-ecs-service-loadbalancers"></a>

`LoadBalancers` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the load balancer to associate with an Amazon Elastic Container Service \(Amazon ECS\) service\.

## Syntax<a name="w3ab2c21c14d677b5"></a>

### JSON<a name="aws-properties-ecs-service-loadbalancers-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-containername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-containerport)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-loadbalancername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-targetgrouparn)" : String
}
```

### YAML<a name="aws-properties-ecs-service-loadbalancers-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-containername): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-containerport): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-loadbalancername): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-loadbalancers-targetgrouparn): String
```

## Properties<a name="w3ab2c21c14d677b7"></a>

`ContainerName`  
The name of a container to use with the load balancer\.  
*Required: *Yes  
*Type*: String

`ContainerPort`  
The port number on the container to direct load balancer traffic to\. Your container instances must allow ingress traffic on this port\.  
*Required: *Yes  
*Type*: Integer

`LoadBalancerName`  
The name of a Classic Load Balancer to associate with the Amazon ECS service\.  
*Required: *No  
*Type*: String

`TargetGroupArn`  
An Application load balancer target group Amazon Resource Name \(ARN\) to associate with the Amazon ECS service\.  
*Required: *No  
*Type*: String