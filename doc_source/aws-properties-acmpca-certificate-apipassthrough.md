# AWS::ACMPCA::Certificate ApiPassthrough<a name="aws-properties-acmpca-certificate-apipassthrough"></a>

Contains X\.509 certificate information to be placed in an issued certificate\. An `APIPassthrough` or `APICSRPassthrough` template variant must be selected, or else this parameter is ignored\. 

If conflicting or duplicate certificate information is supplied from other sources, AWS Private CA applies [order of operation rules](https://docs.aws.amazon.com/privateca/latest/userguide/UsingTemplates.html#template-order-of-operations) to determine what information is used\.

## Syntax<a name="aws-properties-acmpca-certificate-apipassthrough-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-apipassthrough-syntax.json"></a>

```
{
  "[Extensions](#cfn-acmpca-certificate-apipassthrough-extensions)" : Extensions,
  "[Subject](#cfn-acmpca-certificate-apipassthrough-subject)" : Subject
}
```

### YAML<a name="aws-properties-acmpca-certificate-apipassthrough-syntax.yaml"></a>

```
  [Extensions](#cfn-acmpca-certificate-apipassthrough-extensions): 
    Extensions
  [Subject](#cfn-acmpca-certificate-apipassthrough-subject): 
    Subject
```

## Properties<a name="aws-properties-acmpca-certificate-apipassthrough-properties"></a>

`Extensions`  <a name="cfn-acmpca-certificate-apipassthrough-extensions"></a>
Specifies X\.509 extension information for a certificate\.  
*Required*: No  
*Type*: [Extensions](aws-properties-acmpca-certificate-extensions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subject`  <a name="cfn-acmpca-certificate-apipassthrough-subject"></a>
Contains information about the certificate subject\. The Subject field in the certificate identifies the entity that owns or controls the public key in the certificate\. The entity can be a user, computer, device, or service\. The Subject must contain an X\.500 distinguished name \(DN\)\. A DN is a sequence of relative distinguished names \(RDNs\)\. The RDNs are separated by commas in the certificate\.   
*Required*: No  
*Type*: [Subject](aws-properties-acmpca-certificate-subject.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)