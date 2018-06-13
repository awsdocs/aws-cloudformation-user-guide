# AWS::ServiceCatalog::PortfolioShare<a name="aws-resource-servicecatalog-portfolioshare"></a>

Shares the specified portfolio for AWS Service Catalog with the specified account\. For more information, see [CreatePortfolioShare](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreatePortfolioShare.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-portfolioshare-syntax)
+ [Properties](#aws-resource-servicecatalog-portfolioshare-properties)
+ [Return Values](#aws-resource-servicecatalog-portfolioshare-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-portfolioshare-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioshare-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioShare",
  "Properties" : {
    "[AccountId](#cfn-servicecatalog-portfolioshare-accountid)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-portfolioshare-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-portfolioshare-portfolioid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioshare-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::PortfolioShare"
Properties:
  [AccountId](#cfn-servicecatalog-portfolioshare-accountid): String
  [AcceptLanguage](#cfn-servicecatalog-portfolioshare-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-portfolioshare-portfolioid): String
```

## Properties<a name="aws-resource-servicecatalog-portfolioshare-properties"></a>

`AccountId`  <a name="cfn-servicecatalog-portfolioshare-accountid"></a>
The language code\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioshare-acceptlanguage"></a>
The AWS account ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioshare-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-portfolioshare-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioshare-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::PortfolioShare` resource to the intrinsic `Ref` function, the function returns the identifier of the portfolio share\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.