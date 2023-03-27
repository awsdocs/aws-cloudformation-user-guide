# AWS::ECS::Service ServiceConnectConfiguration<a name="aws-properties-ecs-service-serviceconnectconfiguration"></a>

The Service Connect configuration of your Amazon ECS service\. The configuration for this service to discover and connect to services, and be discovered by, and connected from, other services within a namespace\.

Tasks that run in a namespace can use short names to connect to services in the namespace\. Tasks can connect to services across all of the clusters in the namespace\. Tasks connect through a managed proxy container that collects logs and metrics for increased visibility\. Only the tasks that Amazon ECS services create are supported with Service Connect\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-serviceconnectconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-serviceconnectconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-ecs-service-serviceconnectconfiguration-enabled)" : Boolean,
  "[LogConfiguration](#cfn-ecs-service-serviceconnectconfiguration-logconfiguration)" : LogConfiguration,
  "[Namespace](#cfn-ecs-service-serviceconnectconfiguration-namespace)" : String,
  "[Services](#cfn-ecs-service-serviceconnectconfiguration-services)" : [ ServiceConnectService, ... ]
}
```

### YAML<a name="aws-properties-ecs-service-serviceconnectconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-ecs-service-serviceconnectconfiguration-enabled): Boolean
  [LogConfiguration](#cfn-ecs-service-serviceconnectconfiguration-logconfiguration): 
    LogConfiguration
  [Namespace](#cfn-ecs-service-serviceconnectconfiguration-namespace): String
  [Services](#cfn-ecs-service-serviceconnectconfiguration-services): 
    - ServiceConnectService
```

## Properties<a name="aws-properties-ecs-service-serviceconnectconfiguration-properties"></a>

`Enabled`  <a name="cfn-ecs-service-serviceconnectconfiguration-enabled"></a>
Specifies whether to use Service Connect with this service\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfiguration`  <a name="cfn-ecs-service-serviceconnectconfiguration-logconfiguration"></a>
Property description not available\.  
*Required*: No  
*Type*: [LogConfiguration](aws-properties-ecs-service-logconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-ecs-service-serviceconnectconfiguration-namespace"></a>
The namespace name or full Amazon Resource Name \(ARN\) of the AWS Cloud Map namespace for use with Service Connect\. The namespace must be in the same AWS Region as the Amazon ECS service and cluster\. The type of namespace doesn't affect Service Connect\. For more information about AWS Cloud Map, see [Working with Services](https://docs.aws.amazon.com/) in the * AWS Cloud Map Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Services`  <a name="cfn-ecs-service-serviceconnectconfiguration-services"></a>
The list of Service Connect service objects\. These are names and aliases \(also known as endpoints\) that are used by other Amazon ECS services to connect to this service\.   
This field is not required for a "client" Amazon ECS service that's a member of a namespace only to connect to other services within the namespace\. An example of this would be a frontend application that accepts incoming requests from either a load balancer that's attached to the service or by other means\.  
An object selects a port from the task definition, assigns a name for the AWS Cloud Map service, and a list of aliases \(endpoints\) and ports for client applications to refer to this service\.  
*Required*: No  
*Type*: List of [ServiceConnectService](aws-properties-ecs-service-serviceconnectservice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)