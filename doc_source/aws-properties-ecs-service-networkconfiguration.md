# Amazon Elastic Container Service Service NetworkConfiguration<a name="aws-properties-ecs-service-networkconfiguration"></a>

`NetworkConfiguration` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the network configuration for an Amazon Elastic Container Service \(Amazon ECS\) task or service\.

## Syntax<a name="w3ab2c21c14d841b5"></a>

### JSON<a name="aws-properties-ecs-service-networkconfiguration-syntax.json"></a>

```
{
  "[AwsvpcConfiguration](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration)" : [*AwsVpcConfiguration*](aws-properties-ecs-service-awsvpcconfiguration.md)
}
```

### YAML<a name="aws-properties-ecs-service-networkconfiguration-syntax.yaml"></a>

```
[AwsvpcConfiguration](#cfn-ecs-service-networkconfiguration-awsvpcconfiguration): [*AwsVpcConfiguration*](aws-properties-ecs-service-awsvpcconfiguration.md)
```

## Properties<a name="w3ab2c21c14d841b7"></a>

`AwsvpcConfiguration`  <a name="cfn-ecs-service-networkconfiguration-awsvpcconfiguration"></a>
 The VPC subnets and security groups associated with a task\.  
*Required*: No  
*Type*: [Amazon Elastic Container Service Service AwsVpcConfiguration](aws-properties-ecs-service-awsvpcconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)