# AWS::ECS::Cluster ServiceConnectDefaults<a name="aws-properties-ecs-cluster-serviceconnectdefaults"></a>

Use this parameter to set a default Service Connect namespace\. After you set a default Service Connect namespace, any new services with Service Connect turned on that are created in the cluster are added as client services in the namespace\. This setting only applies to new services that set the `enabled` parameter to `true` in the `ServiceConnectConfiguration`\. You can set the namespace of each service individually in the `ServiceConnectConfiguration` to override this default parameter\.

Tasks that run in a namespace can use short names to connect to services in the namespace\. Tasks can connect to services across all of the clusters in the namespace\. Tasks connect through a managed proxy container that collects logs and metrics for increased visibility\. Only the tasks that Amazon ECS services create are supported with Service Connect\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-cluster-serviceconnectdefaults-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-cluster-serviceconnectdefaults-syntax.json"></a>

```
{
  "[Namespace](#cfn-ecs-cluster-serviceconnectdefaults-namespace)" : String
}
```

### YAML<a name="aws-properties-ecs-cluster-serviceconnectdefaults-syntax.yaml"></a>

```
  [Namespace](#cfn-ecs-cluster-serviceconnectdefaults-namespace): String
```

## Properties<a name="aws-properties-ecs-cluster-serviceconnectdefaults-properties"></a>

`Namespace`  <a name="cfn-ecs-cluster-serviceconnectdefaults-namespace"></a>
The namespace name or full Amazon Resource Name \(ARN\) of the AWS Cloud Map namespace that's used when you create a service and don't specify a Service Connect configuration\. The namespace name can include up to 1024 characters\. The name is case\-sensitive\. The name can't include hyphens \(\-\), tilde \(\~\), greater than \(>\), less than \(<\), or slash \(/\)\.  
If you enter an existing namespace name or ARN, then that namespace will be used\. Any namespace type is supported\. The namespace must be in this account and this AWS Region\.  
If you enter a new name, a AWS Cloud Map namespace will be created\. Amazon ECS creates a AWS Cloud Map namespace with the "API calls" method of instance discovery only\. This instance discovery method is the "HTTP" namespace type in the AWS Command Line Interface\. Other types of instance discovery aren't used by Service Connect\.  
If you update the service with an empty string `""` for the namespace name, the cluster configuration for Service Connect is removed\. Note that the namespace will remain in AWS Cloud Map and must be deleted separately\.  
For more information about AWS Cloud Map, see [Working with Services](https://docs.aws.amazon.com/) in the * AWS Cloud Map Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)