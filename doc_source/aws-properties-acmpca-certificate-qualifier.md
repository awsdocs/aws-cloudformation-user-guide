# AWS::ACMPCA::Certificate Qualifier<a name="aws-properties-acmpca-certificate-qualifier"></a>

Defines a `PolicyInformation` qualifier\. AWS Private CA supports the [certification practice statement \(CPS\) qualifier](https://datatracker.ietf.org/doc/html/rfc5280#section-4.2.1.4) defined in RFC 5280\. 

## Syntax<a name="aws-properties-acmpca-certificate-qualifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-qualifier-syntax.json"></a>

```
{
  "[CpsUri](#cfn-acmpca-certificate-qualifier-cpsuri)" : String
}
```

### YAML<a name="aws-properties-acmpca-certificate-qualifier-syntax.yaml"></a>

```
  [CpsUri](#cfn-acmpca-certificate-qualifier-cpsuri): String
```

## Properties<a name="aws-properties-acmpca-certificate-qualifier-properties"></a>

`CpsUri`  <a name="cfn-acmpca-certificate-qualifier-cpsuri"></a>
Contains a pointer to a certification practice statement \(CPS\) published by the CA\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)