# AWS Certificate Manager Certificate DomainValidationOption<a name="aws-properties-certificatemanager-certificate-domainvalidationoption"></a>

`DomainValidationOption` is a property of the [AWS::CertificateManager::Certificate](aws-resource-certificatemanager-certificate.md) resource that specifies the AWS Certificate Manager \(ACM\) Certificate domain that registrars use to send validation emails\.

## Syntax<a name="w3ab2c21c14d218b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-syntax.json"></a>

```
{
  "[DomainName](#cfn-certificatemanager-certificate-domainvalidationoptions-domainname)" : String,
  "[ValidationDomain](#cfn-certificatemanager-certificate-domainvalidationoptions-validationdomain)" : String
}
```

### YAML<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-syntax.yaml"></a>

```
[DomainName](#cfn-certificatemanager-certificate-domainvalidationoptions-domainname): String
[ValidationDomain](#cfn-certificatemanager-certificate-domainvalidationoptions-validationdomain): String
```

## Properties<a name="w3ab2c21c14d218b7"></a>

`DomainName`  <a name="cfn-certificatemanager-certificate-domainvalidationoptions-domainname"></a>
Fully Qualified Domain Name \(FQDN\) of the Certificate that you are requesting\.  
*Required*: Yes  
*Type*: String

`ValidationDomain`  <a name="cfn-certificatemanager-certificate-domainvalidationoptions-validationdomain"></a>
The domain that domain name registrars use to send validation emails\. Registrars use this value as the email address suffix when sending emails to verify your identity\. This value must be the same as the domain name or a superdomain of the domain name\. For more information, see the `ValidationDomain` content for the [DomainValidationOption](http://docs.aws.amazon.com/acm/latest/APIReference/API_DomainValidationOption.html) data type in the *AWS Certificate Manager API Reference*\.  
*Required*: Yes  
*Type*: String