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
      "[ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters)" : [ [ProvisioningArtifactProperties](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md), ... ],
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
  [ProvisioningArtifactParameters](#cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters): 
    - [ProvisioningArtifactProperties](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md)
  [SupportDescription](#cfn-servicecatalog-cloudformationproduct-supportdescription): String
  [SupportEmail](#cfn-servicecatalog-cloudformationproduct-supportemail): String
  [SupportUrl](#cfn-servicecatalog-cloudformationproduct-supporturl): String
  [Tags](#cfn-servicecatalog-cloudformationproduct-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicecatalog-cloudformationproduct-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-cloudformationproduct-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
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

`ProvisioningArtifactParameters`  <a name="cfn-servicecatalog-cloudformationproduct-provisioningartifactparameters"></a>
The configuration of the provisioning artifact \(also known as a version\)\.  
*Required*: Yes  
*Type*: List of [ProvisioningArtifactProperties](aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.md)  
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

## Return Values<a name="aws-resource-servicecatalog-cloudformationproduct-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-cloudformationproduct-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the provisioning artifact, such as `prod-nd24wbqkm4pju`\.

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

## See Also<a name="aws-resource-servicecatalog-cloudformationproduct--seealso"></a>
+ [CreateProduct](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_CreateProduct.html) in the *AWS Service Catalog API Reference*