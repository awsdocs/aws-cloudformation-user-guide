# AWS::LicenseManager::License ValidityDateFormat<a name="aws-properties-licensemanager-license-validitydateformat"></a>

Date and time range during which the license is valid, in ISO8601\-UTC format\.

## Syntax<a name="aws-properties-licensemanager-license-validitydateformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-validitydateformat-syntax.json"></a>

```
{
  "[Begin](#cfn-licensemanager-license-validitydateformat-begin)" : String,
  "[End](#cfn-licensemanager-license-validitydateformat-end)" : String
}
```

### YAML<a name="aws-properties-licensemanager-license-validitydateformat-syntax.yaml"></a>

```
  [Begin](#cfn-licensemanager-license-validitydateformat-begin): String
  [End](#cfn-licensemanager-license-validitydateformat-end): String
```

## Properties<a name="aws-properties-licensemanager-license-validitydateformat-properties"></a>

`Begin`  <a name="cfn-licensemanager-license-validitydateformat-begin"></a>
Start of the time range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`End`  <a name="cfn-licensemanager-license-validitydateformat-end"></a>
End of the time range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)