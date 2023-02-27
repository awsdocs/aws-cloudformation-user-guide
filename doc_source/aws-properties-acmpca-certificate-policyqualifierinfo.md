# AWS::ACMPCA::Certificate PolicyQualifierInfo<a name="aws-properties-acmpca-certificate-policyqualifierinfo"></a>

Modifies the `CertPolicyId` of a `PolicyInformation` object with a qualifier\. AWS Private CA supports the certification practice statement \(CPS\) qualifier\.

## Syntax<a name="aws-properties-acmpca-certificate-policyqualifierinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-policyqualifierinfo-syntax.json"></a>

```
{
  "[PolicyQualifierId](#cfn-acmpca-certificate-policyqualifierinfo-policyqualifierid)" : String,
  "[Qualifier](#cfn-acmpca-certificate-policyqualifierinfo-qualifier)" : Qualifier
}
```

### YAML<a name="aws-properties-acmpca-certificate-policyqualifierinfo-syntax.yaml"></a>

```
  [PolicyQualifierId](#cfn-acmpca-certificate-policyqualifierinfo-policyqualifierid): String
  [Qualifier](#cfn-acmpca-certificate-policyqualifierinfo-qualifier): 
    Qualifier
```

## Properties<a name="aws-properties-acmpca-certificate-policyqualifierinfo-properties"></a>

`PolicyQualifierId`  <a name="cfn-acmpca-certificate-policyqualifierinfo-policyqualifierid"></a>
Identifies the qualifier modifying a `CertPolicyId`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CPS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Qualifier`  <a name="cfn-acmpca-certificate-policyqualifierinfo-qualifier"></a>
Defines the qualifier type\. AWS Private CA supports the use of a URI for a CPS qualifier in this field\.  
*Required*: Yes  
*Type*: [Qualifier](aws-properties-acmpca-certificate-qualifier.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)