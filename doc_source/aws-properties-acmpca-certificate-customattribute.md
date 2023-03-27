# AWS::ACMPCA::Certificate CustomAttribute<a name="aws-properties-acmpca-certificate-customattribute"></a>

Defines the X\.500 relative distinguished name \(RDN\)\.

## Syntax<a name="aws-properties-acmpca-certificate-customattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-customattribute-syntax.json"></a>

```
{
  "[ObjectIdentifier](#cfn-acmpca-certificate-customattribute-objectidentifier)" : String,
  "[Value](#cfn-acmpca-certificate-customattribute-value)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-customattribute-syntax.yaml"></a>

```
  [ObjectIdentifier](#cfn-acmpca-certificate-customattribute-objectidentifier): String
  [Value](#cfn-acmpca-certificate-customattribute-value): String
```

## Properties<a name="aws-properties-acmpca-certificate-customattribute-properties"></a>

`ObjectIdentifier`  <a name="cfn-acmpca-certificate-customattribute-objectidentifier"></a>
Specifies the object identifier \(OID\) of the attribute type of the relative distinguished name \(RDN\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `64`  
*Pattern*: `^([0-2])\.([0-9]|([0-3][0-9]))((\.([0-9]+)){0,126})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-acmpca-certificate-customattribute-value"></a>
  
Specifies the attribute value of relative distinguished name \(RDN\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)