# Amazon SageMaker Endpoint Tag<a name="aws-properties-sagemaker-endpoint-tag"></a>

<a name="aws-properties-sagemaker-endpoint-tag-description"></a>The `Tag` property type specifies tags for the endpoint resource\. Use tags to manage endpoint resources\.

<a name="aws-properties-sagemaker-endpoint-tag-inheritance"></a> `Tag` is a property of the [AWS::SageMaker::Endpoint](aws-resource-sagemaker-endpoint.md) resource\.

## Syntax<a name="aws-properties-sagemaker-endpoint-tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-tag-syntax.json"></a>

```
{
  "[Key](#cfn-sagemaker-endpoint-tag-key)" : String,
  "[Value](#cfn-sagemaker-endpoint-tag-value)" : String
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-tag-syntax.yaml"></a>

```
[Key](#cfn-sagemaker-endpoint-tag-key): String
[Value](#cfn-sagemaker-endpoint-tag-value)" : String
```

## Properties<a name="aws-properties-sagemaker-endpoint-tag-properties"></a>

`Key`  <a name="cfn-sagemaker-endpoint-tag-key"></a>
The key name of the tag\. You can specify a value that is 1 to 127 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-sagemaker-endpoint-tag-value"></a>
The value for the tag\. You can specify a value that is 1 to 255 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 