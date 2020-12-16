# AWS::CertificateManager::Certificate<a name="aws-resource-certificatemanager-certificate"></a>

The `AWS::CertificateManager::Certificate` resource requests an AWS Certificate Manager \(ACM\) certificate that you can use to enable secure connections\. For example, you can deploy an ACM certificate to an Elastic Load Balancer to enable HTTPS support\. For more information, see [RequestCertificate](https://docs.aws.amazon.com/acm/latest/APIReference/API_RequestCertificate.html) in the AWS Certificate Manager API Reference\.

**Important**  
When you use the `AWS::CertificateManager::Certificate` resource in a CloudFormation stack, domain validation is handled automatically if all three of the following are true: The certificate domain is hosted in Amazon Route 53, the domain resides in your AWS account, and you are using DNS validation\.  
However, if the certificate uses email validation, or if the domain is not hosted in Route 53, then the stack will remain in the `CREATE_IN_PROGRESS` state\. Further stack operations are delayed until you validate the certificate request, either by acting upon the instructions in the validation email, or by adding a CNAME record to your DNS configuration\. For more information, see [Use Email to Validate Domain Ownership](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-email.html) and [Use DNS to Validate Domain Ownership](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-dns.html)\.

## Syntax<a name="aws-resource-certificatemanager-certificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-certificatemanager-certificate-syntax.json"></a>

```
{
  "Type" : "AWS::CertificateManager::Certificate",
  "Properties" : {
      "[CertificateAuthorityArn](#cfn-certificatemanager-certificate-certificateauthorityarn)" : String,
      "[CertificateTransparencyLoggingPreference](#cfn-certificatemanager-certificate-certificatetransparencyloggingpreference)" : String,
      "[DomainName](#cfn-certificatemanager-certificate-domainname)" : String,
      "[DomainValidationOptions](#cfn-certificatemanager-certificate-domainvalidationoptions)" : [ DomainValidationOption, ... ],
      "[SubjectAlternativeNames](#cfn-certificatemanager-certificate-subjectalternativenames)" : [ String, ... ],
      "[Tags](#cfn-certificatemanager-certificate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ValidationMethod](#cfn-certificatemanager-certificate-validationmethod)" : String
    }
}
```

### YAML<a name="aws-resource-certificatemanager-certificate-syntax.yaml"></a>

```
Type: AWS::CertificateManager::Certificate
Properties: 
  [CertificateAuthorityArn](#cfn-certificatemanager-certificate-certificateauthorityarn): String
  [CertificateTransparencyLoggingPreference](#cfn-certificatemanager-certificate-certificatetransparencyloggingpreference): String
  [DomainName](#cfn-certificatemanager-certificate-domainname): String
  [DomainValidationOptions](#cfn-certificatemanager-certificate-domainvalidationoptions): 
    - DomainValidationOption
  [SubjectAlternativeNames](#cfn-certificatemanager-certificate-subjectalternativenames): 
    - String
  [Tags](#cfn-certificatemanager-certificate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ValidationMethod](#cfn-certificatemanager-certificate-validationmethod): String
```

## Properties<a name="aws-resource-certificatemanager-certificate-properties"></a>

`CertificateAuthorityArn`  <a name="cfn-certificatemanager-certificate-certificateauthorityarn"></a>
The Amazon Resource Name \(ARN\) of the private certificate authority \(CA\) that will be used to issue the certificate\. If you do not provide an ARN and you are trying to request a private certificate, ACM will attempt to issue a public certificate\. For more information about private CAs, see the [AWS Certificate Manager Private Certificate Authority \(PCA\)](https://docs.aws.amazon.com/acm-pca/latest/userguide/PcaWelcome.html) user guide\. The ARN must have the following form:   
 `arn:aws:acm-pca:region:account:certificate-authority/12345678-1234-1234-1234-123456789012`   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:[\w+=/,.@-]*:[0-9]+:[\w+=,.@-]+(/[\w+=,.@-]+)*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CertificateTransparencyLoggingPreference`  <a name="cfn-certificatemanager-certificate-certificatetransparencyloggingpreference"></a>
You can opt out of certificate transparency logging by specifying the `DISABLED` option\. Opt in by specifying `ENABLED`\.  
If you do not specify a certificate transparency logging preference on a new CloudFormation template, or if you remove the logging preference from an existing template, this is the same as explicitly enabling the preference\.  
Changing the certificate transparency logging preference will update the existing resource by calling `UpdateCertificateOptions` on the certificate\. This action will not create a new resource\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-certificatemanager-certificate-domainname"></a>
The fully qualified domain name \(FQDN\), such as www\.example\.com, with which you want to secure an ACM certificate\. Use an asterisk \(\*\) to create a wildcard certificate that protects several sites in the same domain\. For example, `*.example.com` protects `www.example.com`, `site.example.com`, and `images.example.com.`   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Pattern*: `^(\*\.)?(((?!-)[A-Za-z0-9-]{0,62}[A-Za-z0-9])\.)+((?!-)[A-Za-z0-9-]{1,62}[A-Za-z0-9])$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainValidationOptions`  <a name="cfn-certificatemanager-certificate-domainvalidationoptions"></a>
Domain information that domain name registrars use to verify your identity\.  
*Required*: No  
*Type*: List of [DomainValidationOption](aws-properties-certificatemanager-certificate-domainvalidationoption.md)  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubjectAlternativeNames`  <a name="cfn-certificatemanager-certificate-subjectalternativenames"></a>
Additional FQDNs to be included in the Subject Alternative Name extension of the ACM certificate\. For example, you can add www\.example\.net to a certificate for which the `DomainName` field is www\.example\.com if users can reach your site by using either name\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-certificatemanager-certificate-tags"></a>
Key\-value pairs that can identify the certificate\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationMethod`  <a name="cfn-certificatemanager-certificate-validationmethod"></a>
The method you want to use to validate that you own or control the domain associated with a public certificate\. You can [validate with DNS](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-dns.html) or [validate with email](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-validate-email.html)\. We recommend that you use DNS validation\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DNS | EMAIL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-certificatemanager-certificate-return-values"></a>

### Ref<a name="aws-resource-certificatemanager-certificate-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the certificate's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-certificatemanager-certificate--examples"></a>



### Declaring an Amazon Certificate Manager Certificate Resource<a name="aws-resource-certificatemanager-certificate--examples--Declaring_an_Amazon_Certificate_Manager_Certificate_Resource"></a>

The following example shows how to declare an `AWS::CertificateManager::Certificate` resource to create an ACM certificate\.

#### JSON<a name="aws-resource-certificatemanager-certificate--examples--Declaring_an_Amazon_Certificate_Manager_Certificate_Resource--json"></a>

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

#### YAML<a name="aws-resource-certificatemanager-certificate--examples--Declaring_an_Amazon_Certificate_Manager_Certificate_Resource--yaml"></a>

```
mycert:
  Type: AWS::CertificateManager::Certificate
  Properties:
    DomainName: example.com
    DomainValidationOptions:
          - DomainName: example.com
            ValidationDomain: example.com
```