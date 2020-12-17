# AWS::ServiceCatalog::TagOption<a name="aws-resource-servicecatalog-tagoption"></a>

Specifies a TagOption\. A TagOption is a key\-value pair managed by AWS Service Catalog that serves as a template for creating an AWS tag\.

## Syntax<a name="aws-resource-servicecatalog-tagoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-tagoption-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::TagOption",
  "Properties" : {
      "[Active](#cfn-servicecatalog-tagoption-active)" : Boolean,
      "[Key](#cfn-servicecatalog-tagoption-key)" : String,
      "[Value](#cfn-servicecatalog-tagoption-value)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-tagoption-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::TagOption
Properties: 
  [Active](#cfn-servicecatalog-tagoption-active): Boolean
  [Key](#cfn-servicecatalog-tagoption-key): String
  [Value](#cfn-servicecatalog-tagoption-value): String
```

## Properties<a name="aws-resource-servicecatalog-tagoption-properties"></a>

`Active`  <a name="cfn-servicecatalog-tagoption-active"></a>
The TagOption active state\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-servicecatalog-tagoption-key"></a>
The TagOption key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-servicecatalog-tagoption-value"></a>
The TagOption value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-tagoption-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-tagoption-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the TagOption identifier\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-tagoption--seealso"></a>
+ [CreateTagOption](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateTagOption.html) in the *AWS Service Catalog API Reference*

