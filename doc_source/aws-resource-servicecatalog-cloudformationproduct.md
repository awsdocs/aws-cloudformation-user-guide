# AWS::ServiceCatalog::CloudFormationProduct<a name="aws-resource-servicecatalog-cloudformationproduct"></a>

Specifies a product\.

## Syntax<a name="aws-resource-servicecatalog-cloudformationproduct-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-cloudformationproduct-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::CloudFormationProduct",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-cloudformationproduct-acceptlanguage)" : String,
      "[Description](#cfn-servicecatalog-cloudformationproduct-description)" : String,
      "[Distributor](#cfn-servicecatalog-cloudformationproduct-distributor)" : String,
      "[Name](#cfn-servicecatalog-cloudformationproduct-name)" : String,
      "[Owner](#cfn-servicecatalog-cloudformationproduct-owner)" : String,
      "[ProductType](#cfn-servicecatalog-cloudformationproduct-producttype)" : String,
      "[ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters)" : [ ProvisioningArtifactProperties, ... ],
      "[ReplaceProvisioningArtifacts](#cfn-servicecatalog-cloudformationproduct-replaceprovisioningartifacts)" : Boolean,
      "[SourceConnection](#cfn-servicecatalog-cloudformationproduct-sourceconnection)" : SourceConnection,
      "[SupportDescription](#cfn-servicecatalog-cloudformationproduct-supportdescription)" : String,
      "[SupportEmail](#cfn-servicecatalog-cloudformationproduct-supportemail)" : String,
      "[SupportUrl](#cfn-servicecatalog-cloudformationproduct-supporturl)" : String,
      "[Tags](#cfn-servicecatalog-cloudformationproduct-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-servicecatalog-cloudformationproduct-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::CloudFormationProduct
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-cloudformationproduct-acceptlanguage): String
  [Description](#cfn-servicecatalog-cloudformationproduct-description): String
  [Distributor](#cfn-servicecatalog-cloudformationproduct-distributor): String
  [Name](#cfn-servicecatalog-cloudformationproduct-name): String
  [Owner](#cfn-servicecatalog-cloudformationproduct-owner): String
  [ProductType](#cfn-servicecatalog-cloudformationproduct-producttype): String
  [ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters): 
    - ProvisioningArtifactProperties
  [ReplaceProvisioningArtifacts](#cfn-servicecatalog-cloudformationproduct-replaceprovisioningartifacts): Boolean
  [SourceConnection](#cfn-servicecatalog-cloudformationproduct-sourceconnection): 
    SourceConnection
  [SupportDescription](#cfn-servicecatalog-cloudformationproduct-supportdescription): String
  [SupportEmail](#cfn-servicecatalog-cloudformationproduct-supportemail): String
  [SupportUrl](#cfn-servicecatalog-cloudformationproduct-supporturl): String
  [Tags](#cfn-servicecatalog-cloudformationproduct-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicecatalog-cloudformationproduct-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-cloudformationproduct-acceptlanguage"></a>
The language code\.  
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-servicecatalog-cloudformationproduct-description"></a>
The description of the product\.  
*Required*: No  
*Type*: String  
*Maximum*: `8191`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Distributor`  <a name="cfn-servicecatalog-cloudformationproduct-distributor"></a>
The distributor of the product\.  
*Required*: No  
*Type*: String  
*Maximum*: `8191`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-servicecatalog-cloudformationproduct-name"></a>
The name of the product\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `8191`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Owner`  <a name="cfn-servicecatalog-cloudformationproduct-owner"></a>
The owner of the product\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `8191`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductType`  <a name="cfn-servicecatalog-cloudformationproduct-producttype"></a>
The type of product\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CLOUD_FORMATION_TEMPLATE | MARKETPLACE | TERRAFORM_OPEN_SOURCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisioningArtifactParameters`  <a name="cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters"></a>
The configuration of the provisioning artifact \(also known as a version\)\.  
*Required*: No  
*Type*: List of [ProvisioningArtifactProperties](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplaceProvisioningArtifacts`  <a name="cfn-servicecatalog-cloudformationproduct-replaceprovisioningartifacts"></a>
This property is turned off by default\. If turned off, you can update provisioning artifacts or product attributes \(such as description, distributor, name, owner, and more\) and the associated provisioning artifacts will retain the same unique identifier\. Provisioning artifacts are matched within the CloudFormationProduct resource, and only those that have been updated will be changed\. Provisioning artifacts are matched by a combinaton of provisioning artifact template URL and name\.  
If turned on, provisioning artifacts will be given a new unique identifier when you update the product or provisioning artifacts\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceConnection`  <a name="cfn-servicecatalog-cloudformationproduct-sourceconnection"></a>
A top level `ProductViewDetail` response containing details about the product’s connection\. AWS Service Catalog returns this field for the `CreateProduct`, `UpdateProduct`, `DescribeProductAsAdmin`, and `SearchProductAsAdmin` APIs\. This response contains the same fields as the `ConnectionParameters` request, with the addition of the `LastSync` response\.  
*Required*: No  
*Type*: [SourceConnection](aws-properties-servicecatalog-cloudformationproduct-sourceconnection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportDescription`  <a name="cfn-servicecatalog-cloudformationproduct-supportdescription"></a>
The support information about the product\.  
*Required*: No  
*Type*: String  
*Maximum*: `8191`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportEmail`  <a name="cfn-servicecatalog-cloudformationproduct-supportemail"></a>
The contact email for product support\.  
*Required*: No  
*Type*: String  
*Maximum*: `254`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SupportUrl`  <a name="cfn-servicecatalog-cloudformationproduct-supporturl"></a>
The contact URL for product support\.  
 `^https?:\/\// `/ is the pattern used to validate SupportUrl\.  
*Required*: No  
*Type*: String  
*Maximum*: `2083`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalog-cloudformationproduct-tags"></a>
One or more tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-cloudformationproduct-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-cloudformationproduct-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the provisioning artifact, such as `pa-3mc34fbybfmgp`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicecatalog-cloudformationproduct-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicecatalog-cloudformationproduct-return-values-fn--getatt-fn--getatt"></a>

`ProductName`  <a name="ProductName-fn::getatt"></a>
The name of the product\.

`ProvisioningArtifactIds`  <a name="ProvisioningArtifactIds-fn::getatt"></a>
The IDs of the provisioning artifacts\.

`ProvisioningArtifactNames`  <a name="ProvisioningArtifactNames-fn::getatt"></a>
The names of the provisioning artifacts\.

## See also<a name="aws-resource-servicecatalog-cloudformationproduct--seealso"></a>
+ [CreateProduct](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateProduct.html) in the *AWS Service Catalog API Reference*

