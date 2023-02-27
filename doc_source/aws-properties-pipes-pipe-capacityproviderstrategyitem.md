# AWS::Pipes::Pipe CapacityProviderStrategyItem<a name="aws-properties-pipes-pipe-capacityproviderstrategyitem"></a>

The details of a capacity provider strategy\. To learn more, see [CapacityProviderStrategyItem](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_CapacityProviderStrategyItem.html) in the Amazon ECS API Reference\.

## Syntax<a name="aws-properties-pipes-pipe-capacityproviderstrategyitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-capacityproviderstrategyitem-syntax.json"></a>

```
{
  "[Base](#cfn-pipes-pipe-capacityproviderstrategyitem-base)" : Integer,
  "[CapacityProvider](#cfn-pipes-pipe-capacityproviderstrategyitem-capacityprovider)" : String,
  "[Weight](#cfn-pipes-pipe-capacityproviderstrategyitem-weight)" : Integer
}
```

### YAML<a name="aws-properties-pipes-pipe-capacityproviderstrategyitem-syntax.yaml"></a>

```
  [Base](#cfn-pipes-pipe-capacityproviderstrategyitem-base): Integer
  [CapacityProvider](#cfn-pipes-pipe-capacityproviderstrategyitem-capacityprovider): String
  [Weight](#cfn-pipes-pipe-capacityproviderstrategyitem-weight): Integer
```

## Properties<a name="aws-properties-pipes-pipe-capacityproviderstrategyitem-properties"></a>

`Base`  <a name="cfn-pipes-pipe-capacityproviderstrategyitem-base"></a>
The base value designates how many tasks, at a minimum, to run on the specified capacity provider\. Only one capacity provider in a capacity provider strategy can have a base defined\. If no value is specified, the default value of 0 is used\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityProvider`  <a name="cfn-pipes-pipe-capacityproviderstrategyitem-capacityprovider"></a>
The short name of the capacity provider\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-pipes-pipe-capacityproviderstrategyitem-weight"></a>
The weight value designates the relative percentage of the total number of tasks launched that should use the specified capacity provider\. The weight value is taken into consideration after the base value, if defined, is satisfied\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)