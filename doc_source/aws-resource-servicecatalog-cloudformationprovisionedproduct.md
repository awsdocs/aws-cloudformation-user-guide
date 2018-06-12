# AWS::ServiceCatalog::CloudFormationProvisionedProduct<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct"></a>

Provisions the specified product for AWS Service Catalog\. For more information, see [ProvisionProduct](http://docs.aws.amazon.com/servicecatalog/latest/dg/API_ProvisionProduct.html) in the *AWS Service Catalog Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax)
+ [Properties](#aws-resource-servicecatalog-cloudformationprovisionedproduct-properties)
+ [Return Values](#aws-resource-servicecatalog-cloudformationprovisionedproduct-returnvalues)

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
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-productname"></a>
The product name\. This name must be unique for the user\. You must specify either the name or the ID of the product, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ProvisionedProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname"></a>
A user\-friendly name for the provisioned product\. This name must be unique for the AWS account and cannot be updated after the product is provisioned\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ProvisioningArtifactId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid"></a>
The identifier of the provisioning artifact\. You must specify either the ID or the name of the provisioning artifact, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProvisioningArtifactName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname"></a>
The name of the provisioning artifact\. This name must be unique for the product\. You must specify either the name or the ID of the provisioning artifact, but not both\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProvisioningParameters`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters"></a>
Parameters specified by the administrator that are required for provisioning the product\.  
 *Required*: No  
 *Type*: List of [AWS Service Catalog CloudFormationProvisionedProduct ProvisioningParameter](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-tags"></a>
One or more tags\.  
 *Required*: No  
 *Type*: List of [ AWS CloudFormation Resource Tags TypeAWS CloudFormation Resource Tags  Applies user\-defined tags to supported resource types by using the Resource Tags property type\.   You can use the AWS CloudFormation Resource Tags property to apply tags to resources, which can help you identify and categorize those resources\. You can tag only resources for which AWS CloudFormation supports tagging\. For information about which resources you can tag with AWS CloudFormation, see the individual resources in [AWS Resource Types Reference](aws-template-resource-type-ref.md)\.  Tagging implementations might vary by resource\. For example, AWS::AutoScaling::AutoScalingGroup provides an additional, required `PropagateAtLaunch` property as part of its tagging scheme\.  In addition to any tags you define, AWS CloudFormation automatically creates the following stack\-level tags with the prefix `aws:`:   `aws:cloudformation:logical-id`   `aws:cloudformation:stack-id`   `aws:cloudformation:stack-name`   All stack\-level tags, including automatically created tags, are propagated to resources that AWS CloudFormation supports\. Currently, tags are not propagated to Amazon EBS volumes that are created from block device mappings\. Syntax JSON 

```
{
  "[Key](#cfn-resource-tags-key)" : String,
  "[Value](#cfn-resource-tags-value)" : String
}
```  YAML 

```
[Key](#cfn-resource-tags-key): String
[Value](#cfn-resource-tags-value): String
```   Properties  

`Key`  <a name="cfn-resource-tags-key"></a>
The key name of the tag\. You can specify a value that is 1 to 127 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: Yes  
*Type*: String 

`Value`  <a name="cfn-resource-tags-value"></a>
The value for the tag\. You can specify a value that is 1 to 255 Unicode characters in length and cannot be prefixed with `aws:`\. You can use any of the following characters: the set of Unicode letters, digits, whitespace, `_`, `.`, `/`, `=`, `+`, and `-`\.  
*Required*: Yes  
*Type*: String    Example  This example shows a `Tags` property\. You specify this property within the `Properties` section of a resource that supports it\. When the resource is created, it is tagged with the tags you declare\. JSON 

```
 1. "Tags" : [
 2.       {
 3.         "Key" : "keyname1",
 4.         "Value" : "value1"
 5.       },
 6.       {
 7.         "Key" : "keyname2",
 8.         "Value" : "value2"
 9.       }
10.     ]
```  YAML 

```
1. Tags: 
2.   - 
3.     Key: "keyname1"
4.     Value: "value1"
5.   - 
6.     Key: "keyname2"
7.     Value: "value2"
```   See Also   [Setting Stack Options](cfn-console-add-tags.md)   [Viewing Stack Data and Resources](cfn-console-view-stack-data-resources.md)    ](aws-properties-resource-tags.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

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