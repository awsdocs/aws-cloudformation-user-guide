# AWS::ImageBuilder::ImageRecipe ComponentConfiguration<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration"></a>

 Configuration details of the component\.

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax.json"></a>

```
{
  "[ComponentArn](#cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn)" : String,
  "[Parameters](#cfn-imagebuilder-imagerecipe-componentconfiguration-parameters)" : [ ComponentParameter, ... ]
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax.yaml"></a>

```
  [ComponentArn](#cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn): String
  [Parameters](#cfn-imagebuilder-imagerecipe-componentconfiguration-parameters): 
    - ComponentParameter
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-properties"></a>

`ComponentArn`  <a name="cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn"></a>
The Amazon Resource Name \(ARN\) of the component\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:[0-9]{12}|aws):component/[a-z0-9-_]+/(?:(?:([0-9]+|x)\.([0-9]+|x)\.([0-9]+|x))|(?:[0-9]+\.[0-9]+\.[0-9]+/[0-9]+))$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-imagebuilder-imagerecipe-componentconfiguration-parameters"></a>
A group of parameter settings that Image Builder uses to configure the component for a specific recipe\.  
*Required*: No  
*Type*: List of [ComponentParameter](aws-properties-imagebuilder-imagerecipe-componentparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)