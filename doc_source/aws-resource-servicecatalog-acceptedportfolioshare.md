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

## Return Values<a name="aws-resource-servicecatalog-acceptedportfolioshare-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-acceptedportfolioshare-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-servicecatalog-acceptedportfolioshare--seealso"></a>
+ [AcceptPortfolioShare](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AcceptPortfolioShare.html) in the *AWS Service Catalog API Reference*

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
