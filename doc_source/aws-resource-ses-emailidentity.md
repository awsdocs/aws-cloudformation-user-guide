# AWS::SES::EmailIdentity<a name="aws-resource-ses-emailidentity"></a>

Specifies an identity for using within SES\. An identity is an email address or domain that you use when you send email\. Before you can use an identity to send email, you first have to verify it\. By verifying an identity, you demonstrate that you're the owner of the identity, and that you've given Amazon SES API v2 permission to send email from the identity\.

When you verify an email address, SES sends an email to the address\. Your email address is verified as soon as you follow the link in the verification email\. When you verify a domain without specifying the DkimSigningAttributes properties, OR only the NextSigningKeyLength property of DkimSigningAttributes, this resource provides a set of CNAME token names and values \(DkimDNSTokenName1, DkimDNSTokenValue1, DkimDNSTokenName2, DkimDNSTokenValue2, DkimDNSTokenName3, DkimDNSTokenValue3\) as outputs\. You can then add these to the DNS configuration for your domain\. Your domain is verified when Amazon SES detects these records in the DNS configuration for your domain\. This verification method is known as Easy DKIM\.

Alternatively, you can perform the verification process by providing your own public\-private key pair\. This verification method is known as Bring Your Own DKIM \(BYODKIM\)\. To use BYODKIM, your resource must include DkimSigningAttributes properties DomainSigningSelector and DomainSigningPrivateKey\. When you specify this object, you provide a selector \(DomainSigningSelector\) \(a component of the DNS record name that identifies the public key to use for DKIM authentication\) and a private key \(DomainSigningPrivateKey\)\.

Additionally, you can associate an existing configuration set with the email identity that you're verifying\.

## Syntax<a name="aws-resource-ses-emailidentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-emailidentity-syntax.json"></a>

```
{
  "Type" : "AWS::SES::EmailIdentity",
  "Properties" : {
      "[ConfigurationSetAttributes](#cfn-ses-emailidentity-configurationsetattributes)" : ConfigurationSetAttributes,
      "[DkimAttributes](#cfn-ses-emailidentity-dkimattributes)" : DkimAttributes,
      "[DkimSigningAttributes](#cfn-ses-emailidentity-dkimsigningattributes)" : DkimSigningAttributes,
      "[EmailIdentity](#cfn-ses-emailidentity-emailidentity)" : String,
      "[FeedbackAttributes](#cfn-ses-emailidentity-feedbackattributes)" : FeedbackAttributes,
      "[MailFromAttributes](#cfn-ses-emailidentity-mailfromattributes)" : MailFromAttributes
    }
}
```

### YAML<a name="aws-resource-ses-emailidentity-syntax.yaml"></a>

```
Type: AWS::SES::EmailIdentity
Properties: 
  [ConfigurationSetAttributes](#cfn-ses-emailidentity-configurationsetattributes): 
    ConfigurationSetAttributes
  [DkimAttributes](#cfn-ses-emailidentity-dkimattributes): 
    DkimAttributes
  [DkimSigningAttributes](#cfn-ses-emailidentity-dkimsigningattributes): 
    DkimSigningAttributes
  [EmailIdentity](#cfn-ses-emailidentity-emailidentity): String
  [FeedbackAttributes](#cfn-ses-emailidentity-feedbackattributes): 
    FeedbackAttributes
  [MailFromAttributes](#cfn-ses-emailidentity-mailfromattributes): 
    MailFromAttributes
```

## Properties<a name="aws-resource-ses-emailidentity-properties"></a>

`ConfigurationSetAttributes`  <a name="cfn-ses-emailidentity-configurationsetattributes"></a>
Used to associate a configuration set with an email identity\.  
*Required*: No  
*Type*: [ConfigurationSetAttributes](aws-properties-ses-emailidentity-configurationsetattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DkimAttributes`  <a name="cfn-ses-emailidentity-dkimattributes"></a>
An object that contains information about the DKIM attributes for the identity\.  
*Required*: No  
*Type*: [DkimAttributes](aws-properties-ses-emailidentity-dkimattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DkimSigningAttributes`  <a name="cfn-ses-emailidentity-dkimsigningattributes"></a>
If your request includes this object, Amazon SES configures the identity to use Bring Your Own DKIM \(BYODKIM\) for DKIM authentication purposes, or, configures the key length to be used for [Easy DKIM](https://docs.aws.amazon.com/ses/latest/dg/send-email-authentication-dkim-easy.html)\.  
*Required*: No  
*Type*: [DkimSigningAttributes](aws-properties-ses-emailidentity-dkimsigningattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailIdentity`  <a name="cfn-ses-emailidentity-emailidentity"></a>
The email address or domain to verify\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeedbackAttributes`  <a name="cfn-ses-emailidentity-feedbackattributes"></a>
Used to enable or disable feedback forwarding for an identity\.  
*Required*: No  
*Type*: [FeedbackAttributes](aws-properties-ses-emailidentity-feedbackattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MailFromAttributes`  <a name="cfn-ses-emailidentity-mailfromattributes"></a>
Used to enable or disable the custom Mail\-From domain configuration for an email identity\.  
*Required*: No  
*Type*: [MailFromAttributes](aws-properties-ses-emailidentity-mailfromattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ses-emailidentity-return-values"></a>

### Ref<a name="aws-resource-ses-emailidentity-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ses-emailidentity-return-values-fn--getatt"></a>

#### <a name="aws-resource-ses-emailidentity-return-values-fn--getatt-fn--getatt"></a>

`DkimDNSTokenName1`  <a name="DkimDNSTokenName1-fn::getatt"></a>
The host name for the first token that you have to add to the DNS configuration for your domain\.

`DkimDNSTokenName2`  <a name="DkimDNSTokenName2-fn::getatt"></a>
The host name for the second token that you have to add to the DNS configuration for your domain\.

`DkimDNSTokenName3`  <a name="DkimDNSTokenName3-fn::getatt"></a>
The host name for the third token that you have to add to the DNS configuration for your domain\.

`DkimDNSTokenValue1`  <a name="DkimDNSTokenValue1-fn::getatt"></a>
The record value for the first token that you have to add to the DNS configuration for your domain\.

`DkimDNSTokenValue2`  <a name="DkimDNSTokenValue2-fn::getatt"></a>
The record value for the second token that you have to add to the DNS configuration for your domain\.

`DkimDNSTokenValue3`  <a name="DkimDNSTokenValue3-fn::getatt"></a>
The record value for the third token that you have to add to the DNS configuration for your domain\.