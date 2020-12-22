# AWS::LicenseManager::License RuleList<a name="aws-properties-licensemanager-license-rulelist"></a>

The `RuleList` property type defines the list of license rules\.

## Syntax<a name="aws-properties-licensemanager-license-rulelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-rulelist-syntax.json"></a>

```
{
  "[RuleList](#cfn-licensemanager-license-rulelist-rulelist)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-licensemanager-license-rulelist-syntax.yaml"></a>

```
  [RuleList](#cfn-licensemanager-license-rulelist-rulelist): 
    - Rule
```

## Properties<a name="aws-properties-licensemanager-license-rulelist-properties"></a>

`RuleList`  <a name="cfn-licensemanager-license-rulelist-rulelist"></a>
The list of license rules\.  
*Required*: No  
*Type*: [List](#aws-properties-licensemanager-license-rulelist) of [Rule](aws-properties-licensemanager-license-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)