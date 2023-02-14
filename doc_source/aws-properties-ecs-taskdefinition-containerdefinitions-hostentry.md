# AWS::ECS::TaskDefinition HostEntry<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry"></a>

The `HostEntry` property specifies a hostname and an IP address that are added to the `/etc/hosts` file of a container through the `extraHosts` parameter of its `ContainerDefinition` resource\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-hostentry-properties"></a>

`Hostname`  <a name="cfn-ecs-taskdefinition-containerdefinition-hostentry-hostname"></a>
The hostname to use in the `/etc/hosts` entry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddress`  <a name="cfn-ecs-taskdefinition-containerdefinition-hostentry-ipaddress"></a>
The IP address to use in the `/etc/hosts` entry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)