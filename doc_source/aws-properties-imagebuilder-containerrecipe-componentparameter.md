# AWS::ImageBuilder::ContainerRecipe ComponentParameter<a name="aws-properties-imagebuilder-containerrecipe-componentparameter"></a>

Contains a key/value pair that sets the named component parameter\.

## Syntax<a name="aws-properties-imagebuilder-containerrecipe-componentparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-containerrecipe-componentparameter-syntax.json"></a>

```
{
  "[Name](#cfn-imagebuilder-containerrecipe-componentparameter-name)" : String,
  "[Value](#cfn-imagebuilder-containerrecipe-componentparameter-value)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-imagebuilder-containerrecipe-componentparameter-syntax.yaml"></a>

```
  [Name](#cfn-imagebuilder-containerrecipe-componentparameter-name): String
  [Value](#cfn-imagebuilder-containerrecipe-componentparameter-value): 
    - String
```

## Properties<a name="aws-properties-imagebuilder-containerrecipe-componentparameter-properties"></a>

`Name`  <a name="cfn-imagebuilder-containerrecipe-componentparameter-name"></a>
The name of the component parameter to set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[^\x00]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-imagebuilder-containerrecipe-componentparameter-value"></a>
Sets the value for the named component parameter\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)