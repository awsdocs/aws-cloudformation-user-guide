# AWS::ACMPCA::Certificate ExtendedKeyUsageList<a name="aws-properties-acmpca-certificate-extendedkeyusagelist"></a>

Specifies additional purposes for which the certified public key may be used other than basic purposes indicated in the `KeyUsage` extension\.

## Syntax<a name="aws-properties-acmpca-certificate-extendedkeyusagelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-extendedkeyusagelist-syntax.json"></a>

```
{
  "[ExtendedKeyUsageList](#cfn-acmpca-certificate-extendedkeyusagelist-extendedkeyusagelist)" : [ ExtendedKeyUsage, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-extendedkeyusagelist-syntax.yaml"></a>

```
  [ExtendedKeyUsageList](#cfn-acmpca-certificate-extendedkeyusagelist-extendedkeyusagelist): 
    - ExtendedKeyUsage
```

## Properties<a name="aws-properties-acmpca-certificate-extendedkeyusagelist-properties"></a>

`ExtendedKeyUsageList`  <a name="cfn-acmpca-certificate-extendedkeyusagelist-extendedkeyusagelist"></a>
List of extended key usage types\.  
*Required*: No  
*Type*: [List](#aws-properties-acmpca-certificate-extendedkeyusagelist) of [ExtendedKeyUsage](aws-properties-acmpca-certificate-extendedkeyusage.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)