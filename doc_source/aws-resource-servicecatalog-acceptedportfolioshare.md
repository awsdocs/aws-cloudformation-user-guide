# AWS::ServiceCatalog::AcceptedPortfolioShare<a name="aws-resource-servicecatalog-acceptedportfolioshare"></a>

Accepts an offer to share the specified portfolio\.

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
Type: AWS::ServiceCatalog::AcceptedPortfolioShare
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-acceptedportfolioshare-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-acceptedportfolioshare-portfolioid): String
```

## Properties<a name="aws-resource-servicecatalog-acceptedportfolioshare-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-acceptedportfolioshare-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-acceptedportfolioshare-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-acceptedportfolioshare-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-acceptedportfolioshare-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-acceptedportfolioshare--seealso"></a>
+ [AcceptPortfolioShare](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AcceptPortfolioShare.html) in the *AWS Service Catalog API Reference*

