# AWS::ECS::Service ServiceConnectService<a name="aws-properties-ecs-service-serviceconnectservice"></a>

The Service Connect service object configuration\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-serviceconnectservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-serviceconnectservice-syntax.json"></a>

```
{
  "[ClientAliases](#cfn-ecs-service-serviceconnectservice-clientaliases)" : [ ServiceConnectClientAlias, ... ],
  "[DiscoveryName](#cfn-ecs-service-serviceconnectservice-discoveryname)" : String,
  "[IngressPortOverride](#cfn-ecs-service-serviceconnectservice-ingressportoverride)" : Integer,
  "[PortName](#cfn-ecs-service-serviceconnectservice-portname)" : String
}
```

### YAML<a name="aws-properties-ecs-service-serviceconnectservice-syntax.yaml"></a>

```
  [ClientAliases](#cfn-ecs-service-serviceconnectservice-clientaliases): 
    - ServiceConnectClientAlias
  [DiscoveryName](#cfn-ecs-service-serviceconnectservice-discoveryname): String
  [IngressPortOverride](#cfn-ecs-service-serviceconnectservice-ingressportoverride): Integer
  [PortName](#cfn-ecs-service-serviceconnectservice-portname): String
```

## Properties<a name="aws-properties-ecs-service-serviceconnectservice-properties"></a>

`ClientAliases`  <a name="cfn-ecs-service-serviceconnectservice-clientaliases"></a>
The list of client aliases for this Service Connect service\. You use these to assign names that can be used by client applications\. The maximum number of client aliases that you can have in this list is 1\.  
Each alias \("endpoint"\) is a fully\-qualified name and port number that other Amazon ECS tasks \("clients"\) can use to connect to this service\.  
Each name and port mapping must be unique within the namespace\.  
For each `ServiceConnectService`, you must provide at least one `clientAlias` with one `port`\.  
*Required*: No  
*Type*: List of [ServiceConnectClientAlias](aws-properties-ecs-service-serviceconnectclientalias.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DiscoveryName`  <a name="cfn-ecs-service-serviceconnectservice-discoveryname"></a>
The `discoveryName` is the name of the new AWS Cloud Map service that Amazon ECS creates for this Amazon ECS service\. This must be unique within the AWS Cloud Map namespace\. The name can contain up to 64 characters\. The name can include lowercase letters, numbers, underscores \(\_\), and hyphens \(\-\)\. The name can't start with a hyphen\.  
If this parameter isn't specified, the default value of `discoveryName.namespace` is used\. If the `discoveryName` isn't specified, the port mapping name from the task definition is used in `portName.namespace`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressPortOverride`  <a name="cfn-ecs-service-serviceconnectservice-ingressportoverride"></a>
The port number for the Service Connect proxy to listen on\.  
Use the value of this field to bypass the proxy for traffic on the port number specified in the named `portMapping` in the task definition of this application, and then use it in your VPC security groups to allow traffic into the proxy for this Amazon ECS service\.  
In `awsvpc` mode and Fargate, the default value is the container port number\. The container port number is in the `portMapping` in the task definition\. In bridge mode, the default value is the ephemeral port of the Service Connect proxy\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortName`  <a name="cfn-ecs-service-serviceconnectservice-portname"></a>
The `portName` must match the name of one of the `portMappings` from all the containers in the task definition of this Amazon ECS service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)