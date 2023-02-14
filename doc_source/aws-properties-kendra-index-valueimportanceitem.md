# AWS::Kendra::Index ValueImportanceItem<a name="aws-properties-kendra-index-valueimportanceitem"></a>

Specifies a key\-value pair that determines the search boost value that a document receives when the key is part of the metadata of a document\.

## Syntax<a name="aws-properties-kendra-index-valueimportanceitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-valueimportanceitem-syntax.json"></a>

```
{
  "[Key](#cfn-kendra-index-valueimportanceitem-key)" : String,
  "[Value](#cfn-kendra-index-valueimportanceitem-value)" : Integer
}
```

### YAML<a name="aws-properties-kendra-index-valueimportanceitem-syntax.yaml"></a>

```
  [Key](#cfn-kendra-index-valueimportanceitem-key): String
  [Value](#cfn-kendra-index-valueimportanceitem-value): Integer
```

## Properties<a name="aws-properties-kendra-index-valueimportanceitem-properties"></a>

`Key`  <a name="cfn-kendra-index-valueimportanceitem-key"></a>
The document metadata value that receives the search boost\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-kendra-index-valueimportanceitem-value"></a>
The boost value that a document receives when the key is part of the metadata of a document\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)