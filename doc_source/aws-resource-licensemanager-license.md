# AWS::LicenseManager::License<a name="aws-resource-licensemanager-license"></a>

Specifies a granted license\.

Granted licenses are licenses for products that your organization purchased from AWS Marketplace or directly from a seller who integrated their software with managed entitlements\. For more information, see [Granted licenses](https://docs.aws.amazon.com/license-manager/latest/userguide/granted-licenses.html) in the *AWS License Manager User Guide*\.

## Syntax<a name="aws-resource-licensemanager-license-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-licensemanager-license-syntax.json"></a>

```
{
  "Type" : "AWS::LicenseManager::License",
  "Properties" : {
      "[Beneficiary](#cfn-licensemanager-license-beneficiary)" : String,
      "[ClientToken](#cfn-licensemanager-license-clienttoken)" : String,
      "[ConsumptionConfiguration](#cfn-licensemanager-license-consumptionconfiguration)" : ConsumptionConfiguration,
      "[Entitlements](#cfn-licensemanager-license-entitlements)" : EntitlementList,
      "[Filters](#cfn-licensemanager-license-filters)" : FilterList,
      "[HomeRegion](#cfn-licensemanager-license-homeregion)" : String,
      "[Issuer](#cfn-licensemanager-license-issuer)" : IssuerData,
      "[LicenseArns](#cfn-licensemanager-license-licensearns)" : ArnList,
      "[LicenseMetadata](#cfn-licensemanager-license-licensemetadata)" : MetadataList,
      "[LicenseName](#cfn-licensemanager-license-licensename)" : String,
      "[MaxResults](#cfn-licensemanager-license-maxresults)" : Integer,
      "[NextToken](#cfn-licensemanager-license-nexttoken)" : String,
      "[ProductName](#cfn-licensemanager-license-productname)" : String,
      "[ProductSKU](#cfn-licensemanager-license-productsku)" : String,
      "[SourceVersion](#cfn-licensemanager-license-sourceversion)" : String,
      "[Status](#cfn-licensemanager-license-status)" : String,
      "[Tags](#cfn-licensemanager-license-tags)" : TagList,
      "[Validity](#cfn-licensemanager-license-validity)" : ValidityDateFormat,
      "[Version](#cfn-licensemanager-license-version)" : String
    }
}
```

### YAML<a name="aws-resource-licensemanager-license-syntax.yaml"></a>

```
Type: AWS::LicenseManager::License
Properties: 
  [Beneficiary](#cfn-licensemanager-license-beneficiary): String
  [ClientToken](#cfn-licensemanager-license-clienttoken): String
  [ConsumptionConfiguration](#cfn-licensemanager-license-consumptionconfiguration): 
    ConsumptionConfiguration
  [Entitlements](#cfn-licensemanager-license-entitlements): 
    EntitlementList
  [Filters](#cfn-licensemanager-license-filters): 
    FilterList
  [HomeRegion](#cfn-licensemanager-license-homeregion): String
  [Issuer](#cfn-licensemanager-license-issuer): 
    IssuerData
  [LicenseArns](#cfn-licensemanager-license-licensearns): 
    ArnList
  [LicenseMetadata](#cfn-licensemanager-license-licensemetadata): 
    MetadataList
  [LicenseName](#cfn-licensemanager-license-licensename): String
  [MaxResults](#cfn-licensemanager-license-maxresults): Integer
  [NextToken](#cfn-licensemanager-license-nexttoken): String
  [ProductName](#cfn-licensemanager-license-productname): String
  [ProductSKU](#cfn-licensemanager-license-productsku): String
  [SourceVersion](#cfn-licensemanager-license-sourceversion): String
  [Status](#cfn-licensemanager-license-status): String
  [Tags](#cfn-licensemanager-license-tags): 
    TagList
  [Validity](#cfn-licensemanager-license-validity): 
    ValidityDateFormat
  [Version](#cfn-licensemanager-license-version): String
```

## Properties<a name="aws-resource-licensemanager-license-properties"></a>

`Beneficiary`  <a name="cfn-licensemanager-license-beneficiary"></a>
License beneficiary\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientToken`  <a name="cfn-licensemanager-license-clienttoken"></a>
Unique, case\-sensitive identifier that you provide to ensure the idempotency of the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConsumptionConfiguration`  <a name="cfn-licensemanager-license-consumptionconfiguration"></a>
Configuration for consumption of the license\.  
*Required*: Yes  
*Type*: [ConsumptionConfiguration](aws-properties-licensemanager-license-consumptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Entitlements`  <a name="cfn-licensemanager-license-entitlements"></a>
License entitlements\.  
*Required*: Yes  
*Type*: [EntitlementList](aws-properties-licensemanager-license-entitlementlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filters`  <a name="cfn-licensemanager-license-filters"></a>
Filters to scope the results\. The following filters are supported:  
+  `Beneficiary` 
+  `ProductSKU` 
+  `KeyFingerprint` 
+  `Status` 
*Required*: No  
*Type*: [FilterList](aws-properties-licensemanager-license-filterlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeRegion`  <a name="cfn-licensemanager-license-homeregion"></a>
Home Region of the license\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Issuer`  <a name="cfn-licensemanager-license-issuer"></a>
License issuer\.  
*Required*: Yes  
*Type*: [IssuerData](aws-properties-licensemanager-license-issuerdata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseArns`  <a name="cfn-licensemanager-license-licensearns"></a>
Amazon Resource Names \(ARNs\) of the licenses\.  
*Required*: No  
*Type*: [ArnList](aws-properties-licensemanager-license-arnlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseMetadata`  <a name="cfn-licensemanager-license-licensemetadata"></a>
License metadata\.  
*Required*: No  
*Type*: [MetadataList](aws-properties-licensemanager-license-metadatalist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseName`  <a name="cfn-licensemanager-license-licensename"></a>
License name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxResults`  <a name="cfn-licensemanager-license-maxresults"></a>
Maximum number of results to return in a single call\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextToken`  <a name="cfn-licensemanager-license-nexttoken"></a>
Token for the next set of results\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductName`  <a name="cfn-licensemanager-license-productname"></a>
Product name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductSKU`  <a name="cfn-licensemanager-license-productsku"></a>
Product SKU\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceVersion`  <a name="cfn-licensemanager-license-sourceversion"></a>
License version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-licensemanager-license-status"></a>
License status\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-licensemanager-license-tags"></a>
One or more tags\.  
*Required*: No  
*Type*: [TagList](aws-properties-licensemanager-license-taglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Validity`  <a name="cfn-licensemanager-license-validity"></a>
Date and time range during which the license is valid, in ISO8601\-UTC format\.  
*Required*: Yes  
*Type*: [ValidityDateFormat](aws-properties-licensemanager-license-validitydateformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-licensemanager-license-version"></a>
License version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-licensemanager-license-return-values"></a>

### Ref<a name="aws-resource-licensemanager-license-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the license\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-licensemanager-license-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-licensemanager-license-return-values-fn--getatt-fn--getatt"></a>

`LicenseArn`  <a name="LicenseArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the license\.