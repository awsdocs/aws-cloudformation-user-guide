# AWS::CertificateManager::Certificate<a name="aws-resource-certificatemanager-certificate"></a>

The `AWS::CertificateManager::Certificate` resource requests an AWS Certificate Manager \(ACM\) certificate that you can use with AWS services to enable secure connections\. For example, you can deploy an ACM certificate to an Elastic Load Balancing load balancer to enable HTTPS support\. For more information, see the `[RequestCertificate](https://docs.aws.amazon.com/acm/latest/APIReference/API_RequestCertificate.html)` action in the *AWS Certificate Manager API Reference*\.

**Important**  
When you use the `AWS::CertificateManager::Certificate` resource in an AWS CloudFormation stack, the stack will remain in the `CREATE_IN_PROGRESS` state and any further stack operations will be delayed until you validate the certificate request, either by acting upon the instructions in the certificate validation email, or by adding a CNAME record to your DNS configuration\.

If the certificate request is not validated within XXX hours, the stack will time out and be rolled back, deleting the pending certificate.

**Topics**
+ [Syntax](#aws-resource-certificatemanager-certificate-syntax)
+ [Properties](#aws-resource-certificatemanager-certificate-properties)
+ [Return Value](#aws-resource-certificatemanager-certificate-return-values)
+ [Example](#aws-resource-certificatemanager-certificate-examples)

## Syntax<a name="aws-resource-certificatemanager-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-certificatemanager-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::CertificateManager::Certificate",
  "Properties" : {
    "[DomainName](#cfn-certificatemanager-certificate-domainname)" : String,
    "[DomainValidationOptions](#cfn-certificatemanager-certificate-domainvalidationoptions)" : [ [DomainValidationOptions](aws-properties-certificatemanager-certificate-domainvalidationoption.md), ... ],
    "[SubjectAlternativeNames](#cfn-certificatemanager-certificate-subjectalternativenames)" : [ String, ... ],
    "[Tags](#cfn-certificatemanager-certificate-tags)" : [ Resource Tag, ... ],
    "[ValidationMethod](#cfn-certificatemanager-certificate-validationmethod)" : String
  }
}
```

### YAML<a name="aws-resource-certificatemanager-certificate-syntax.yaml"></a>

```
Type: AWS::CertificateManager::Certificate
Properties: 
  [DomainName](#cfn-certificatemanager-certificate-domainname): String
  [DomainValidationOptions](#cfn-certificatemanager-certificate-domainvalidationoptions):
    - [DomainValidationOptions](aws-properties-certificatemanager-certificate-domainvalidationoption.md)
  [SubjectAlternativeNames](#cfn-certificatemanager-certificate-subjectalternativenames):
    - String
  [Tags](#cfn-certificatemanager-certificate-tags):
    - Resource Tag
  [ValidationMethod](#cfn-certificatemanager-certificate-validationmethod): String
```

## Properties<a name="aws-resource-certificatemanager-certificate-properties"></a>

`DomainName`  <a name="cfn-certificatemanager-certificate-domainname"></a>
Fully qualified domain name \(FQDN\), such as `www.example.com`, of the site that you want to secure with the ACM certificate\. To protect several sites in the same domain, use an asterisk \(`*`\) to specify a wildcard\. For example, `*.example.com` protects `www.example.com`, `site.example.com`, and `images.example.com`\.  
For constraints, see the `DomainName` parameter for the [RequestCertificate](https://docs.aws.amazon.com/acm/latest/APIReference/API_RequestCertificate.html) action in the *AWS Certificate Manager API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DomainValidationOptions`  <a name="cfn-certificatemanager-certificate-domainvalidationoptions"></a>
Domain information that domain name registrars use to verify your identity\. For more information and the default values, see [Configure Email for Your Domain](https://docs.aws.amazon.com/acm/latest/userguide/setup-email.html) and [Validate Domain Ownership](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-email.html) in the *AWS Certificate Manager User Guide*\.  
*Required*: No  
*Type*: List of [AWS Certificate Manager Certificate DomainValidationOption](aws-properties-certificatemanager-certificate-domainvalidationoption.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubjectAlternativeNames`  <a name="cfn-certificatemanager-certificate-subjectalternativenames"></a>
FQDNs to be included in the Subject Alternative Name extension of the ACM certificate\. For example, you can add `www.example.net` to a certificate for the `www.example.com` domain name so that users can reach your site by using either name\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-certificatemanager-certificate-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this ACM certificate\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`ValidationMethod`  <a name="cfn-certificatemanager-certificate-validationmethod"></a>
The method you want to use if you are requesting a public certificate to validate that you own or control a domain\. Valid values include `EMAIL` or `DNS`\. We recommend that you use DNS validation\. The default is `EMAIL`\.  
ACM uses CNAME \(Canonical Name\) records to validate that you own or control a domain\. When you choose DNS validation, ACM provides you one or more CNAME records to insert into your DNS database\. During stack creation, CloudFormation emits a **CREATE\_IN\_PROGRESS** event which lists these CNAME records\. They are displayed in the **Status reason** column on the **Events** page for the stack\. In order for CloudFormation to complete stack creation, you must add the CNAME records to your DNS database\. For more information, see [Use DNS to Validate Domain Ownership](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-dns.html) in the *[AWS Certificate Manager User Guide](https://docs.aws.amazon.com/acm/latest/userguide/)*\.  
For more information on email validation, see [Use Email to Validate Domain Ownership](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-email.html) in the *[AWS Certificate Manager User Guide](https://docs.aws.amazon.com/acm/latest/userguide/)*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-certificatemanager-certificate-return-values"></a>

### Ref<a name="aws-resource-certificatemanager-certificate-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the certificate Amazon Resource Name \(ARN\), such as `arn:aws:acm:us-east-1:123456789012:certificate/12ab3c4d-56789-0ef1-2345-3dab6fa3ee50`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-certificatemanager-certificate-examples"></a>

The following example creates an ACM certificate for the `example.com` domain name\. ACM sends validation emails to the email address that is registered to the `example.com` domain\.

### JSON<a name="aws-resource-certificatemanager-certificate-example.json"></a>

```
"mycert" : {
  "Type" : "AWS::CertificateManager::Certificate",
  "Properties" : {
    "DomainName" : "example.com",
    "DomainValidationOptions" : [{
      "DomainName" : "example.com",
      "ValidationDomain" : "example.com"
    }]
  }
}
```

### YAML<a name="aws-resource-certificatemanager-certificate-example.yaml"></a>

```
mycert:
  Type: AWS::CertificateManager::Certificate
  Properties:
    DomainName: example.com
    DomainValidationOptions:
    - DomainName: example.com
      ValidationDomain: example.com
```
