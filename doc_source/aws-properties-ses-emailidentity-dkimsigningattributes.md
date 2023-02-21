# AWS::SES::EmailIdentity DkimSigningAttributes<a name="aws-properties-ses-emailidentity-dkimsigningattributes"></a>

Used to configure or change the DKIM authentication settings for an email domain identity\. You can use this operation to do any of the following:
+ Update the signing attributes for an identity that uses Bring Your Own DKIM \(BYODKIM\)\.
+ Update the key length that should be used for Easy DKIM\.
+ Change from using no DKIM authentication to using Easy DKIM\.
+ Change from using no DKIM authentication to using BYODKIM\.
+ Change from using Easy DKIM to using BYODKIM\.
+ Change from using BYODKIM to using Easy DKIM\.

## Syntax<a name="aws-properties-ses-emailidentity-dkimsigningattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-emailidentity-dkimsigningattributes-syntax.json"></a>

```
{
  "[DomainSigningPrivateKey](#cfn-ses-emailidentity-dkimsigningattributes-domainsigningprivatekey)" : String,
  "[DomainSigningSelector](#cfn-ses-emailidentity-dkimsigningattributes-domainsigningselector)" : String,
  "[NextSigningKeyLength](#cfn-ses-emailidentity-dkimsigningattributes-nextsigningkeylength)" : String
}
```

### YAML<a name="aws-properties-ses-emailidentity-dkimsigningattributes-syntax.yaml"></a>

```
  [DomainSigningPrivateKey](#cfn-ses-emailidentity-dkimsigningattributes-domainsigningprivatekey): String
  [DomainSigningSelector](#cfn-ses-emailidentity-dkimsigningattributes-domainsigningselector): String
  [NextSigningKeyLength](#cfn-ses-emailidentity-dkimsigningattributes-nextsigningkeylength): String
```

## Properties<a name="aws-properties-ses-emailidentity-dkimsigningattributes-properties"></a>

`DomainSigningPrivateKey`  <a name="cfn-ses-emailidentity-dkimsigningattributes-domainsigningprivatekey"></a>
\[Bring Your Own DKIM\] A private key that's used to generate a DKIM signature\.  
The private key must use 1024 or 2048\-bit RSA encryption, and must be encoded using base64 encoding\.  
Rather than embedding sensitive information directly in your CFN templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CFN, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainSigningSelector`  <a name="cfn-ses-emailidentity-dkimsigningattributes-domainsigningselector"></a>
\[Bring Your Own DKIM\] A string that's used to identify a public key in the DNS configuration for a domain\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextSigningKeyLength`  <a name="cfn-ses-emailidentity-dkimsigningattributes-nextsigningkeylength"></a>
\[Easy DKIM\] The key length of the future DKIM key pair to be generated\. This can be changed at most once per day\.  
Valid Values: `RSA_1024_BIT | RSA_2048_BIT`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)