# AWS::ACMPCA::Certificate CertificatePolicyList<a name="aws-properties-acmpca-certificate-certificatepolicylist"></a>

Contains a sequence of one or more policy information terms, each of which consists of an object identifier \(OID\) and optional qualifiers\.

In an end\-entity certificate, these terms indicate the policy under which the certificate was issued and the purposes for which it may be used\. In a CA certificate, these terms limit the set of policies for certification paths that include this certificate\.

## Syntax<a name="aws-properties-acmpca-certificate-certificatepolicylist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-certificatepolicylist-syntax.json"></a>

```
{
  "[CertificatePolicyList](#cfn-acmpca-certificate-certificatepolicylist-certificatepolicylist)" : [ PolicyInformation, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-certificatepolicylist-syntax.yaml"></a>

```
  [CertificatePolicyList](#cfn-acmpca-certificate-certificatepolicylist-certificatepolicylist): 
    - PolicyInformation
```

## Properties<a name="aws-properties-acmpca-certificate-certificatepolicylist-properties"></a>

`CertificatePolicyList`  <a name="cfn-acmpca-certificate-certificatepolicylist-certificatepolicylist"></a>
A list of certificate policies\.  
*Required*: No  
*Type*: [List](#aws-properties-acmpca-certificate-certificatepolicylist) of [PolicyInformation](aws-properties-acmpca-certificate-policyinformation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)