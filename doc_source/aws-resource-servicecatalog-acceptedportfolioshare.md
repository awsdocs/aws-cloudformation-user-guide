# AWS::ServiceCatalog::AcceptedPortfolioShare<a name="aws-resource-servicecatalog-acceptedportfolioshare"></a>

Accepts an offer to share the specified portfolio for AWS Service Catalog\. For more information, see [AcceptPortfolioShare](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_AcceptPortfolioShare.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-acceptedportfolioshare-syntax)
+ [Properties](#aws-resource-servicecatalog-acceptedportfolioshare-properties)
+ [Return Values](#aws-resource-servicecatalog-acceptedportfolioshare-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-acceptedportfolioshare-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-acceptedportfolioshare-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::AcceptedPortfolioShare",
  "Properties" : {
    "[AcceptLanguage](#cfn-servicecatalog-acceptedportfolioshare-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-acceptedportfolioshare-portfolioid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-acceptedportfolioshare-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::AcceptedPortfolioShare"
Properties:
  [AcceptLanguage](#cfn-servicecatalog-acceptedportfolioshare-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-acceptedportfolioshare-portfolioid): String
```

## Properties<a name="aws-resource-servicecatalog-acceptedportfolioshare-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-acceptedportfolioshare-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-acceptedportfolioshare-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-acceptedportfolioshare-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-acceptedportfolioshare-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::AcceptedPortfolioShare` resource to the intrinsic `Ref` function, the function returns a unique identifier\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.