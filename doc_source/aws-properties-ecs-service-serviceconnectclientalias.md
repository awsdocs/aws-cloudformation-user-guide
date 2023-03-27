# AWS::ECS::Service ServiceConnectClientAlias<a name="aws-properties-ecs-service-serviceconnectclientalias"></a>

Each alias \("endpoint"\) is a fully\-qualified name and port number that other tasks \("clients"\) can use to connect to this service\.

Each name and port mapping must be unique within the namespace\.

Tasks that run in a namespace can use short names to connect to services in the namespace\. Tasks can connect to services across all of the clusters in the namespace\. Tasks connect through a managed proxy container that collects logs and metrics for increased visibility\. Only the tasks that Amazon ECS services create are supported with Service Connect\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-serviceconnectclientalias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-serviceconnectclientalias-syntax.json"></a>

```
{
  "[DnsName](#cfn-ecs-service-serviceconnectclientalias-dnsname)" : String,
  "[Port](#cfn-ecs-service-serviceconnectclientalias-port)" : Integer
}
```

### YAML<a name="aws-properties-ecs-service-serviceconnectclientalias-syntax.yaml"></a>

```
  [DnsName](#cfn-ecs-service-serviceconnectclientalias-dnsname): String
  [Port](#cfn-ecs-service-serviceconnectclientalias-port): Integer
```

## Properties<a name="aws-properties-ecs-service-serviceconnectclientalias-properties"></a>

`DnsName`  <a name="cfn-ecs-service-serviceconnectclientalias-dnsname"></a>
The `dnsName` is the name that you use in the applications of client tasks to connect to this service\. The name must be a valid DNS name but doesn't need to be fully\-qualified\. The name can include up to 127 characters\. The name can include lowercase letters, numbers, underscores \(\_\), hyphens \(\-\), and periods \(\.\)\. The name can't start with a hyphen\.  
If this parameter isn't specified, the default value of `discoveryName.namespace` is used\. If the `discoveryName` isn't specified, the port mapping name from the task definition is used in `portName.namespace`\.  
To avoid changing your applications in client Amazon ECS services, set this to the same name that the client application uses by default\. For example, a few common names are `database`, `db`, or the lowercase name of a database, such as `mysql` or `redis`\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-ecs-service-serviceconnectclientalias-port"></a>
The listening port number for the Service Connect proxy\. This port is available inside of all of the tasks within the same namespace\.  
To avoid changing your applications in client Amazon ECS services, set this to the same port that the client application uses by default\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)