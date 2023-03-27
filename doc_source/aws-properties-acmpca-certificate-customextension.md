# AWS::ACMPCA::Certificate CustomExtension<a name="aws-properties-acmpca-certificate-customextension"></a>



Specifies the X\.509 extension information for a certificate\.

Extensions present in `CustomExtensions` follow the `ApiPassthrough` [template rules](https://docs.aws.amazon.com/privateca/latest/userguide/UsingTemplates.html#template-order-of-operations)\. 

## Syntax<a name="aws-properties-acmpca-certificate-customextension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-customextension-syntax.json"></a>

```
{
  "[Critical](#cfn-acmpca-certificate-customextension-critical)" : Boolean,
  "[ObjectIdentifier](#cfn-acmpca-certificate-customextension-objectidentifier)" : String,
  "[Value](#cfn-acmpca-certificate-customextension-value)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-customextension-syntax.yaml"></a>

```
  [Critical](#cfn-acmpca-certificate-customextension-critical): Boolean
  [ObjectIdentifier](#cfn-acmpca-certificate-customextension-objectidentifier): String
  [Value](#cfn-acmpca-certificate-customextension-value): String
```

## Properties<a name="aws-properties-acmpca-certificate-customextension-properties"></a>

`Critical`  <a name="cfn-acmpca-certificate-customextension-critical"></a>
  
Specifies the critical flag of the X\.509 extension\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectIdentifier`  <a name="cfn-acmpca-certificate-customextension-objectidentifier"></a>
  
Specifies the object identifier \(OID\) of the X\.509 extension\. For more information, see the [Global OID reference database\.](https://oidref.com/2.5.29)   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `^([0-2])\.([0-9]|([0-3][0-9]))((\.([0-9]+)){0,126})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-acmpca-certificate-customextension-value"></a>
  
Specifies the base64\-encoded value of the X\.509 extension\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Pattern*: `^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==|[A-Za-z0-9+/]{3}=)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)