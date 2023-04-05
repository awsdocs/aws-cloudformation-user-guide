# AWS::Comprehend::Flywheel DocumentClassificationConfig<a name="aws-properties-comprehend-flywheel-documentclassificationconfig"></a>

Configuration required for a custom classification model\.

## Syntax<a name="aws-properties-comprehend-flywheel-documentclassificationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-flywheel-documentclassificationconfig-syntax.json"></a>

```
{
  "[Labels](#cfn-comprehend-flywheel-documentclassificationconfig-labels)" : [ String, ... ],
  "[Mode](#cfn-comprehend-flywheel-documentclassificationconfig-mode)" : String
}
```

### YAML<a name="aws-properties-comprehend-flywheel-documentclassificationconfig-syntax.yaml"></a>

```
  [Labels](#cfn-comprehend-flywheel-documentclassificationconfig-labels): 
    - String
  [Mode](#cfn-comprehend-flywheel-documentclassificationconfig-mode): String
```

## Properties<a name="aws-properties-comprehend-flywheel-documentclassificationconfig-properties"></a>

`Labels`  <a name="cfn-comprehend-flywheel-documentclassificationconfig-labels"></a>
One or more labels to associate with the custom classifier\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Mode`  <a name="cfn-comprehend-flywheel-documentclassificationconfig-mode"></a>
Classification mode indicates whether the documents are `MULTI_CLASS` or `MULTI_LABEL`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MULTI_CLASS | MULTI_LABEL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)