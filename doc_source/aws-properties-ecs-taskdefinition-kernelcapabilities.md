# Amazon Elastic Container Service TaskDefinition KernelCapabilities<a name="aws-properties-ecs-taskdefinition-kernelcapabilities"></a>

<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-description"></a>The `KernelCapabilities` property type specifies the Linux capabilities to add or drop from the default Docker configuration in an Amazon Elastic Container Service \(Amazon ECS\) container\. For more information, see [ KernelCapabilities](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_KernelCapabilities.html) in the *Amazon Elastic Container Service API Reference*\.

<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-inheritance"></a> `KernelCapabilities` is a property of the [Amazon ECS TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax.json"></a>

```
{
  "[Add](#cfn-ecs-taskdefinition-kernelcapabilities-add)" : [ String, ... ],
  "[Drop](#cfn-ecs-taskdefinition-kernelcapabilities-drop)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax.yaml"></a>

```
[Add](#cfn-ecs-taskdefinition-kernelcapabilities-add): 
  - String
[Drop](#cfn-ecs-taskdefinition-kernelcapabilities-drop): 
  - String
```

## Properties<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-properties"></a>

`Add`  <a name="cfn-ecs-taskdefinition-kernelcapabilities-add"></a>
The Linux capabilities to add to the default Docker configuration\. This maps to `CapAdd` in the [ Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.27/#create-a-container) section of the *Docker Remote API* and the `--cap-add` option to [docker run](https://docs.docker.com/engine/reference/run/)\. For valid values, see [ KernelCapabilities](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_KernelCapabilities.html) in the *Amazon Elastic Container Service API Reference*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Drop`  <a name="cfn-ecs-taskdefinition-kernelcapabilities-drop"></a>
The Linux capabilities to remove from the default Docker configuration\. This maps to `CapDrop` in the [ Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.27/#create-a-container) section of the *Docker Remote API* and the `--cap-drop` option to [docker run](https://docs.docker.com/engine/reference/run/)\. For valid values, see [ KernelCapabilities](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_KernelCapabilities.html) in the *Amazon Elastic Container Service API Reference*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 