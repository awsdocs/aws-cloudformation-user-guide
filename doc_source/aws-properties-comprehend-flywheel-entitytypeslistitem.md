# AWS::Comprehend::Flywheel EntityTypesListItem<a name="aws-properties-comprehend-flywheel-entitytypeslistitem"></a>

An entity type within a labeled training dataset that Amazon Comprehend uses to train a custom entity recognizer\.

## Syntax<a name="aws-properties-comprehend-flywheel-entitytypeslistitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-flywheel-entitytypeslistitem-syntax.json"></a>

```
{
  "[Type](#cfn-comprehend-flywheel-entitytypeslistitem-type)" : String
}
```

### YAML<a name="aws-properties-comprehend-flywheel-entitytypeslistitem-syntax.yaml"></a>

```
  [Type](#cfn-comprehend-flywheel-entitytypeslistitem-type): String
```

## Properties<a name="aws-properties-comprehend-flywheel-entitytypeslistitem-properties"></a>

`Type`  <a name="cfn-comprehend-flywheel-entitytypeslistitem-type"></a>
An entity type within a labeled training dataset that Amazon Comprehend uses to train a custom entity recognizer\.  
Entity types must not contain the following invalid characters: \\n \(line break\), \\\\n \(escaped line break, \\r \(carriage return\), \\\\r \(escaped carriage return\), \\t \(tab\), \\\\t \(escaped tab\), space, and , \(comma\)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `^(?![^\n\r\t,]*\\n|\\r|\\t)[^\n\r\t,]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)