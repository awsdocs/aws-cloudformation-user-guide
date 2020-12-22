# AWS::LicenseManager::License IssuerData<a name="aws-properties-licensemanager-license-issuerdata"></a>

Details about the issuer of a license\.

## Syntax<a name="aws-properties-licensemanager-license-issuerdata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-issuerdata-syntax.json"></a>

```
{
  "[Name](#cfn-licensemanager-license-issuerdata-name)" : String,
  "[SignKey](#cfn-licensemanager-license-issuerdata-signkey)" : String
}
```

### YAML<a name="aws-properties-licensemanager-license-issuerdata-syntax.yaml"></a>

```
  [Name](#cfn-licensemanager-license-issuerdata-name): String
  [SignKey](#cfn-licensemanager-license-issuerdata-signkey): String
```

## Properties<a name="aws-properties-licensemanager-license-issuerdata-properties"></a>

`Name`  <a name="cfn-licensemanager-license-issuerdata-name"></a>
Issuer name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SignKey`  <a name="cfn-licensemanager-license-issuerdata-signkey"></a>
Asymmetric CMK from AWS Key Management Service\. The CMK must have a key usage of sign and verify, and support the RSASSA\-PSS SHA\-256 signing algorithm\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)