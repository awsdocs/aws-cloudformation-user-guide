# AWS::ECS::Cluster CapacityProviderStrategyItem<a name="aws-properties-ecs-cluster-capacityproviderstrategyitem"></a>

The `CapacityProviderStrategyItem` property specifies the details of the default capacity provider strategy for the cluster\. When services or tasks are run in the cluster with no launch type or capacity provider strategy specified, the default capacity provider strategy is used\.

## Syntax<a name="aws-properties-ecs-cluster-capacityproviderstrategyitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-cluster-capacityproviderstrategyitem-syntax.json"></a>

```
{
  "[Base](#cfn-ecs-cluster-capacityproviderstrategyitem-base)" : Integer,
  "[CapacityProvider](#cfn-ecs-cluster-capacityproviderstrategyitem-capacityprovider)" : String,
  "[Weight](#cfn-ecs-cluster-capacityproviderstrategyitem-weight)" : Integer
}
```

### YAML<a name="aws-properties-ecs-cluster-capacityproviderstrategyitem-syntax.yaml"></a>

```
  [Base](#cfn-ecs-cluster-capacityproviderstrategyitem-base): Integer
  [CapacityProvider](#cfn-ecs-cluster-capacityproviderstrategyitem-capacityprovider): String
  [Weight](#cfn-ecs-cluster-capacityproviderstrategyitem-weight): Integer
```

## Properties<a name="aws-properties-ecs-cluster-capacityproviderstrategyitem-properties"></a>

`Base`  <a name="cfn-ecs-cluster-capacityproviderstrategyitem-base"></a>
The *base* value designates how many tasks, at a minimum, to run on the specified capacity provider\. Only one capacity provider in a capacity provider strategy can have a *base* defined\. If no value is specified, the default value of `0` is used\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityProvider`  <a name="cfn-ecs-cluster-capacityproviderstrategyitem-capacityprovider"></a>
The short name of the capacity provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-ecs-cluster-capacityproviderstrategyitem-weight"></a>
The *weight* value designates the relative percentage of the total number of tasks launched that should use the specified capacity provider\. The `weight` value is taken into consideration after the `base` value, if defined, is satisfied\.  
If no `weight` value is specified, the default value of `0` is used\. When multiple capacity providers are specified within a capacity provider strategy, at least one of the capacity providers must have a weight value greater than zero and any capacity providers with a weight of `0` can't be used to place tasks\. If you specify multiple capacity providers in a strategy that all have a weight of `0`, any `RunTask` or `CreateService` actions using the capacity provider strategy will fail\.  
An example scenario for using weights is defining a strategy that contains two capacity providers and both have a weight of `1`, then when the `base` is satisfied, the tasks will be split evenly across the two capacity providers\. Using that same logic, if you specify a weight of `1` for *capacityProviderA* and a weight of `4` for *capacityProviderB*, then for every one task that's run using *capacityProviderA*, four tasks would use *capacityProviderB*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)