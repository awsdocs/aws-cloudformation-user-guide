# AWS::ServiceCatalog::Portfolio<a name="aws-resource-servicecatalog-portfolio"></a>

Creates a portfolio for AWS Service Catalog\. For more information, see [CreatePortfolio](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreatePortfolio.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-portfolio-syntax)
+ [Properties](#aws-resource-servicecatalog-portfolio-properties)
+ [Return Values](#aws-resource-servicecatalog-portfolio-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-portfolio-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolio-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::Portfolio",
  "Properties" : {
    "[ProviderName](#cfn-servicecatalog-portfolio-providername)" : String,
    "[Description](#cfn-servicecatalog-portfolio-description)" : String,
    "[DisplayName](#cfn-servicecatalog-portfolio-displayname)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-portfolio-acceptlanguage)" : String,
    "[Tags](#cfn-servicecatalog-portfolio-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolio-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::Portfolio"
Properties:
  [ProviderName](#cfn-servicecatalog-portfolio-providername): String
  [Description](#cfn-servicecatalog-portfolio-description): String
  [DisplayName](#cfn-servicecatalog-portfolio-displayname): String
  [AcceptLanguage](#cfn-servicecatalog-portfolio-acceptlanguage): String
  [Tags](#cfn-servicecatalog-portfolio-tags): 
    - [*Resource Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-servicecatalog-portfolio-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolio-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-portfolio-description"></a>
The description of the portfolio\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisplayName`  <a name="cfn-servicecatalog-portfolio-displayname"></a>
The name to use for display purposes\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ProviderName`  <a name="cfn-servicecatalog-portfolio-providername"></a>
The name of the portfolio provider\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalog-portfolio-tags"></a>
One or more tags\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-servicecatalog-portfolio-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-portfolio-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::Portfolio` resource to the intrinsic `Ref` function, the function returns the portfolio identifier\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-servicecatalog-portfolio-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`PortfolioName`  
The name of the portfolio\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.