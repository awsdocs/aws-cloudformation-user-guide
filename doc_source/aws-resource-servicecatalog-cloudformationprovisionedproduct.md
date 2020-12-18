# AWS::ServiceCatalog::CloudFormationProvisionedProduct<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct"></a>

Provisions the specified product\.

A provisioned product is a resourced instance of a product\. For example, provisioning a product based on a CloudFormation template launches a CloudFormation stack and its underlying resources\. You can check the status of this request using [DescribeRecord](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_DescribeRecord.html)\.

If the request contains a tag key with an empty list of values, there is a tag conflict for that key\. Do not include conflicted keys as tags, or this causes the error "Parameter validation failed: Missing required parameter in Tags\[*N*\]:*Value*"\.

## Syntax<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::CloudFormationProvisionedProduct",
  "Properties" : {
      "[AcceptLanguage](#cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage)" : String,
      "[NotificationArns](#cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns)" : [ String, ... ],
      "[PathId](#cfn-servicecatalog-cloudformationprovisionedproduct-pathid)" : String,
      "[PathName](#cfn-servicecatalog-cloudformationprovisionedproduct-pathname)" : String,
      "[ProductId](#cfn-servicecatalog-cloudformationprovisionedproduct-productid)" : String,
      "[ProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-productname)" : String,
      "[ProvisionedProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname)" : String,
      "[ProvisioningArtifactId](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid)" : String,
      "[ProvisioningArtifactName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname)" : String,
      "[ProvisioningParameters](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters)" : [ ProvisioningParameter, ... ],
      "[ProvisioningPreferences](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences)" : ProvisioningPreferences,
      "[Tags](#cfn-servicecatalog-cloudformationprovisionedproduct-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::CloudFormationProvisionedProduct
Properties: 
  [AcceptLanguage](#cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage): String
  [NotificationArns](#cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns): 
    - String
  [PathId](#cfn-servicecatalog-cloudformationprovisionedproduct-pathid): String
  [PathName](#cfn-servicecatalog-cloudformationprovisionedproduct-pathname): String
  [ProductId](#cfn-servicecatalog-cloudformationprovisionedproduct-productid): String
  [ProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-productname): String
  [ProvisionedProductName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname): String
  [ProvisioningArtifactId](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid): String
  [ProvisioningArtifactName](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname): String
  [ProvisioningParameters](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters): 
    - ProvisioningParameter
  [ProvisioningPreferences](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences): 
    ProvisioningPreferences
  [Tags](#cfn-servicecatalog-cloudformationprovisionedproduct-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-properties"></a>

`AcceptLanguage`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-acceptlanguage"></a>
The language code\.  
+  `en` \- English \(default\)
+  `jp` \- Japanese
+  `zh` \- Chinese
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationArns`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-notificationarns"></a>
Passed to CloudFormation\. The SNS topic ARNs to which to publish stack\-related events\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PathId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-pathid"></a>
The path identifier of the product\. This value is optional if the product has a default path, and required if the product has more than one path\. To list the paths for a product, use [ListLaunchPaths](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_ListLaunchPaths.html)\.  
You must provide the name or ID, but not both\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-pathname"></a>
The name of the path\. This value is optional if the product has a default path, and required if the product has more than one path\. To list the paths for a product, use [ListLaunchPaths](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_ListLaunchPaths.html)\.  
You must provide the name or ID, but not both\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-productid"></a>
The product identifier\.  
You must specify either the ID or the name of the product, but not both\.
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-productname"></a>
A user\-friendly name for the provisioned product\. This value must be unique for the AWS account and cannot be updated after the product is provisioned\.  
Each time a stack is created or updated, if `ProductName` is provided it will successfully resolve to `ProductId` as long as only one product exists in the account/region with that `ProductName`\.  
You must specify either the name or the ID of the product, but not both\.
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9._-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisionedProductName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisionedproductname"></a>
A user\-friendly name for the provisioned product\. This value must be unique for the AWS account and cannot be updated after the product is provisioned\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9._-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisioningArtifactId`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactid"></a>
The identifier of the provisioning artifact \(also known as a version\)\.  
You must specify either the ID or the name of the provisioning artifact, but not both\.
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisioningArtifactName`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningartifactname"></a>
The name of the provisioning artifact \(also known as a version\) for the product\. This name must be unique for the product\.  
You must specify either the name or the ID of the provisioning artifact, but not both\.
*Required*: Conditional  
*Type*: String  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisioningParameters`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningparameters"></a>
Parameters specified by the administrator that are required for provisioning the product\.  
*Required*: No  
*Type*: List of [ProvisioningParameter](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisioningPreferences`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences"></a>
 StackSet preferences that are required for provisioning the product or updating a provisioned product\.   
*Required*: No  
*Type*: [ProvisioningPreferences](aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-tags"></a>
One or more tags\.  
Requires the provisioned product to have an [ResourceUpdateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-resourceupdateconstraint.html) resource with `TagUpdatesOnProvisionedProduct` set to `ALLOWED` to allow tag updates\. If `RESOURCE_UPDATE` constraint is not present, tags updates are ignored\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the provisioned product ID, such as `pp-hfyszaotincww`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicecatalog-cloudformationprovisionedproduct-return-values-fn--getatt-fn--getatt"></a>

`CloudformationStackArn`  <a name="CloudformationStackArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the CloudFormation stack, such as `arn:aws:cloudformation:eu-west-1:123456789012:stack/SC-499278721343-pp-hfyszaotincww/8f3df460-346a-11e8-9444-503abe701c29`\.

`Outputs`  <a name="Outputs-fn::getatt"></a>
The output of the product you are provisioning\. For example, the DNS of an EC2 instance\.

`ProvisionedProductId`  <a name="ProvisionedProductId-fn::getatt"></a>
The ID of the provisioned product\.

`RecordId`  <a name="RecordId-fn::getatt"></a>
The ID of the record, such as `rec-rjeatvy434trk`\.

## Examples<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct--examples"></a>



### GetAtt Example<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct--examples--GetAtt_Example"></a>

#### YAML<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct--examples--GetAtt_Example--yaml"></a>

```
      AWSTemplateFormatVersion: '2010-09-09'
      Description: Serverless Stack
      Resources:
         SimpleLambda:
           Type: AWS::ServiceCatalog::CloudFormationProvisionedProduct
           Properties:
            ProductName: Basic Lambda
            ProvisioningArtifactName: '1.0'
            
         SimpleApiGateway:
           Type: AWS::ServiceCatalog::CloudFormationProvisionedProduct
           Properties:
            ProductName: API Gateway
            ProvisioningArtifactName: '1.0'
            ProvisioningParameters:
               -
                  Key: LambdaArn
                  Value: !GetAtt [SimpleLambda, Outputs.SCLambdaArn]
```

## See also<a name="aws-resource-servicecatalog-cloudformationprovisionedproduct--seealso"></a>
+ [ProvisionProduct](https://docs.aws.amazon.com/servicecatalog/latest/dg/API_ProvisionProduct.html) in the *AWS Service Catalog API Reference*

