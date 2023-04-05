# AWS::Comprehend::Flywheel TaskConfig<a name="aws-properties-comprehend-flywheel-taskconfig"></a>

Configuration about the custom classifier associated with the flywheel\.

## Syntax<a name="aws-properties-comprehend-flywheel-taskconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-flywheel-taskconfig-syntax.json"></a>

```
{
  "[DocumentClassificationConfig](#cfn-comprehend-flywheel-taskconfig-documentclassificationconfig)" : DocumentClassificationConfig,
  "[EntityRecognitionConfig](#cfn-comprehend-flywheel-taskconfig-entityrecognitionconfig)" : EntityRecognitionConfig,
  "[LanguageCode](#cfn-comprehend-flywheel-taskconfig-languagecode)" : String
}
```

### YAML<a name="aws-properties-comprehend-flywheel-taskconfig-syntax.yaml"></a>

```
  [DocumentClassificationConfig](#cfn-comprehend-flywheel-taskconfig-documentclassificationconfig): 
    DocumentClassificationConfig
  [EntityRecognitionConfig](#cfn-comprehend-flywheel-taskconfig-entityrecognitionconfig): 
    EntityRecognitionConfig
  [LanguageCode](#cfn-comprehend-flywheel-taskconfig-languagecode): String
```

## Properties<a name="aws-properties-comprehend-flywheel-taskconfig-properties"></a>

`DocumentClassificationConfig`  <a name="cfn-comprehend-flywheel-taskconfig-documentclassificationconfig"></a>
Configuration required for a classification model\.  
*Required*: No  
*Type*: [DocumentClassificationConfig](aws-properties-comprehend-flywheel-documentclassificationconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EntityRecognitionConfig`  <a name="cfn-comprehend-flywheel-taskconfig-entityrecognitionconfig"></a>
Configuration required for an entity recognition model\.  
*Required*: No  
*Type*: [EntityRecognitionConfig](aws-properties-comprehend-flywheel-entityrecognitionconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LanguageCode`  <a name="cfn-comprehend-flywheel-taskconfig-languagecode"></a>
Language code for the language that the model supports\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ar | de | en | es | fr | hi | it | ja | ko | pt | zh | zh-TW`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)