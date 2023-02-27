# AWS::ServiceCatalog::PortfolioPrincipalAssociation<a name="aws-resource-servicecatalog-portfolioprincipalassociation"></a>

Associates the specified principal ARN with the specified portfolio\.

If you share the portfolio with principal name sharing enabled, the `PrincipalARN` association is included in the share\. 

The `PortfolioID`, `PrincipalARN`, and `PrincipalType` parameters are required\. 

You can associate a maximum of 10 Principals with a portfolio using `PrincipalType` as `IAM_PATTERN` 

**Note**  
When you associate a principal with portfolio, a potential privilege escalation path may occur when that portfolio is then shared with other accounts\. For a user in a recipient account who is *not* an Service Catalog Admin, but still has the ability to create Principals \(Users/Groups/Roles\), that user could create a role that matches a principal name association for the portfolio\. Although this user may not know which principal names are associated through Service Catalog, they may be able to guess the user\. If this potential escalation path is a concern, then Service Catalog recommends using `PrincipalType` as `IAM`\. With this configuration, the `PrincipalARN` must already exist in the recipient account before it can be associated\. 

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
The ARN of the principal \(IAM user, role, or group\)\. This field allows an ARN with no `accountID` if `PrincipalType` is `IAM_PATTERN`\.   
You can associate multiple `IAM` patterns even if the account has no principal with that name\. This is useful in Principal Name Sharing if you want to share a principal without creating it in the account that owns the portfolio\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PrincipalType`  <a name="cfn-servicecatalog-portfolioprincipalassociation-principaltype"></a>
The principal type\. The supported value is `IAM` if you use a fully defined ARN, or `IAM_PATTERN` if you use an ARN with no `accountID`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `IAM | IAM_PATTERN`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-portfolioprincipalassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioprincipalassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-servicecatalog-portfolioprincipalassociation--seealso"></a>
+ [AssociatePrincipalWithPortfolio](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociatePrincipalWithPortfolio.html) in the *AWS Service Catalog API Reference*

