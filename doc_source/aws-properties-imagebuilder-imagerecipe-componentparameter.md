# AWS::ImageBuilder::ImageRecipe ComponentParameter<a name="aws-properties-imagebuilder-imagerecipe-componentparameter"></a>

Contains a key/value pair that sets the named component parameter\.

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-componentparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-componentparameter-syntax.json"></a>

```
{
  "[Name](#cfn-imagebuilder-imagerecipe-componentparameter-name)" : String,
  "[Value](#cfn-imagebuilder-imagerecipe-componentparameter-value)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-componentparameter-syntax.yaml"></a>

```
  [Name](#cfn-imagebuilder-imagerecipe-componentparameter-name): String
  [Value](#cfn-imagebuilder-imagerecipe-componentparameter-value): 
    - String
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-componentparameter-properties"></a>

`Name`  <a name="cfn-imagebuilder-imagerecipe-componentparameter-name"></a>
The name of the component parameter to set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[^\x00]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-imagebuilder-imagerecipe-componentparameter-value"></a>
Sets the value for the named component parameter\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)