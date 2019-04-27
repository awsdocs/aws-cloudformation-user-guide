# AWS::ServiceCatalog::CloudFormationProvisionedProduct<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct"></a>

Provisions the specified product for AWS Service Catalog\. For more information, see [ProvisionProduct](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_ProvisionProduct.html) in the *AWS Service Catalog Developer Guide*\. 

## Syntax<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::CloudFormationProvisionedProduct",
  "Properties" : {
    "[PathId](#cfn-servicecatalog-cloudformationprovisionedproduct-pathid)" : String,
    "[ProvisioningParameters](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters)" : [ [*ProvisioningParameter*](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter.md), ... ],
    "[ProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-productname)" : String,
    "[ProvisioningArtifactName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname)" : String,
    "[NotificationArns](#cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns)" : [ String, ... ],
    "[AcceptLanguage](#cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage)" : String,
    "[ProductId](#cfn-servicecatalog-cloudformationprovisionedproduct-productid)" : String,
    "[Tags](#cfn-servicecatalog-cloudformationprovisionedproduct-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[ProvisionedProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname)" : String,
    "[ProvisioningArtifactId](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid)" : String
  }
}
```

### YAML<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::CloudFormationProvisionedProduct"
Properties:
  [PathId](#cfn-servicecatalog-cloudformationprovisionedproduct-pathid): String
  [ProvisioningParameters](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters): 
    - [*ProvisioningParameter*](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter.md)
  [ProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-productname): String
  [ProvisioningArtifactName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname): String
  [NotificationArns](#cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns): 
    - String
  [AcceptLanguage](#cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage): String
  [ProductId](#cfn-servicecatalog-cloudformationprovisionedproduct-productid): String
  [Tags](#cfn-servicecatalog-cloudformationprovisionedproduct-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
  [ProvisionedProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname): String
  [ProvisioningArtifactId](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid): String
```

## Properties<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage"></a>
The language code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NotificationArns`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns"></a>
The SNS topic ARNs for stack\-related events\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`PathId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-pathid"></a>
The path identifier of the product\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProductId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-productid"></a>
The product identifier\. You must specify either the ID or the name of the product, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-productname"></a>
The product name\. This name must be unique for the user\. You must specify either the name or the ID of the product, but not both\.  
Each time a stack is created or updated, if `ProductName` is provided it will successfully resolve to `ProductId` as long as only one product exists in the account/region with that `ProductName`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProvisionedProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname"></a>
A user\-friendly name for the provisioned product\. This name must be unique for the AWS account and cannot be updated after the product is provisioned\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ProvisioningArtifactId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid"></a>
The identifier of the provisioning artifact \(also known as a version\) for the product\. You must specify either the ID or the name of the provisioning artifact, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProvisioningArtifactName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname"></a>
The name of the provisioning artifact \(also known as a version\) for the product\. This name must be unique for the product\. You must specify either the name or the ID of the provisioning artifact, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProvisioningParameters`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters"></a>
Parameters specified by the administrator that are required for provisioning the product\.  
 *Required*: No  
 *Type*: List of [ProvisioningParameter](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-tags"></a>
One or more tags\. Requires the provisioned product to have [`RESOURCE_UPDATE`](aws-resource-servicecatalog-resourceupdateconstraint.md) constraint with `TagUpdatesOnProvisionedProduct` set to `ALLOWED` to allow tag updates\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::CloudFormationProvisionedProduct` resource to the intrinsic `Ref` function, the function returns the provisioned product ID, such as `pp-hfyszaotincww`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`CloudformationStackArn`  
The Amazon Resource Name \(ARN\) of the CloudFormation stack, such as `arn:aws:cloudformation:eu-west-1:123456789012:stack/SC-499278721343-pp-hfyszaotincww/8f3df460-346a-11e8-9444-503abe701c29`\. 

`RecordId`  
The ID of the record, such as `rec-rjeatvy434trk`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 