# AWS::PinpointEmail::Identity<a name="aws-resource-pinpointemail-identity"></a>

Specifies an identity to use for sending email through Amazon Pinpoint\. In Amazon Pinpoint, an *identity* is an email address or domain that you use when you send email\. Before you can use Amazon Pinpoint to send an email from an identity, you first have to verify it\. By verifying an identity, you demonstrate that you're the owner of the address or domain, and that you've given Amazon Pinpoint permission to send email from that identity\.

When you verify an email address, Amazon Pinpoint sends an email to the address\. Your email address is verified as soon as you follow the link in the verification email\.

When you verify a domain, this operation provides a set of DKIM tokens, which you can convert into CNAME tokens\. You add these CNAME tokens to the DNS configuration for your domain\. Your domain is verified when Amazon Pinpoint detects these records in the DNS configuration for your domain\. It usually takes around 72 hours to complete the domain verification process\.

**Important**  
When you use CloudFormation to specify an identity, CloudFormation might indicate that the identity was created successfully\. However, you have to verify the identity before you can use it to send email\.

## Syntax<a name="aws-resource-pinpointemail-identity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpointemail-identity-syntax.json"></a>

```
{
  "Type" : "AWS::PinpointEmail::Identity",
  "Properties" : {
      "[DkimSigningEnabled](#cfn-pinpointemail-identity-dkimsigningenabled)" : Boolean,
      "[FeedbackForwardingEnabled](#cfn-pinpointemail-identity-feedbackforwardingenabled)" : Boolean,
      "[MailFromAttributes](#cfn-pinpointemail-identity-mailfromattributes)" : MailFromAttributes,
      "[Name](#cfn-pinpointemail-identity-name)" : String,
      "[Tags](#cfn-pinpointemail-identity-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-pinpointemail-identity-syntax.yaml"></a>

```
Type: AWS::PinpointEmail::Identity
Properties: 
  [DkimSigningEnabled](#cfn-pinpointemail-identity-dkimsigningenabled): Boolean
  [FeedbackForwardingEnabled](#cfn-pinpointemail-identity-feedbackforwardingenabled): Boolean
  [MailFromAttributes](#cfn-pinpointemail-identity-mailfromattributes): 
    MailFromAttributes
  [Name](#cfn-pinpointemail-identity-name): String
  [Tags](#cfn-pinpointemail-identity-tags): 
    - Tags
```

## Properties<a name="aws-resource-pinpointemail-identity-properties"></a>

`DkimSigningEnabled`  <a name="cfn-pinpointemail-identity-dkimsigningenabled"></a>
For domain identities, this attribute is used to enable or disable DomainKeys Identified Mail \(DKIM\) signing for the domain\.  
If the value is `true`, then the messages that you send from the domain are signed using both the DKIM keys for your domain, as well as the keys for the `amazonses.com` domain\. If the value is `false`, then the messages that you send are only signed using the DKIM keys for the `amazonses.com` domain\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FeedbackForwardingEnabled`  <a name="cfn-pinpointemail-identity-feedbackforwardingenabled"></a>
Used to enable or disable feedback forwarding for an identity\. This setting determines what happens when an identity is used to send an email that results in a bounce or complaint event\.  
When you enable feedback forwarding, Amazon Pinpoint sends you email notifications when bounce or complaint events occur\. Amazon Pinpoint sends this notification to the address that you specified in the Return\-Path header of the original email\.  
When you disable feedback forwarding, Amazon Pinpoint sends notifications through other mechanisms, such as by notifying an Amazon SNS topic\. You're required to have a method of tracking bounces and complaints\. If you haven't set up another mechanism for receiving bounce or complaint notifications, Amazon Pinpoint sends an email notification when these events occur \(even if this setting is disabled\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MailFromAttributes`  <a name="cfn-pinpointemail-identity-mailfromattributes"></a>
Used to enable or disable the custom Mail\-From domain configuration for an email identity\.  
*Required*: No  
*Type*: [MailFromAttributes](aws-properties-pinpointemail-identity-mailfromattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-pinpointemail-identity-name"></a>
The address or domain of the identity, such as *sender@example\.com* or *example\.co\.uk*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-pinpointemail-identity-tags"></a>
An object that defines the tags \(keys and values\) that you want to associate with the email identity\.  
*Required*: No  
*Type*: [List](aws-properties-pinpointemail-identity-tags.md) of [Tags](aws-properties-pinpointemail-identity-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpointemail-identity-return-values"></a>

### Ref<a name="aws-resource-pinpointemail-identity-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myEmailIdentity" }` 

For the Amazon Pinpoint identity `myEmailIdentity`, Ref returns the name of the identity \(the email address or domain name\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpointemail-identity-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpointemail-identity-return-values-fn--getatt-fn--getatt"></a>

`IdentityDNSRecordName1`  <a name="IdentityDNSRecordName1-fn::getatt"></a>
The host name for the first token that you have to add to the DNS configuration for your domain\.  
For more information, see [Verifying a Domain](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-email-manage-verify.html#channels-email-manage-verify-domain) in the Amazon Pinpoint User Guide\.

`IdentityDNSRecordName2`  <a name="IdentityDNSRecordName2-fn::getatt"></a>
The host name for the second token that you have to add to the DNS configuration for your domain\.

`IdentityDNSRecordName3`  <a name="IdentityDNSRecordName3-fn::getatt"></a>
The host name for the third token that you have to add to the DNS configuration for your domain\.

`IdentityDNSRecordValue1`  <a name="IdentityDNSRecordValue1-fn::getatt"></a>
The record value for the first token that you have to add to the DNS configuration for your domain\.

`IdentityDNSRecordValue2`  <a name="IdentityDNSRecordValue2-fn::getatt"></a>
The record value for the second token that you have to add to the DNS configuration for your domain\.

`IdentityDNSRecordValue3`  <a name="IdentityDNSRecordValue3-fn::getatt"></a>
The record value for the third token that you have to add to the DNS configuration for your domain\.

## See also<a name="aws-resource-pinpointemail-identity--seealso"></a>
+ [Verifying Email Identities](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-email-manage-verify.html) in the *Amazon Pinpoint User Guide*