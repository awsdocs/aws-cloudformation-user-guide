# AWS::ServiceCatalog::PortfolioProductAssociation<a name="aws-resource-servicecatalog-portfolioproductassociation"></a>

Associates the specified product with the specified portfolio\.

A delegated admin is authorized to invoke this command\.

## Syntax<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioProductAssociation",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-portfolioproductassociation-acceptlanguage)" : String,
      "[PortfolioId](#cfn-servicecatalog-portfolioproductassociation-portfolioid)" : String,
      "[ProductId](#cfn-servicecatalog-portfolioproductassociation-productid)" : String,
      "[SourcePortfolioId](#cfn-servicecatalog-portfolioproductassociation-sourceportfolioid)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioproductassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::PortfolioProductAssociation
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-portfolioproductassociation-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-portfolioproductassociation-portfolioid): String
  [ProductId](#cfn-servicecatalog-portfolioproductassociation-productid): String
  [SourcePortfolioId](#cfn-servicecatalog-portfolioproductassociation-sourceportfolioid): String
```

## Properties<a name="aws-resource-servicecatalog-portfolioproductassociation-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioproductassociation-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioproductassociation-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-portfolioproductassociation-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePortfolioId`  <a name="cfn-servicecatalog-portfolioproductassociation-sourceportfolioid"></a>
The identifier of the source portfolio\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-portfolioproductassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioproductassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-portfolioproductassociation--seealso"></a>
+ [AssociateProductWithPortfolio](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociateProductWithPortfolio.html) in the *AWS Service Catalog API Reference*

