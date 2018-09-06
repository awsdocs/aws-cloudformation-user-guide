# Amazon Elastic Container Service Service ServiceRegistry<a name="aws-properties-ecs-service-serviceregistry"></a>

<a name="aws-properties-ecs-service-serviceregistry-description"></a>The `ServiceRegistry` property type specifies details of the service registry\.

<a name="aws-properties-ec2-launchtemplate-instancemarketoptions-inheritance"></a> `ServiceRegistry` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource\.

## Syntax<a name="w3ab2c21c14d857b7"></a>

### JSON<a name="aws-properties-ecs-service-serviceregistry-syntax.json"></a>

```
{
  "[Port](#cfn-ecs-service-serviceregistry-port)" : Integer,
  "[RegistryArn](#cfn-ecs-service-serviceregistry-registryarn)" : String
}
```

### YAML<a name="aws-properties-ecs-service-serviceregistry-syntax.yaml"></a>

```
[Port](#cfn-ecs-service-serviceregistry-port): Integer
[RegistryArn](#cfn-ecs-service-serviceregistry-registryarn): String
```

## Properties<a name="w3ab2c21c14d857b9"></a>

`Port`  <a name="cfn-ecs-service-serviceregistry-port"></a>
The port value used if your service discovery service specified an SRV record\.  
*Required*: No  
*Type*: Integer

`RegistryArn`  <a name="cfn-ecs-service-serviceregistry-registryarn"></a>
The Amazon Resource Name \(ARN\) of the service registry\. The currently supported service registry is Amazon Route 53 auto naming\.   
*Required*: No  
*Type*: String

## See Also<a name="aws-properties-ecs-service-serviceregistry-seealso"></a>
+ [ServiceRegistry](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ServiceRegistry.html) in the *Amazon Elastic Container Service API Reference*