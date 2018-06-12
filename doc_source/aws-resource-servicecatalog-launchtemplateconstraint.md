# AWS::ServiceCatalog::LaunchTemplateConstraint<a name="aws-resource-servicecatalog-launchtemplateconstraint"></a>

Creates a template constraint for AWS Service Catalog\. For more information, see [CreateConstraint](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-launchtemplateconstraint-syntax)
+ [Properties](#aws-resource-servicecatalog-launchtemplateconstraint-properties)
+ [Return Values](#aws-resource-servicecatalog-launchtemplateconstraint-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::LaunchTemplateConstraint",
  "Properties" : {
    "[Description](#cfn-servicecatalog-launchtemplateconstraint-description)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-launchtemplateconstraint-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-launchtemplateconstraint-portfolioid)" : String,
    "[ProductId](#cfn-servicecatalog-launchtemplateconstraint-productid)" : String,
    "[Rules](#cfn-servicecatalog-launchtemplateconstraint-rules)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-launchtemplateconstraint-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::LaunchTemplateConstraint"
Properties:
  [Description](#cfn-servicecatalog-launchtemplateconstraint-description): String
  [AcceptLanguage](#cfn-servicecatalog-launchtemplateconstraint-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-launchtemplateconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-launchtemplateconstraint-productid): String
  [Rules](#cfn-servicecatalog-launchtemplateconstraint-rules): String
```

## Properties<a name="aws-resource-servicecatalog-launchtemplateconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-launchtemplateconstraint-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-launchtemplateconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PortfolioId`  <a name="cfn-servicecatalog-launchtemplateconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-launchtemplateconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Rules`  <a name="cfn-servicecatalog-launchtemplateconstraint-rules"></a>
The constraint rules\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-launchtemplateconstraint-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-launchtemplateconstraint-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::LaunchTemplateConstraint` resource to the intrinsic `Ref` function, the function returns the identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.