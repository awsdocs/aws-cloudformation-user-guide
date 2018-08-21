# AWS::ServiceCatalog::TagOption<a name="aws-resource-servicecatalog-tagoption"></a>

A TagOption is a key\-value pair managed by AWS Service Catalog that serves as a template for creating an AWS tag\. For more information, see [AWS Service Catalog TagOptionLibrary](http://docs.aws.amazon.com/servicecatalog/latest/adminguide/tagoptions.html) in the *AWS Service Catalog Administrator Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-tagoption-syntax)
+ [Properties](#aws-resource-servicecatalog-tagoption-properties)
+ [Return Values](#aws-resource-servicecatalog-tagoption-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-tagoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-tagoption-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::TagOption",
  "Properties" : {
    "[Active](#cfn-servicecatalog-tagoption-active)" : Boolean,
    "[Value](#cfn-servicecatalog-tagoption-value)" : String,
    "[Key](#cfn-servicecatalog-tagoption-key)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-tagoption-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::TagOption"
Properties:
  [Active](#cfn-servicecatalog-tagoption-active): Boolean
  [Value](#cfn-servicecatalog-tagoption-value): String
  [Key](#cfn-servicecatalog-tagoption-key): String
```

## Properties<a name="aws-resource-servicecatalog-tagoption-properties"></a>

`Active`  <a name="cfn-servicecatalog-tagoption-active"></a>
Indicates whether the TagOption is active\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Key`  <a name="cfn-servicecatalog-tagoption-key"></a>
The TagOption key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Value`  <a name="cfn-servicecatalog-tagoption-value"></a>
The TagOption value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-tagoption-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-tagoption-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::TagOption` resource to the intrinsic `Ref` function, the function returns the TagOption identifier\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.