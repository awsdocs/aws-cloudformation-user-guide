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

## Return Values<a name="aws-resource-servicecatalog-tagoption-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-tagoption-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the TagOption identifier\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-servicecatalog-tagoption--seealso"></a>
+ [CreateTagOption](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateTagOption.html) in the *AWS Service Catalog API Reference*

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
