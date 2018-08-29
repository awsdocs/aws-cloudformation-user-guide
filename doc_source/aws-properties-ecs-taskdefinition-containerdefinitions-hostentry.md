# Amazon Elastic Container Service TaskDefinition HostEntry<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry"></a>

`HostEntry` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that specifies the hostnames and IP address entries to add to the Amazon Elastic Container Service \(Amazon ECS\) container's `/etc/hosts` file\.

## Syntax<a name="w3ab2c21c14d872b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry-syntax.json"></a>

```
{
  "[Hostname](#cfn-ecs-taskdefinition-containerdefinition-hostentry-hostname)" : String,
  "[IpAddress](#cfn-ecs-taskdefinition-containerdefinition-hostentry-ipaddress)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry-syntax.yaml"></a>

```
[Hostname](#cfn-ecs-taskdefinition-containerdefinition-hostentry-hostname): String
[IpAddress](#cfn-ecs-taskdefinition-containerdefinition-hostentry-ipaddress): String
```

## Properties<a name="w3ab2c21c14d872b7"></a>

`Hostname`  <a name="cfn-ecs-taskdefinition-containerdefinition-hostentry-hostname"></a>
The hostname to use in the `/etc/hosts` file\.  
*Required*: Yes  
*Type*: String

`IpAddress`  <a name="cfn-ecs-taskdefinition-containerdefinition-hostentry-ipaddress"></a>
The IP address to use in the `/etc/hosts` file\.  
*Required*: Yes  
*Type*: String