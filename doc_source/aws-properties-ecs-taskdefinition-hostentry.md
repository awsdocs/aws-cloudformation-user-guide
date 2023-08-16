# AWS::ECS::TaskDefinition HostEntry<a name="aws-properties-ecs-taskdefinition-hostentry"></a>

The `HostEntry` property specifies a hostname and an IP address that are added to the `/etc/hosts` file of a container through the `extraHosts` parameter of its `ContainerDefinition` resource\.

## Syntax<a name="aws-properties-ecs-taskdefinition-hostentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-hostentry-syntax.json"></a>

```
{
  "[Hostname](#cfn-ecs-taskdefinition-hostentry-hostname)" : String,
  "[IpAddress](#cfn-ecs-taskdefinition-hostentry-ipaddress)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-hostentry-syntax.yaml"></a>

```
  [Hostname](#cfn-ecs-taskdefinition-hostentry-hostname): String
  [IpAddress](#cfn-ecs-taskdefinition-hostentry-ipaddress): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-hostentry-properties"></a>

`Hostname`  <a name="cfn-ecs-taskdefinition-hostentry-hostname"></a>
The hostname to use in the `/etc/hosts` entry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddress`  <a name="cfn-ecs-taskdefinition-hostentry-ipaddress"></a>
The IP address to use in the `/etc/hosts` entry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)