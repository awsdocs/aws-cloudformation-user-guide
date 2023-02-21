# AWS::IoTTwinMaker::Entity PropertyGroup<a name="aws-properties-iottwinmaker-entity-propertygroup"></a>

The property group\.

## Syntax<a name="aws-properties-iottwinmaker-entity-propertygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-entity-propertygroup-syntax.json"></a>

```
{
  "[GroupType](#cfn-iottwinmaker-entity-propertygroup-grouptype)" : String,
  "[PropertyNames](#cfn-iottwinmaker-entity-propertygroup-propertynames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-iottwinmaker-entity-propertygroup-syntax.yaml"></a>

```
  [GroupType](#cfn-iottwinmaker-entity-propertygroup-grouptype): String
  [PropertyNames](#cfn-iottwinmaker-entity-propertygroup-propertynames): 
    - String
```

## Properties<a name="aws-properties-iottwinmaker-entity-propertygroup-properties"></a>

`GroupType`  <a name="cfn-iottwinmaker-entity-propertygroup-grouptype"></a>
The group type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyNames`  <a name="cfn-iottwinmaker-entity-propertygroup-propertynames"></a>
The property names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)