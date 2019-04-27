# AWS::ServiceCatalog::ResourceUpdateConstraint<a name="aws-resource-servicecatalog-resourceupdateconstraint"></a>

Creates a `RESOURCE_UPDATE` constraint for AWS Service Catalog\. For more information, see [CreateConstraint](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog Developer Guide*\. 

## Syntax<a name="aws-resource-servicecatalog-resourceupdateconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-resourceupdateconstraint-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::ResourceUpdateConstraint",
  "Properties" : {
    "[AcceptLanguage](#cfn-servicecatalog-resourceupdateconstraint-acceptlanguage)" : String,
    "[Description](#cfn-servicecatalog-resourceupdateconstraint-description)" : String,
    "[PortfolioId](#cfn-servicecatalog-resourceupdateconstraint-portfolioid)" : String,
    "[ProductId](#cfn-servicecatalog-resourceupdateconstraint-productid)" : String,
    "[TagUpdateOnProvisionedProduct](#cfn-servicecatalog-resourceupdateconstraint-tagupdateonprovisionedproduct)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-resourceupdateconstraint-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::ResourceUpdateConstraint"
Properties:
  [AcceptLanguage](#cfn-servicecatalog-resourceupdateconstraint-acceptlanguage): String
  [Description](#cfn-servicecatalog-resourceupdateconstraint-description): String
  [PortfolioId](#cfn-servicecatalog-resourceupdateconstraint-portfolioid): String
  [ProductId](#cfn-servicecatalog-resourceupdateconstraint-productid): String
  [TagUpdateOnProvisionedProduct](#cfn-servicecatalog-resourceupdateconstraint-tagupdateonprovisionedproduct): String
```

## Properties<a name="aws-resource-servicecatalog-resourceupdateconstraint-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-resourceupdateconstraint-acceptlanguage"></a>
The language code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-servicecatalog-resourceupdateconstraint-description"></a>
The description of the constraint\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PortfolioId`  <a name="cfn-servicecatalog-resourceupdateconstraint-portfolioid"></a>
The portfolio identifier\. Minimum length of 1\. Maximum length of 100\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ProductId`  <a name="cfn-servicecatalog-resourceupdateconstraint-productid"></a>
The product identifier\. Minimum length of 1\. Maximum length of 100  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TagUpdateOnProvisionedProduct`  <a name="cfn-servicecatalog-resourceupdateconstraint-tagupdateonprovisionedproduct"></a>
Accepts string values of `ALLOWED` and `NOT_ALLOWED`\.   
`ALLOWED` \- Lets users change tags in CloudFormationProvisionedProduct resource\.  
`NOT_ALLOWED` \- Prevents users from changing tags in [CloudFormationProvisionedProduct](aws-resource-servicecatalog-cloudformationprovisionedproduct.md) resource\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-servicecatalog-resourceupdateconstraint-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-resourceupdateconstraint-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::ResourceUpdateConstraint` resource to the intrinsic `Ref` function, the function returns the identifier of the constraint\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-servicecatalog-resourceupdateconstraint-examples"></a>

### <a name="aws-resource-servicecatalog-resourceupdateconstraint-example1"></a>

#### JSON<a name="aws-resource-servicecatalog-resourceupdateconstraint-example1.json"></a>

```
 {
    "Type" : "AWS::ServiceCatalog::ResourceUpdateConstraint",
    "Properties" : {
    "AcceptLanguage" : "en",
    "Description" : "Sample description",
    "PortfolioId" : "port-xxx",
    "ProductId" : "prod-xxx",
    "TagUpdateOnProvisionedProduct" : "ALLOWED"
  }
```

#### YAML<a name="aws-resource-servicecatalog-resourceupdateconstraint-example1.yaml"></a>

```
      Type: 'AWS::ServiceCatalog::ResourceUpdateConstraint'

      Properties:
      
      Description: Sample description
      
      TagUpdateOnProvisionedProduct: 'ALLOWED'
      
      PortfolioId: port-xxx
      
      ProductId: prod-xxx`
```