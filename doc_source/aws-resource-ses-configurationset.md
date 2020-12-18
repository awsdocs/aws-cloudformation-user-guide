# AWS::SES::ConfigurationSet<a name="aws-resource-ses-configurationset"></a>

Specifies a configuration set\. Configuration sets let you create groups of rules that you can apply to the emails you send using Amazon SES\. For more information about using configuration sets, see [Using Amazon SES Configuration Sets](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/using-configuration-sets.html) in the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/)\.

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
Type: AWS::SES::ConfigurationSet
Properties: 
  [Name](#cfn-ses-configurationset-name): String
```

## Properties<a name="aws-resource-ses-configurationset-properties"></a>

`Name`  <a name="cfn-ses-configurationset-name"></a>
The name of the configuration set\. The name must:  
+ Only contain ASCII letters \(a–z, A–Z\), numbers \(0–9\), underscores \(\_\), or dashes \(\-\)\.
+ Contain 64 characters or fewer\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ses-configurationset-return-values"></a>

### Ref<a name="aws-resource-ses-configurationset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ses-configurationset--examples"></a>



### <a name="aws-resource-ses-configurationset--examples--"></a>

Specifies a configuration set\.

#### JSON<a name="aws-resource-ses-configurationset--examples----json"></a>

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

#### YAML<a name="aws-resource-ses-configurationset--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS SES ConfigurationSet Sample Template
Parameters:
  ConfigSetName:
    Type: String
Resources:
  ConfigSet:
    Type: 'AWS::SES::ConfigurationSet'
    Properties:
      Name: !Ref ConfigSetName
```