# AWS::ServiceCatalog::PortfolioPrincipalAssociation<a name="aws-resource-servicecatalog-portfolioprincipalassociation"></a>

Associates the specified principal ARN with the specified portfolio\.

## Syntax<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioPrincipalAssociation",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage)" : String,
      "[PortfolioId](#cfn-servicecatalog-portfolioprincipalassociation-portfolioid)" : String,
      "[PrincipalARN](#cfn-servicecatalog-portfolioprincipalassociation-principalarn)" : String,
      "[PrincipalType](#cfn-servicecatalog-portfolioprincipalassociation-principaltype)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::PortfolioPrincipalAssociation
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-portfolioprincipalassociation-portfolioid): String
  [PrincipalARN](#cfn-servicecatalog-portfolioprincipalassociation-principalarn): String
  [PrincipalType](#cfn-servicecatalog-portfolioprincipalassociation-principaltype): String
```

## Properties<a name="aws-resource-servicecatalog-portfolioprincipalassociation-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioprincipalassociation-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalARN`  <a name="cfn-servicecatalog-portfolioprincipalassociation-principalarn"></a>
The ARN of the principal \(IAM user, role, or group\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalType`  <a name="cfn-servicecatalog-portfolioprincipalassociation-principaltype"></a>
The principal type\. The supported value is `IAM`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `IAM`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-portfolioprincipalassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioprincipalassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-portfolioprincipalassociation--seealso"></a>
+ [AssociatePrincipalWithPortfolio](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociatePrincipalWithPortfolio.html) in the *AWS Service Catalog API Reference*

