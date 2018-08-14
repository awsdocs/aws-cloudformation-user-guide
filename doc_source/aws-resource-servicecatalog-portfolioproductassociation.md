# AWS::ServiceCatalog::PortfolioProductAssociation<a name="aws-resource-servicecatalog-portfolioproductassociation"></a>

Associates the specified product with the specified portfolio for AWS Service Catalog\. For more information, see [AssociateProductWithPortfolio](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociateProductWithPortfolio.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-portfolioproductassociation-syntax)
+ [Properties](#aws-resource-servicecatalog-portfolioproductassociation-properties)
+ [Return Values](#aws-resource-servicecatalog-portfolioproductassociation-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioProductAssociation",
  "Properties" : {
    "[SourcePortfolioId](#cfn-servicecatalog-portfolioproductassociation-sourceportfolioid)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-portfolioproductassociation-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-portfolioproductassociation-portfolioid)" : String,
    "[ProductId](#cfn-servicecatalog-portfolioproductassociation-productid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::PortfolioProductAssociation"
Properties:
  [SourcePortfolioId](#cfn-servicecatalog-portfolioproductassociation-sourceportfolioid): String
  [AcceptLanguage](#cfn-servicecatalog-portfolioproductassociation-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-portfolioproductassociation-portfolioid): String
  [ProductId](#cfn-servicecatalog-portfolioproductassociation-productid): String
```

## Properties<a name="aws-resource-servicecatalog-portfolioproductassociation-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioproductassociation-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioproductassociation-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-portfolioproductassociation-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SourcePortfolioId`  <a name="cfn-servicecatalog-portfolioproductassociation-sourceportfolioid"></a>
The identifier of the source portfolio\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-portfolioproductassociation-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioproductassociation-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::PortfolioProductAssociation` resource to the intrinsic `Ref` function, the function returns a unique identifier for the association\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.