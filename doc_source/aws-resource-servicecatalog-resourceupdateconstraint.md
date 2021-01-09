# AWS::ServiceCatalog::ResourceUpdateConstraint<a name="aws-resource-servicecatalog-resourceupdateconstraint"></a>

Specifies a `RESOURCE_UPDATE` constraint\.

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
Type: AWS::ServiceCatalog::ResourceUpdateConstraint
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
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-resourceupdateconstraint-description"></a>
The description of the constraint\.  
*Required*: No  
*Type*: String  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortfolioId`  <a name="cfn-servicecatalog-resourceupdateconstraint-portfolioid"></a>
The portfolio identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProductId`  <a name="cfn-servicecatalog-resourceupdateconstraint-productid"></a>
The product identifier\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagUpdateOnProvisionedProduct`  <a name="cfn-servicecatalog-resourceupdateconstraint-tagupdateonprovisionedproduct"></a>
If set to `ALLOWED`, lets users change tags in a [CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html) resource\.  
If set to `NOT_ALLOWED`, prevents users from changing tags in a [CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html) resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-resourceupdateconstraint-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-resourceupdateconstraint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the identifier of the constraint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-servicecatalog-resourceupdateconstraint--examples"></a>



### Create a RESOURCE\_UPDATE constraint<a name="aws-resource-servicecatalog-resourceupdateconstraint--examples--Create_a_RESOURCE_UPDATE_constraint"></a>

#### JSON<a name="aws-resource-servicecatalog-resourceupdateconstraint--examples--Create_a_RESOURCE_UPDATE_constraint--json"></a>

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

#### YAML<a name="aws-resource-servicecatalog-resourceupdateconstraint--examples--Create_a_RESOURCE_UPDATE_constraint--yaml"></a>

```
Type: 'AWS::ServiceCatalog::ResourceUpdateConstraint'
Properties:
  Description: Sample description
  TagUpdateOnProvisionedProduct: 'ALLOWED'
  PortfolioId: port-xxx
  ProductId: prod-xxx`
```

## See also<a name="aws-resource-servicecatalog-resourceupdateconstraint--seealso"></a>
+ [CreateConstraint](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateConstraint.html) in the *AWS Service Catalog API Reference*

