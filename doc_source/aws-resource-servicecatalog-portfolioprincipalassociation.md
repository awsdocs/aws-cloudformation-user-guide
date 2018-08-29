# AWS::ServiceCatalog::PortfolioPrincipalAssociation<a name="aws-resource-servicecatalog-portfolioprincipalassociation"></a>

Associates the specified principal with the specified portfolio for AWS Service Catalog\. For more information, see [AssociatePrincipalWithPortfolio](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_AssociatePrincipalWithPortfolio.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-portfolioprincipalassociation-syntax)
+ [Properties](#aws-resource-servicecatalog-portfolioprincipalassociation-properties)
+ [Return Values](#aws-resource-servicecatalog-portfolioprincipalassociation-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::PortfolioPrincipalAssociation",
  "Properties" : {
    "[PrincipalARN](#cfn-servicecatalog-portfolioprincipalassociation-principalarn)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage)" : String,
    "[PortfolioId](#cfn-servicecatalog-portfolioprincipalassociation-portfolioid)" : String,
    "[PrincipalType](#cfn-servicecatalog-portfolioprincipalassociation-principaltype)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-portfolioprincipalassociation-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::PortfolioPrincipalAssociation"
Properties:
  [PrincipalARN](#cfn-servicecatalog-portfolioprincipalassociation-principalarn): String
  [AcceptLanguage](#cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage): String
  [PortfolioId](#cfn-servicecatalog-portfolioprincipalassociation-portfolioid): String
  [PrincipalType](#cfn-servicecatalog-portfolioprincipalassociation-principaltype): String
```

## Properties<a name="aws-resource-servicecatalog-portfolioprincipalassociation-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-portfolioprincipalassociation-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PortfolioId`  <a name="cfn-servicecatalog-portfolioprincipalassociation-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PrincipalARN`  <a name="cfn-servicecatalog-portfolioprincipalassociation-principalarn"></a>
The ARN of the principal \(IAM user, role, or group\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PrincipalType`  <a name="cfn-servicecatalog-portfolioprincipalassociation-principaltype"></a>
The principal type \(`IAM`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicecatalog-portfolioprincipalassociation-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-portfolioprincipalassociation-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::PortfolioPrincipalAssociation` resource to the intrinsic `Ref` function, the function returns a unique identifier for the association\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.