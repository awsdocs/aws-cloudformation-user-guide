# AWS::ServiceCatalog::CloudFormationProduct<a name="aws-resource-servicecatalog-cloudformationproduct"></a>

Creates the specified product for AWS Service Catalog\. For more information, see [CreateProduct](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateProduct.html) in the *AWS Service Catalog Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-servicecatalog-cloudformationproduct-syntax)
+ [Properties](#aws-resource-servicecatalog-cloudformationproduct-properties)
+ [Return Values](#aws-resource-servicecatalog-cloudformationproduct-returnvalues)

## Syntax<a name="aws-resource-servicecatalog-cloudformationproduct-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-cloudformationproduct-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::CloudFormationProduct",
  "Properties" : {
    "[Owner](#cfn-servicecatalog-cloudformationproduct-owner)" : String,
    "[SupportDescription](#cfn-servicecatalog-cloudformationproduct-supportdescription)" : String,
    "[Description](#cfn-servicecatalog-cloudformationproduct-description)" : String,
    "[Distributor](#cfn-servicecatalog-cloudformationproduct-distributor)" : String,
    "[SupportEmail](#cfn-servicecatalog-cloudformationproduct-supportemail)" : String,
    "[AcceptLanguage](#cfn-servicecatalog-cloudformationproduct-acceptlanguage)" : String,
    "[SupportUrl](#cfn-servicecatalog-cloudformationproduct-supporturl)" : String,
    "[Tags](#cfn-servicecatalog-cloudformationproduct-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ],
    "[Name](#cfn-servicecatalog-cloudformationproduct-name)" : String,
    "[ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters)" : [ [*ProvisioningArtifactProperties*](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md), ... ]
  }
}
```

### YAML<a name="aws-resource-servicecatalog-cloudformationproduct-syntax.yaml"></a>

```
Type: "AWS::ServiceCatalog::CloudFormationProduct"
Properties:
  [Owner](#cfn-servicecatalog-cloudformationproduct-owner): String
  [SupportDescription](#cfn-servicecatalog-cloudformationproduct-supportdescription): String
  [Description](#cfn-servicecatalog-cloudformationproduct-description): String
  [Distributor](#cfn-servicecatalog-cloudformationproduct-distributor): String
  [SupportEmail](#cfn-servicecatalog-cloudformationproduct-supportemail): String
  [AcceptLanguage](#cfn-servicecatalog-cloudformationproduct-acceptlanguage): String
  [SupportUrl](#cfn-servicecatalog-cloudformationproduct-supporturl): String
  [Tags](#cfn-servicecatalog-cloudformationproduct-tags): 
    - [*Resource Tag*](aws-properties-resource-tags.md)
  [Name](#cfn-servicecatalog-cloudformationproduct-name): String
  [ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters): 
    - [*ProvisioningArtifactProperties*](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md)
```

## Properties<a name="aws-resource-servicecatalog-cloudformationproduct-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-cloudformationproduct-acceptlanguage"></a>
The language code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-cloudformationproduct-description"></a>
The description of the product\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Distributor`  <a name="cfn-servicecatalog-cloudformationproduct-distributor"></a>
The distributor of the product\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-servicecatalog-cloudformationproduct-name"></a>
The name of the product\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Owner`  <a name="cfn-servicecatalog-cloudformationproduct-owner"></a>
The owner of the product\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ProvisioningArtifactParameters`  <a name="cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters"></a>
The configuration of the provisioning artifact \(also known as a version\) for a product\.  
*Required*: Yes  
*Type*: List of [AWS Service Catalog CloudFormationProduct ProvisioningArtifactProperties](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SupportDescription`  <a name="cfn-servicecatalog-cloudformationproduct-supportdescription"></a>
The support information about the product\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SupportEmail`  <a name="cfn-servicecatalog-cloudformationproduct-supportemail"></a>
The contact email for product support\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SupportUrl`  <a name="cfn-servicecatalog-cloudformationproduct-supporturl"></a>
The contact URL for product support\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalog-cloudformationproduct-tags"></a>
One or more tags\.  
*Required*: No  
*Type*: List of [*Resource Tag*](aws-properties-resource-tags.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-servicecatalog-cloudformationproduct-returnvalues"></a>

### Ref<a name="aws-resource-servicecatalog-cloudformationproduct-ref"></a>

When you pass the logical ID of an `AWS::ServiceCatalog::CloudFormationProduct` resource to the intrinsic `Ref` function, the function returns the ID of the provisioning artifact, such as `prod-nd24wbqkm4pju`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-servicecatalog-cloudformationproduct-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes\.

`ProductName`  
The name of the product\.

`ProvisioningArtifactIds`  
The IDs of the provisioning artifacts\.

`ProvisioningArtifactNames`  
The names of the provisioning artifacts\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.