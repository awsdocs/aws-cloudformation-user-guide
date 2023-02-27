# AWS::IoTTwinMaker::Entity Property<a name="aws-properties-iottwinmaker-entity-property"></a>

An object that sets information about a property\.

## Syntax<a name="aws-properties-iottwinmaker-entity-property-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-property-syntax.json"></a>

```
{
  "[Definition](#cfn-iottwinmaker-entity-property-definition)" : Definition,
  "[Value](#cfn-iottwinmaker-entity-property-value)" : DataValue
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-property-syntax.yaml"></a>

```
  [Definition](#cfn-iottwinmaker-entity-property-definition): 
    Definition
  [Value](#cfn-iottwinmaker-entity-property-value): 
    DataValue
```

## Properties<a name="aws-properties-iottwinmaker-entity-property-properties"></a>

`Definition`  <a name="cfn-iottwinmaker-entity-property-definition"></a>
An object that specifies information about a property\.  
*Required*: No  
*Type*: [Definition](aws-properties-iottwinmaker-entity-definition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iottwinmaker-entity-property-value"></a>
An object that contains information about a value for a time series property\.  
*Required*: No  
*Type*: [DataValue](aws-properties-iottwinmaker-entity-datavalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)