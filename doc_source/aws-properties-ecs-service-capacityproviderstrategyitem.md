# AWS::ECS::Service CapacityProviderStrategyItem<a name="aws-properties-ecs-service-capacityproviderstrategyitem"></a>

The details of a capacity provider strategy\. A capacity provider strategy can be set when using the `RunTask` or `CreateService` APIs or as the default capacity provider strategy for a cluster with the `CreateCluster` API\.

Only capacity providers that are already associated with a cluster and have an `ACTIVE` or `UPDATING` status can be used in a capacity provider strategy\. The `PutClusterCapacityProviders` API is used to associate a capacity provider with a cluster\.

If specifying a capacity provider that uses an Auto Scaling group, the capacity provider must already be created\. New Auto Scaling group capacity providers can be created with the `CreateCapacityProvider` API operation\.

To use an AWS Fargate capacity provider, specify either the `FARGATE` or `FARGATE_SPOT` capacity providers\. The AWS Fargate capacity providers are available to all accounts and only need to be associated with a cluster to be used in a capacity provider strategy\.

## Syntax<a name="aws-properties-ecs-service-capacityproviderstrategyitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-capacityproviderstrategyitem-syntax.json"></a>

```
{
  "[Base](#cfn-ecs-service-capacityproviderstrategyitem-base)" : Integer,
  "[CapacityProvider](#cfn-ecs-service-capacityproviderstrategyitem-capacityprovider)" : String,
  "[Weight](#cfn-ecs-service-capacityproviderstrategyitem-weight)" : Integer
}
```

### YAML<a name="aws-properties-ecs-service-capacityproviderstrategyitem-syntax.yaml"></a>

```
  [Base](#cfn-ecs-service-capacityproviderstrategyitem-base): Integer
  [CapacityProvider](#cfn-ecs-service-capacityproviderstrategyitem-capacityprovider): String
  [Weight](#cfn-ecs-service-capacityproviderstrategyitem-weight): Integer
```

## Properties<a name="aws-properties-ecs-service-capacityproviderstrategyitem-properties"></a>

`Base`  <a name="cfn-ecs-service-capacityproviderstrategyitem-base"></a>
The *base* value designates how many tasks, at a minimum, to run on the specified capacity provider\. Only one capacity provider in a capacity provider strategy can have a *base* defined\. If no value is specified, the default value of `0` is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityProvider`  <a name="cfn-ecs-service-capacityproviderstrategyitem-capacityprovider"></a>
The short name of the capacity provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-ecs-service-capacityproviderstrategyitem-weight"></a>
The *weight* value designates the relative percentage of the total number of tasks launched that should use the specified capacity provider\. The `weight` value is taken into consideration after the `base` value, if defined, is satisfied\.  
If no `weight` value is specified, the default value of `0` is used\. When multiple capacity providers are specified within a capacity provider strategy, at least one of the capacity providers must have a weight value greater than zero and any capacity providers with a weight of `0` can't be used to place tasks\. If you specify multiple capacity providers in a strategy that all have a weight of `0`, any `RunTask` or `CreateService` actions using the capacity provider strategy will fail\.  
An example scenario for using weights is defining a strategy that contains two capacity providers and both have a weight of `1`, then when the `base` is satisfied, the tasks will be split evenly across the two capacity providers\. Using that same logic, if you specify a weight of `1` for *capacityProviderA* and a weight of `4` for *capacityProviderB*, then for every one task that's run using *capacityProviderA*, four tasks would use *capacityProviderB*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)