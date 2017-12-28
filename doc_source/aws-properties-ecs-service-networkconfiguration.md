# Amazon Elastic Container Service Service NetworkConfiguration<a name="aws-properties-ecs-service-networkconfiguration"></a>

`NetworkConfiguration` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the network configuration for an Amazon Elastic Container Service \(Amazon ECS\) task or service\.

## Syntax<a name="w3ab2c21c14d665b5"></a>

### JSON<a name="aws-properties-ecs-service-networkconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration)" : AwsVpcConfiguration
}
```

### YAML<a name="aws-properties-ecs-service-networkconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration): AwsVpcConfiguration
```

## Properties<a name="w3ab2c21c14d665b7"></a>

`AwsvpcConfiguration`  
 The VPC subnets and security groups associated with a task\.  
*Required: *No  
*Type*: [Amazon Elastic Container Service Service AwsVpcConfiguration](aws-properties-ecs-service-awsvpcconfiguration.md)  
*Update requires*: No interruption