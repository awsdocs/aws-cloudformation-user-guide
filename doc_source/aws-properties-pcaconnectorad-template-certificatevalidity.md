# AWS::PCAConnectorAD::Template CertificateValidity<a name="aws-properties-pcaconnectorad-template-certificatevalidity"></a>

Information describing the end of the validity period of the certificate\. This parameter sets the “Not After” date for the certificate\. Certificate validity is the period of time during which a certificate is valid\. Validity can be expressed as an explicit date and time when the certificate expires, or as a span of time after issuance, stated in days, months, or years\. For more information, see Validity in RFC 5280\. This value is unaffected when ValidityNotBefore is also specified\. For example, if Validity is set to 20 days in the future, the certificate will expire 20 days from issuance time regardless of the ValidityNotBefore value\.

## Syntax<a name="aws-properties-pcaconnectorad-template-certificatevalidity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-certificatevalidity-syntax.json"></a>

```
{
  "[RenewalPeriod](#cfn-pcaconnectorad-template-certificatevalidity-renewalperiod)" : ValidityPeriod,
  "[ValidityPeriod](#cfn-pcaconnectorad-template-certificatevalidity-validityperiod)" : ValidityPeriod
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-certificatevalidity-syntax.yaml"></a>

```
  [RenewalPeriod](#cfn-pcaconnectorad-template-certificatevalidity-renewalperiod): 
    ValidityPeriod
  [ValidityPeriod](#cfn-pcaconnectorad-template-certificatevalidity-validityperiod): 
    ValidityPeriod
```

## Properties<a name="aws-properties-pcaconnectorad-template-certificatevalidity-properties"></a>

`RenewalPeriod`  <a name="cfn-pcaconnectorad-template-certificatevalidity-renewalperiod"></a>
Renewal period is the period of time before certificate expiration when a new certificate will be requested\.  
*Required*: Yes  
*Type*: [ValidityPeriod](aws-properties-pcaconnectorad-template-validityperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidityPeriod`  <a name="cfn-pcaconnectorad-template-certificatevalidity-validityperiod"></a>
Information describing the end of the validity period of the certificate\. This parameter sets the “Not After” date for the certificate\. Certificate validity is the period of time during which a certificate is valid\. Validity can be expressed as an explicit date and time when the certificate expires, or as a span of time after issuance, stated in days, months, or years\. For more information, see Validity in RFC 5280\. This value is unaffected when ValidityNotBefore is also specified\. For example, if Validity is set to 20 days in the future, the certificate will expire 20 days from issuance time regardless of the ValidityNotBefore value\.  
*Required*: Yes  
*Type*: [ValidityPeriod](aws-properties-pcaconnectorad-template-validityperiod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)