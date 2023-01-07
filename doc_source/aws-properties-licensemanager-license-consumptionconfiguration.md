# AWS::LicenseManager::License ConsumptionConfiguration<a name="aws-properties-licensemanager-license-consumptionconfiguration"></a>

Details about a consumption configuration\.

## Syntax<a name="aws-properties-licensemanager-license-consumptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-consumptionconfiguration-syntax.json"></a>

```
{
  "[BorrowConfiguration](#cfn-licensemanager-license-consumptionconfiguration-borrowconfiguration)" : BorrowConfiguration,
  "[ProvisionalConfiguration](#cfn-licensemanager-license-consumptionconfiguration-provisionalconfiguration)" : ProvisionalConfiguration,
  "[RenewType](#cfn-licensemanager-license-consumptionconfiguration-renewtype)" : String
}
```

### YAML<a name="aws-properties-licensemanager-license-consumptionconfiguration-syntax.yaml"></a>

```
  [BorrowConfiguration](#cfn-licensemanager-license-consumptionconfiguration-borrowconfiguration): 
    BorrowConfiguration
  [ProvisionalConfiguration](#cfn-licensemanager-license-consumptionconfiguration-provisionalconfiguration): 
    ProvisionalConfiguration
  [RenewType](#cfn-licensemanager-license-consumptionconfiguration-renewtype): String
```

## Properties<a name="aws-properties-licensemanager-license-consumptionconfiguration-properties"></a>

`BorrowConfiguration`  <a name="cfn-licensemanager-license-consumptionconfiguration-borrowconfiguration"></a>
Details about a borrow configuration\.  
*Required*: No  
*Type*: [BorrowConfiguration](aws-properties-licensemanager-license-borrowconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisionalConfiguration`  <a name="cfn-licensemanager-license-consumptionconfiguration-provisionalconfiguration"></a>
Details about a provisional configuration\.  
*Required*: No  
*Type*: [ProvisionalConfiguration](aws-properties-licensemanager-license-provisionalconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RenewType`  <a name="cfn-licensemanager-license-consumptionconfiguration-renewtype"></a>
Renewal frequency\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)