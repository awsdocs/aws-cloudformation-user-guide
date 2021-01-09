# AWS::LicenseManager::Grant FilterList<a name="aws-properties-licensemanager-grant-filterlist"></a>

A list of filters\.

## Syntax<a name="aws-properties-licensemanager-grant-filterlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-grant-filterlist-syntax.json"></a>

```
{
  "[FilterList](#cfn-licensemanager-grant-filterlist-filterlist)" : [ Filter, ... ]
}
```

### YAML<a name="aws-properties-licensemanager-grant-filterlist-syntax.yaml"></a>

```
  [FilterList](#cfn-licensemanager-grant-filterlist-filterlist): 
    - Filter
```

## Properties<a name="aws-properties-licensemanager-grant-filterlist-properties"></a>

`FilterList`  <a name="cfn-licensemanager-grant-filterlist-filterlist"></a>
A list of filters\.  
*Required*: No  
*Type*: [List](#aws-properties-licensemanager-grant-filterlist) of [Filter](aws-properties-licensemanager-grant-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)