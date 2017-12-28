# Amazon Elastic Container Service Service AwsVpcConfiguration<a name="aws-properties-ecs-service-awsvpcconfiguration"></a>

`AwsVpcConfiguration` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the subnets and security groups for an Amazon Elastic Container Service \(Amazon ECS\) task or service\.

## Syntax<a name="w3ab2c21c14d652b5"></a>

### JSON<a name="aws-properties-ecs-service-awsvpcconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-assignpublicip)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-securitygroups)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-service-awsvpcconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-assignpublicip): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-securitygroups): 
   - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-service-awsvpcconfiguration-subnets): 
   - String
```

## Properties<a name="w3ab2c21c14d652b7"></a>

`AssignPublicIp`  
Valid values include `ENABLED` and `DISABLED`\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SecurityGroups`  
The security groups associated with the task or service\. If you do not specify a security group, the default security group for the VPC is used\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`Subnets`  
The subnets associated with the Amazon ECS task or service\.  
*Required: *Yes  
*Type*: List of String values  
*Update requires*: No interruption