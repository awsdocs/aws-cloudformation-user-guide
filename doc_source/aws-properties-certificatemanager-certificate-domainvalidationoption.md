# AWS::CertificateManager::Certificate DomainValidationOption<a name="aws-properties-certificatemanager-certificate-domainvalidationoption"></a>

 `DomainValidationOption` is a property of the [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html) resource that specifies the AWS Certificate Manager \(ACM\) certificate domain to validate\. Depending on the chosen validation method, ACM checks the domain's DNS record for a validation CNAME, or it attempts to send a validation email message to the domain owner\.

## Syntax<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-syntax.json"></a>

```
{
  "[DomainName](#cfn-certificatemanager-certificate-domainvalidationoptions-domainname)" : String,
  "[HostedZoneId](#cfn-certificatemanager-certificate-domainvalidationoption-hostedzoneid)" : String,
  "[ValidationDomain](#cfn-certificatemanager-certificate-domainvalidationoption-validationdomain)" : String
}
```

### YAML<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-syntax.yaml"></a>

```
  [DomainName](#cfn-certificatemanager-certificate-domainvalidationoptions-domainname): String
  [HostedZoneId](#cfn-certificatemanager-certificate-domainvalidationoption-hostedzoneid): String
  [ValidationDomain](#cfn-certificatemanager-certificate-domainvalidationoption-validationdomain): String
```

## Properties<a name="aws-properties-certificatemanager-certificate-domainvalidationoption-properties"></a>

`DomainName`  <a name="cfn-certificatemanager-certificate-domainvalidationoptions-domainname"></a>
A fully qualified domain name \(FQDN\) in the certificate request\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Pattern*: `^(\*\.)?(((?!-)[A-Za-z0-9-]{0,62}[A-Za-z0-9])\.)+((?!-)[A-Za-z0-9-]{1,62}[A-Za-z0-9])$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-certificatemanager-certificate-domainvalidationoption-hostedzoneid"></a>
The `HostedZoneId` option, which is available if you are using Route 53 as your domain registrar, causes ACM to add your CNAME to the domain record\. Your list of `DomainValidationOptions` must contain one and only one of the domain\-validation options, and the `HostedZoneId` can be used only when `DNS` is specified as your validation method\.  
Use the Route 53 `ListHostedZones` API to discover IDs for available hosted zones\.   
The `ListHostedZones` API returns IDs in the format "/hostedzone/Z111111QQQQQQQ", but CloudFormation requires the IDs to be in the format "Z111111QQQQQQQ"\.
When you change your `DomainValidationOptions`, a new resource is created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationDomain`  <a name="cfn-certificatemanager-certificate-domainvalidationoption-validationdomain"></a>
The domain name to which you want ACM to send validation emails\. This domain name is the suffix of the email addresses that you want ACM to use\. This must be the same as the `DomainName` value or a superdomain of the `DomainName` value\. For example, if you request a certificate for `testing.example.com`, you can specify `example.com` as this value\. In that case, ACM sends domain validation emails to the following five addresses:  
+ admin@example\.com
+ administrator@example\.com
+ hostmaster@example\.com
+ postmaster@example\.com
+ webmaster@example\.com
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `253`  
*Pattern*: `^(\*\.)?(((?!-)[A-Za-z0-9-]{0,62}[A-Za-z0-9])\.)+((?!-)[A-Za-z0-9-]{1,62}[A-Za-z0-9])$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)