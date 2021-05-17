# AWS::ACMPCA::Certificate GeneralNameList<a name="aws-properties-acmpca-certificate-generalnamelist"></a>

Describes an ASN\.1 X\.400 `GeneralName` as defined in [RFC 5280](https://tools.ietf.org/html/rfc5280)\. Only one of the following naming options should be provided\. Providing more than one option results in an `InvalidArgsException` error\.

## Syntax<a name="aws-properties-acmpca-certificate-generalnamelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-generalnamelist-syntax.json"></a>

```
{
  "[GeneralNameList](#cfn-acmpca-certificate-generalnamelist-generalnamelist)" : [ GeneralName, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-generalnamelist-syntax.yaml"></a>

```
  [GeneralNameList](#cfn-acmpca-certificate-generalnamelist-generalnamelist): 
    - GeneralName
```

## Properties<a name="aws-properties-acmpca-certificate-generalnamelist-properties"></a>

`GeneralNameList`  <a name="cfn-acmpca-certificate-generalnamelist-generalnamelist"></a>
List of GeneralName objects\.  
*Required*: No  
*Type*: [List](#aws-properties-acmpca-certificate-generalnamelist) of [GeneralName](aws-properties-acmpca-certificate-generalname.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)