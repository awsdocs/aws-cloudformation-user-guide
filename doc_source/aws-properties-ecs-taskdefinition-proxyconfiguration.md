# Amazon ECS TaskDefinition ProxyConfiguration<a name="aws-properties-ecs-taskdefinition-proxyconfiguration"></a>

<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-description"></a>The `ProxyConfiguration` property type specifies the configuration details for the App Mesh proxy\.

For tasks using the EC2 launch type, the container instances require at least version 1\.26\.0 of the container agent and at least version 1\.26\.0\-1 of the ecs\-init package to enable a proxy configuration\. If your container instances are launched from the Amazon ECS\-optimized AMI version 20190301 or later, then they contain the required versions of the container agent and ecs\-init\. For more information, see [Amazon ECS\-optimized Linux AMI](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.

This parameter is available for tasks using the Fargate launch type in the Ohio \(us\-east\-2\) region only and the task or service requires platform version 1\.3\.0 or later\.

<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-inheritance"></a> `ProxyConfiguration` is a property of the [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md) resource type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-syntax.json"></a>

```
{
  "[ProxyConfigurationProperties](#cfn-ecs-taskdefinition-proxyconfiguration-proxyconfigurationproperties)" : String,
  "[Type](#cfn-ecs-taskdefinition-proxyconfiguration-type)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-syntax.yaml"></a>

```
[ProxyConfigurationProperties](#cfn-ecs-taskdefinition-proxyconfiguration-proxyconfigurationproperties): String
[Type](#cfn-ecs-taskdefinition-proxyconfiguration-type): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-proxyconfiguration-properties"></a>

`ProxyConfigurationProperties`  <a name="cfn-ecs-taskdefinition-proxyconfiguration-proxyconfigurationproperties"></a>
The set of network configuration parameters to provide the Container Network Interface \(CNI\) plugin, specified as key\-value pairs\. For a listing of these properties, see [ProxyConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ProxyConfiguration.html) in the *Amazon Elastic Container Service API Reference*\.  
Duplicates are not allowed\.  
 *Required*: No  
 *Type*: List of key\-pair values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Type`  <a name="cfn-ecs-taskdefinition-proxyconfiguration-type"></a>
The proxy type\. The only supported value is `APPMESH`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 