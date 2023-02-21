# AWS::IoTTwinMaker::Entity Component<a name="aws-properties-iottwinmaker-entity-component"></a>

The entity component\.

## Syntax<a name="aws-properties-iottwinmaker-entity-component-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-component-syntax.json"></a>

```
{
  "[ComponentName](#cfn-iottwinmaker-entity-component-componentname)" : String,
  "[ComponentTypeId](#cfn-iottwinmaker-entity-component-componenttypeid)" : String,
  "[DefinedIn](#cfn-iottwinmaker-entity-component-definedin)" : String,
  "[Description](#cfn-iottwinmaker-entity-component-description)" : String,
  "[Properties](#cfn-iottwinmaker-entity-component-properties)" : {Key : Value, ...},
  "[PropertyGroups](#cfn-iottwinmaker-entity-component-propertygroups)" : {Key : Value, ...},
  "[Status](#cfn-iottwinmaker-entity-component-status)" : Status
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-component-syntax.yaml"></a>

```
  [ComponentName](#cfn-iottwinmaker-entity-component-componentname): String
  [ComponentTypeId](#cfn-iottwinmaker-entity-component-componenttypeid): String
  [DefinedIn](#cfn-iottwinmaker-entity-component-definedin): String
  [Description](#cfn-iottwinmaker-entity-component-description): String
  [Properties](#cfn-iottwinmaker-entity-component-properties): 
    Key : Value
  [PropertyGroups](#cfn-iottwinmaker-entity-component-propertygroups): 
    Key : Value
  [Status](#cfn-iottwinmaker-entity-component-status): 
    Status
```

## Properties<a name="aws-properties-iottwinmaker-entity-component-properties"></a>

`ComponentName`  <a name="cfn-iottwinmaker-entity-component-componentname"></a>
The name of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentTypeId`  <a name="cfn-iottwinmaker-entity-component-componenttypeid"></a>
The ID of the ComponentType\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefinedIn`  <a name="cfn-iottwinmaker-entity-component-definedin"></a>
The name of the property definition set in the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iottwinmaker-entity-component-description"></a>
The description of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Properties`  <a name="cfn-iottwinmaker-entity-component-properties"></a>
An object that maps strings to the properties to set in the component type\. Each string in the mapping must be unique to this object\.  
*Required*: No  
*Type*: Map of [Property](aws-properties-iottwinmaker-entity-property.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyGroups`  <a name="cfn-iottwinmaker-entity-component-propertygroups"></a>
An object that maps strings to the property groups in the component type\. Each string in the mapping must be unique to this object\.  
*Required*: No  
*Type*: Map of [PropertyGroup](aws-properties-iottwinmaker-entity-propertygroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-iottwinmaker-entity-component-status"></a>
The status of the component\.  
*Required*: No  
*Type*: [Status](aws-properties-iottwinmaker-entity-status.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)