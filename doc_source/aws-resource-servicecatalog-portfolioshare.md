# AWS::ServiceCatalog::PortfolioShare<a name="aws-resource-servicecatalog-portfolioshare"></a>

Shares the specified portfolio with the specified account\.

## Syntax<a name="aws-resource-servicecatalog-portfolioshare-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioshare-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioShare",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-portfolioshare-acceptlanguage)" : String,
      "[AccountId](#cfn-servicecatalog-portfolioshare-accountid)" : String,
      "[PortfolioId](#cfn-servicecatalog-portfolioshare-portfolioid)" : String,
      "[ShareTagOptions](#cfn-servicecatalog-portfolioshare-sharetagoptions)" : Boolean
    }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioshare-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::PortfolioShare
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-portfolioshare-acceptlanguage): String
  [AccountId](#cfn-servicecatalog-portfolioshare-accountid): String
  [PortfolioId](#cfn-servicecatalog-portfolioshare-portfolioid): String
  [ShareTagOptions](#cfn-servicecatalog-portfolioshare-sharetagoptions): Boolean
```

## Properties<a name="aws-resource-servicecatalog-portfolioshare-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioshare-acceptlanguage"></a>
The language code\.  
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AccountId`  <a name="cfn-servicecatalog-portfolioshare-accountid"></a>
The AWS account ID\. For example, `123456789012`\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioshare-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShareTagOptions`  <a name="cfn-servicecatalog-portfolioshare-sharetagoptions"></a>
Indicates whether TagOptions sharing is enabled or disabled for the portfolio share\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-portfolioshare-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioshare-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the identifier of the portfolio share\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-portfolioshare--seealso"></a>
+ [CreatePortfolioShare](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreatePortfolioShare.html) in the *AWS Service Catalog API Reference*

