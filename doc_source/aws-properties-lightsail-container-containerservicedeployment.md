# AWS::Lightsail::Container ContainerServiceDeployment<a name="aws-properties-lightsail-container-containerservicedeployment"></a>

`ContainerServiceDeployment` is a property of the [AWS::Lightsail::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-container.html) resource\. It describes a container deployment configuration of a container service\.

A deployment specifies the settings, such as the ports and launch command, of containers that are deployed to your container service\.

## Syntax<a name="aws-properties-lightsail-container-containerservicedeployment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-container-containerservicedeployment-syntax.json"></a>

```
{
  "[Containers](#cfn-lightsail-container-containerservicedeployment-containers)" : [ Container, ... ],
  "[PublicEndpoint](#cfn-lightsail-container-containerservicedeployment-publicendpoint)" : PublicEndpoint
}
```

### YAML<a name="aws-properties-lightsail-container-containerservicedeployment-syntax.yaml"></a>

```
  [Containers](#cfn-lightsail-container-containerservicedeployment-containers): 
    - Container
  [PublicEndpoint](#cfn-lightsail-container-containerservicedeployment-publicendpoint): 
    PublicEndpoint
```

## Properties<a name="aws-properties-lightsail-container-containerservicedeployment-properties"></a>

`Containers`  <a name="cfn-lightsail-container-containerservicedeployment-containers"></a>
An object that describes the configuration for the containers of the deployment\.  
*Required*: No  
*Type*: List of [Container](aws-properties-lightsail-container-container.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicEndpoint`  <a name="cfn-lightsail-container-containerservicedeployment-publicendpoint"></a>
An object that describes the endpoint of the deployment\.  
*Required*: No  
*Type*: [PublicEndpoint](aws-properties-lightsail-container-publicendpoint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)