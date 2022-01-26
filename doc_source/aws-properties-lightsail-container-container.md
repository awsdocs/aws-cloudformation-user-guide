# AWS::Lightsail::Container Container<a name="aws-properties-lightsail-container-container"></a>

`Container` is a property of the [ContainerServiceDeployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-container-containerservicedeployment.html) property\. It describes the settings of a container that will be launched, or that is launched, to an Amazon Lightsail container service\.

## Syntax<a name="aws-properties-lightsail-container-container-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-container-container-syntax.json"></a>

```
{
  "[Command](#cfn-lightsail-container-container-command)" : [ String, ... ],
  "[ContainerName](#cfn-lightsail-container-container-containername)" : String,
  "[Environment](#cfn-lightsail-container-container-environment)" : [ EnvironmentVariable, ... ],
  "[Image](#cfn-lightsail-container-container-image)" : String,
  "[Ports](#cfn-lightsail-container-container-ports)" : [ PortInfo, ... ]
}
```

### YAML<a name="aws-properties-lightsail-container-container-syntax.yaml"></a>

```
  [Command](#cfn-lightsail-container-container-command): 
    - String
  [ContainerName](#cfn-lightsail-container-container-containername): String
  [Environment](#cfn-lightsail-container-container-environment): 
    - EnvironmentVariable
  [Image](#cfn-lightsail-container-container-image): String
  [Ports](#cfn-lightsail-container-container-ports): 
    - PortInfo
```

## Properties<a name="aws-properties-lightsail-container-container-properties"></a>

`Command`  <a name="cfn-lightsail-container-container-command"></a>
The launch command for the container\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContainerName`  <a name="cfn-lightsail-container-container-containername"></a>
The name of the container\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Environment`  <a name="cfn-lightsail-container-container-environment"></a>
The environment variables of the container\.  
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-lightsail-container-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Image`  <a name="cfn-lightsail-container-container-image"></a>
The name of the image used for the container\.  
Container images that are sourced from \(registered and stored on\) your container service start with a colon \(`:`\)\. For example, if your container service name is `container-service-1`, the container image label is `mystaticsite`, and you want to use the third version \(`3`\) of the registered container image, then you should specify `:container-service-1.mystaticsite.3`\. To use the latest version of a container image, specify `latest` instead of a version number \(for example, `:container-service-1.mystaticsite.latest`\)\. Your container service will automatically use the highest numbered version of the registered container image\.  
Container images that are sourced from a public registry like Docker Hub don’t start with a colon\. For example, `nginx:latest` or `nginx`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ports`  <a name="cfn-lightsail-container-container-ports"></a>
An object that describes the open firewall ports and protocols of the container\.  
*Required*: No  
*Type*: List of [PortInfo](aws-properties-lightsail-container-portinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)