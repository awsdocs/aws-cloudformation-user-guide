# AWS::ECS::Cluster<a name="aws-resource-ecs-cluster"></a>

The `AWS::ECS::Cluster` resource creates an Amazon Elastic Container Service \(Amazon ECS\) cluster\.

## Syntax<a name="aws-resource-ecs-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::Cluster",
  "Properties" : {
      "[CapacityProviders](#cfn-ecs-cluster-capacityproviders)" : [ String, ... ],
      "[ClusterName](#cfn-ecs-cluster-clustername)" : String,
      "[ClusterSettings](#cfn-ecs-cluster-clustersettings)" : [ ClusterSettings, ... ],
      "[Configuration](#cfn-ecs-cluster-configuration)" : ClusterConfiguration,
      "[DefaultCapacityProviderStrategy](#cfn-ecs-cluster-defaultcapacityproviderstrategy)" : [ CapacityProviderStrategyItem, ... ],
      "[ServiceConnectDefaults](#cfn-ecs-cluster-serviceconnectdefaults)" : ServiceConnectDefaults,
      "[Tags](#cfn-ecs-cluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ecs-cluster-syntax.yaml"></a>

```
Type: AWS::ECS::Cluster
Properties: 
  [CapacityProviders](#cfn-ecs-cluster-capacityproviders): 
    - String
  [ClusterName](#cfn-ecs-cluster-clustername): String
  [ClusterSettings](#cfn-ecs-cluster-clustersettings): 
    - ClusterSettings
  [Configuration](#cfn-ecs-cluster-configuration): 
    ClusterConfiguration
  [DefaultCapacityProviderStrategy](#cfn-ecs-cluster-defaultcapacityproviderstrategy): 
    - CapacityProviderStrategyItem
  [ServiceConnectDefaults](#cfn-ecs-cluster-serviceconnectdefaults): 
    ServiceConnectDefaults
  [Tags](#cfn-ecs-cluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ecs-cluster-properties"></a>

`CapacityProviders`  <a name="cfn-ecs-cluster-capacityproviders"></a>
The short name of one or more capacity providers to associate with the cluster\. A capacity provider must be associated with a cluster before it can be included as part of the default capacity provider strategy of the cluster or used in a capacity provider strategy when calling the [CreateService](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_CreateService.html) or [RunTask](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RunTask.html) actions\.  
If specifying a capacity provider that uses an Auto Scaling group, the capacity provider must be created but not associated with another cluster\. New Auto Scaling group capacity providers can be created with the [CreateCapacityProvider](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_CreateCapacityProvider.html) API operation\.  
To use a AWS Fargate capacity provider, specify either the `FARGATE` or `FARGATE_SPOT` capacity providers\. The AWS Fargate capacity providers are available to all accounts and only need to be associated with a cluster to be used\.  
The [PutCapacityProvider](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_PutCapacityProvider.html) API operation is used to update the list of available capacity providers for a cluster after the cluster is created\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterName`  <a name="cfn-ecs-cluster-clustername"></a>
A user\-generated string that you use to identify your cluster\. If you don't specify a name, AWS CloudFormation generates a unique physical ID for the name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterSettings`  <a name="cfn-ecs-cluster-clustersettings"></a>
The setting to use when creating a cluster\. This parameter is used to use CloudWatch Container Insights for a cluster\. If this value is specified, it will override the `containerInsights` value set with [PutAccountSetting](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_PutAccountSetting.html) or [PutAccountSettingDefault](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_PutAccountSettingDefault.html)\.  
*Required*: No  
*Type*: [List](aws-properties-ecs-cluster-clustersettings.md) of [ClusterSettings](aws-properties-ecs-cluster-clustersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-ecs-cluster-configuration"></a>
The execute command configuration for the cluster\.  
*Required*: No  
*Type*: [ClusterConfiguration](aws-properties-ecs-cluster-clusterconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultCapacityProviderStrategy`  <a name="cfn-ecs-cluster-defaultcapacityproviderstrategy"></a>
The default capacity provider strategy for the cluster\. When services or tasks are run in the cluster with no launch type or capacity provider strategy specified, the default capacity provider strategy is used\.  
*Required*: No  
*Type*: List of [CapacityProviderStrategyItem](aws-properties-ecs-cluster-capacityproviderstrategyitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceConnectDefaults`  <a name="cfn-ecs-cluster-serviceconnectdefaults"></a>
Use this parameter to set a default Service Connect namespace\. After you set a default Service Connect namespace, any new services with Service Connect turned on that are created in the cluster are added as client services in the namespace\. This setting only applies to new services that set the `enabled` parameter to `true` in the `ServiceConnectConfiguration`\. You can set the namespace of each service individually in the `ServiceConnectConfiguration` to override this default parameter\.  
Tasks that run in a namespace can use short names to connect to services in the namespace\. Tasks can connect to services across all of the clusters in the namespace\. Tasks connect through a managed proxy container that collects logs and metrics for increased visibility\. Only the tasks that Amazon ECS services create are supported with Service Connect\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: [ServiceConnectDefaults](aws-properties-ecs-cluster-serviceconnectdefaults.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ecs-cluster-tags"></a>
The metadata that you apply to the cluster to help you categorize and organize them\. Each tag consists of a key and an optional value\. You define both\.  
The following basic restrictions apply to tags:  
+ Maximum number of tags per resource \- 50
+ For each resource, each tag key must be unique, and each tag key can have only one value\.
+ Maximum key length \- 128 Unicode characters in UTF\-8
+ Maximum value length \- 256 Unicode characters in UTF\-8
+ If your tagging schema is used across multiple services and resources, remember that other services may have restrictions on allowed characters\. Generally allowed characters are: letters, numbers, and spaces representable in UTF\-8, and the following characters: \+ \- = \. \_ : / @\.
+ Tag keys and values are case\-sensitive\.
+ Do not use `aws:`, `AWS:`, or any upper or lowercase combination of such as a prefix for either keys or values as it is reserved for AWS use\. You cannot edit or delete tag keys or values with this prefix\. Tags with this prefix do not count against your tags per resource limit\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecs-cluster-return-values"></a>

### Ref<a name="aws-resource-ecs-cluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

In the following example, the `Ref` function returns the name of the `MyECSCluster` cluster, such as `MyStack-MyECSCluster-NT5EUXTNTXXD`\.

 `{ "Ref": "MyECSCluster" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecs-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecs-cluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon ECS cluster, such as `arn:aws:ecs:us-east-2:123456789012:cluster/MyECSCluster`\.

## Examples<a name="aws-resource-ecs-cluster--examples"></a>



### Define a cluster with the Fargate capacity providers and a default capacity provider strategy defined<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_the__capacity_providers_and_a_default_capacity_provider_strategy_defined"></a>

The following example defines a cluster named `MyFargateCluster` with the `FARGATE` and `FARGATE_SPOT` capacity providers\. A default capacity provider strategy is also defined where tasks launched will be split evenly between the `FARGATE` and `FARGATE_SPOT` capacity providers\.

#### JSON<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_the__capacity_providers_and_a_default_capacity_provider_strategy_defined--json"></a>

```
"ECSCluster": {
    "Type": "AWS: : ECS: : Cluster",
    "Properties": {
        "ClusterName": "MyFargateCluster",
        "CapacityProviders": [
            "FARGATE",
            "FARGATE_SPOT"
        ],
        "DefaultCapacityProviderStrategy": [
            {
                "CapacityProvider": "FARGATE",
                "Weight": 1
            },
            {
                "CapacityProvider": "FARGATE_SPOT",
                "Weight": 1
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_the__capacity_providers_and_a_default_capacity_provider_strategy_defined--yaml"></a>

```
ECSCluster:
  Type: 'AWS::ECS::Cluster'
  Properties:
    ClusterName: MyFargateCluster
    CapacityProviders:
      - FARGATE
      - FARGATE_SPOT
    DefaultCapacityProviderStrategy:
      - CapacityProvider: FARGATE
        Weight: 1
      - CapacityProvider: FARGATE_SPOT
        Weight: 1
```

### Define a cluster with an ECS Exec configuration defined<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_an_ECS_Exec_configuration_defined"></a>

The following example defines a cluster named `MyCluster` with ECS Exec enabled using the default logging configuration\. For more information, see [Using ECS Exec for debugging](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-exec.html) in the *Amazon ECS Developer Guide*\.

#### JSON<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_an_ECS_Exec_configuration_defined--json"></a>

```
{
    "ECSCluster": {
        "Type": "AWS::ECS::Cluster",
        "Properties": {
            "ClusterName": "MyCluster",
            "Configuration": {
                "ExecuteCommandConfiguration": {
                    "Logging": "DEFAULT"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecs-cluster--examples--Define_a_cluster_with_an_ECS_Exec_configuration_defined--yaml"></a>

```
ECSCluster:
  Type: 'AWS::ECS::Cluster'
  Properties:
    ClusterName: MyCluster
    Configuration:
       ExecuteCommandConfiguration:
          Logging: DEFAULT
```

### Define an empty cluster<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster"></a>

The following example defines an empty cluster named `MyEmptyCluster`\.

#### JSON<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster--json"></a>

```
"ECSCluster": {
    "Type": "AWS::ECS::Cluster",
    "Properties": {
        "ClusterName": "MyEmptyCluster"
    }
}
```

#### YAML<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster--yaml"></a>

```
ECSCluster:
  Type: 'AWS::ECS::Cluster'
  Properties:
    ClusterName: MyEmptyCluster
```

### Define an empty cluster with CloudWatch Container Insights enabled and defined tags<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster_with_CloudWatch_Container_Insights_enabled_and_defined_tags"></a>

The following example defines an empty cluster named `MyCluster` with CloudWatch Container Insights enabled that is tagged with the key `environment` and the value `production`\.

#### JSON<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster_with_CloudWatch_Container_Insights_enabled_and_defined_tags--json"></a>

```
"ECSCluster": {
    "Type": "AWS::ECS::Cluster",
    "Properties": {
        "ClusterName": "MyCluster",
        "ClusterSettings": [
            {
                "Name": "containerInsights",
                "Value": "enabled"
            }
        ],
        "Tags": [
            {
                "Key": "environment",
                "Value": "production"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-ecs-cluster--examples--Define_an_empty_cluster_with_CloudWatch_Container_Insights_enabled_and_defined_tags--yaml"></a>

```
ECSCluster:
  Type: 'AWS::ECS::Cluster'
  Properties:
    ClusterName: MyCluster
    ClusterSettings:
      - Name: containerInsights
        Value: enabled
    Tags:
      - Key: environment
        Value: production
```