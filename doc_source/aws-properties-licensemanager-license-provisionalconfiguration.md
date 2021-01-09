# AWS::LicenseManager::License ProvisionalConfiguration<a name="aws-properties-licensemanager-license-provisionalconfiguration"></a>

Details about a provisional configuration\.

## Syntax<a name="aws-properties-licensemanager-license-provisionalconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-provisionalconfiguration-syntax.json"></a>

```
{
  "[MaxTimeToLiveInMinutes](#cfn-licensemanager-license-provisionalconfiguration-maxtimetoliveinminutes)" : Integer
}
```

### YAML<a name="aws-properties-licensemanager-license-provisionalconfiguration-syntax.yaml"></a>

```
  [MaxTimeToLiveInMinutes](#cfn-licensemanager-license-provisionalconfiguration-maxtimetoliveinminutes): Integer
```

## Properties<a name="aws-properties-licensemanager-license-provisionalconfiguration-properties"></a>

`MaxTimeToLiveInMinutes`  <a name="cfn-licensemanager-license-provisionalconfiguration-maxtimetoliveinminutes"></a>
Maximum time for the provisional configuration, in minutes\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)