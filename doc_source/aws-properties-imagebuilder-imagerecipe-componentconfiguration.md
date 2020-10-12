# AWS::ImageBuilder::ImageRecipe ComponentConfiguration<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration"></a>

 The image recipe component configuration includes the configuration details of this component\. 

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax.json"></a>

```
{
  "[ComponentArn](#cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-syntax.yaml"></a>

```
  [ComponentArn](#cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn): String
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-componentconfiguration-properties"></a>

`ComponentArn`  <a name="cfn-imagebuilder-imagerecipe-componentconfiguration-componentarn"></a>
The Amazon Resource Name \(ARN\) of the component\.   
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):component/[a-z0-9-_]+/(?:(?:(\d+|x)\.(\d+|x)\.(\d+|x))|(?:\d+\.\d+\.\d+/\d+))$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)