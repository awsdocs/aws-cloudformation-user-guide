# AWS::IoTTwinMaker::ComponentType PropertyGroup<a name="aws-properties-iottwinmaker-componenttype-propertygroup"></a>

The property group\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-propertygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-propertygroup-syntax.json"></a>

```
{
  "[GroupType](#cfn-iottwinmaker-componenttype-propertygroup-grouptype)" : String,
  "[PropertyNames](#cfn-iottwinmaker-componenttype-propertygroup-propertynames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-propertygroup-syntax.yaml"></a>

```
  [GroupType](#cfn-iottwinmaker-componenttype-propertygroup-grouptype): String
  [PropertyNames](#cfn-iottwinmaker-componenttype-propertygroup-propertynames): 
    - String
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-propertygroup-properties"></a>

`GroupType`  <a name="cfn-iottwinmaker-componenttype-propertygroup-grouptype"></a>
The group type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyNames`  <a name="cfn-iottwinmaker-componenttype-propertygroup-propertynames"></a>
The property names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)