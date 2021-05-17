# AWS::ACMPCA::Certificate PolicyQualifierInfoList<a name="aws-properties-acmpca-certificate-policyqualifierinfolist"></a>

Modifies the `CertPolicyId` of a `PolicyInformation` object with a qualifier\. ACM Private CA supports the certification practice statement \(CPS\) qualifier\.

## Syntax<a name="aws-properties-acmpca-certificate-policyqualifierinfolist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-policyqualifierinfolist-syntax.json"></a>

```
{
  "[PolicyQualifierInfoList](#cfn-acmpca-certificate-policyqualifierinfolist-policyqualifierinfolist)" : [ PolicyQualifierInfo, ... ]
}
```

### YAML<a name="aws-properties-acmpca-certificate-policyqualifierinfolist-syntax.yaml"></a>

```
  [PolicyQualifierInfoList](#cfn-acmpca-certificate-policyqualifierinfolist-policyqualifierinfolist): 
    - PolicyQualifierInfo
```

## Properties<a name="aws-properties-acmpca-certificate-policyqualifierinfolist-properties"></a>

`PolicyQualifierInfoList`  <a name="cfn-acmpca-certificate-policyqualifierinfolist-policyqualifierinfolist"></a>
List of PolicyQualifierInfo objects\.  
*Required*: No  
*Type*: [List](#aws-properties-acmpca-certificate-policyqualifierinfolist) of [PolicyQualifierInfo](aws-properties-acmpca-certificate-policyqualifierinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)