# AWS::LicenseManager::License FilterList<a name="aws-properties-licensemanager-license-filterlist"></a>

Filters to scope the results\. The following filters are supported:
+  `Beneficiary` 
+  `ProductSKU` 
+  `KeyFingerprint` 
+  `Status` 

## Syntax<a name="aws-properties-licensemanager-license-filterlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-filterlist-syntax.json"></a>

```
{
  "[FilterList](#cfn-licensemanager-license-filterlist-filterlist)" : [ Filter, ... ]
}
```

### YAML<a name="aws-properties-licensemanager-license-filterlist-syntax.yaml"></a>

```
  [FilterList](#cfn-licensemanager-license-filterlist-filterlist): 
    - Filter
```

## Properties<a name="aws-properties-licensemanager-license-filterlist-properties"></a>

`FilterList`  <a name="cfn-licensemanager-license-filterlist-filterlist"></a>
Filters to scope the results\. The following filters are supported:  
+  `Beneficiary` 
+  `ProductSKU` 
+  `KeyFingerprint` 
+  `Status` 
*Required*: No  
*Type*: [List](#aws-properties-licensemanager-license-filterlist) of [Filter](aws-properties-licensemanager-license-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)