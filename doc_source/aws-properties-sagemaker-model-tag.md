# Amazon SageMaker Model Tag<a name="aws-properties-sagemaker-model-tag"></a>

<a name="aws-properties-sagemaker-model-tag-description"></a>The `Tag` property type specifies tags for the model resource\. Use tags to manage endpoint resources\.

<a name="aws-properties-sagemaker-model-tag-inheritance"></a> `Tag` is a property of the [AWS::SageMaker::Model](aws-resource-sagemaker-model.md) resource\.

## Syntax<a name="aws-properties-sagemaker-model-tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-tag-syntax.json"></a>

```
{
  "[Key](#cfn-sagemaker-model-tag-key)" : String,
  "[Value](#cfn-sagemaker-model-tag-value)" : String
}
```

### YAML<a name="aws-properties-sagemaker-model-tag-syntax.yaml"></a>

```
[Key](#cfn-sagemaker-model-tag-key): String
[Value](#cfn-sagemaker-model-tag-value): String
```

## Properties<a name="aws-properties-sagemaker-model-tag-properties"></a>

`Key`  <a name="cfn-sagemaker-model-tag-key"></a>
The key name of the tag\. You can specify a value that is 1 to 127 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-sagemaker-model-tag-value"></a>
The value for the tag\. You can specify a value that is 1 to 255 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 