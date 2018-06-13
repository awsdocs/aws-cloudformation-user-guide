# AWS::SES::ConfigurationSet<a name="aws-resource-ses-configurationset"></a>

The `AWS::SES::ConfigurationSet` resource let syou create groups of rules that you can apply to the emails you send using Amazon SES\. For more information about using configuration sets, see [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*\.

Configuration sets 

**Topics**
+ [Syntax](#aws-resource-ses-configurationset-syntax)
+ [Properties](#aws-resource-ses-configurationset-properties)
+ [Example](#aws-resource-ses-configurationset-examples)
+ [See Also](#aws-resource-ses-configurationset-seealso)

## Syntax<a name="aws-resource-ses-configurationset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-configurationset-syntax.json"></a>

```
{
  "Type" : "AWS::SES::ConfigurationSet",
  "Properties" : {
    "[Name](#cfn-ses-configurationset-name)" : String
  }
}
```

### YAML<a name="aws-resource-ses-configurationset-syntax.yaml"></a>

```
Type: "AWS::SES::ConfigurationSet"
Properties:
  [Name](#cfn-ses-configurationset-name): String
```

## Properties<a name="aws-resource-ses-configurationset-properties"></a>

`Name`  <a name="cfn-ses-configurationset-name"></a>
The name of the configuration set\. The name must meet the following requirements:  
+ Contain only letters \(a\-z, A\-Z\), numbers \(0\-9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 64 characters or fewer\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Example<a name="aws-resource-ses-configurationset-examples"></a>

### <a name="aws-resource-ses-configurationset-example1"></a>

#### JSON<a name="aws-resource-ses-configurationset-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS SES ConfigurationSet Sample Template",
    "Parameters": {
        "ConfigSetName": {
            "Type": "String"
        }
    },
    "Resources": {
        "ConfigSet": {
            "Type": "AWS::SES::ConfigurationSet",
            "Properties": {
                "Name": {
                    "Ref": "ConfigSetName"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ses-configurationset-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: "AWS SES ConfigurationSet Sample Template"
Parameters:
  ConfigSetName:
    Type: String
Resources:
  ConfigSet:
    Type: "AWS::SES::ConfigurationSet"
    Properties:
      Name: !Ref ConfigSetName
```

## See Also<a name="aws-resource-ses-configurationset-seealso"></a>
+ [Using Amazon SES Configuration Sets](url-ses-dev;using-configuration-sets.html) in the *Amazon Simple Email Service Developer Guide*
+ [ConfigurationSet](url-ses-api;API_ConfigurationSet.html) in the *Amazon Simple Email Service API Reference*