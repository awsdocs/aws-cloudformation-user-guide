# AWS::ECS::Service CapacityProviderStrategyItem<a name="aws-properties-ecs-service-capacityproviderstrategyitem"></a>

The details of a capacity provider strategy\.

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
The *base* value designates how many tasks, at a minimum, to run on the specified capacity provider\. Only one capacity provider in a capacity provider strategy can have a *base* defined\.  
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
The *weight* value designates the relative percentage of the total number of tasks launched that should use the specified capacity provider\.  
For example, if you have a strategy that contains two capacity providers and both have a weight of `1`, then when the `base` is satisfied, the tasks will be split evenly across the two capacity providers\. Using that same logic, if you specify a weight of `1` for *capacityProviderA* and a weight of `4` for *capacityProviderB*, then for every one task that is run using *capacityProviderA*, four tasks would use *capacityProviderB*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)