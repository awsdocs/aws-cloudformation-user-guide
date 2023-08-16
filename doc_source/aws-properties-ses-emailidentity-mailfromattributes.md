# AWS::SES::EmailIdentity MailFromAttributes<a name="aws-properties-ses-emailidentity-mailfromattributes"></a>

Used to enable or disable the custom Mail\-From domain configuration for an email identity\.

## Syntax<a name="aws-properties-ses-emailidentity-mailfromattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-emailidentity-mailfromattributes-syntax.json"></a>

```
{
  "[BehaviorOnMxFailure](#cfn-ses-emailidentity-mailfromattributes-behavioronmxfailure)" : String,
  "[MailFromDomain](#cfn-ses-emailidentity-mailfromattributes-mailfromdomain)" : String
}
```

### YAML<a name="aws-properties-ses-emailidentity-mailfromattributes-syntax.yaml"></a>

```
  [BehaviorOnMxFailure](#cfn-ses-emailidentity-mailfromattributes-behavioronmxfailure): String
  [MailFromDomain](#cfn-ses-emailidentity-mailfromattributes-mailfromdomain): String
```

## Properties<a name="aws-properties-ses-emailidentity-mailfromattributes-properties"></a>

`BehaviorOnMxFailure`  <a name="cfn-ses-emailidentity-mailfromattributes-behavioronmxfailure"></a>
The action to take if the required MX record isn't found when you send an email\. When you set this value to `USE_DEFAULT_VALUE`, the mail is sent using *amazonses\.com* as the MAIL FROM domain\. When you set this value to `REJECT_MESSAGE`, the Amazon SES API v2 returns a `MailFromDomainNotVerified` error, and doesn't attempt to deliver the email\.  
These behaviors are taken when the custom MAIL FROM domain configuration is in the `Pending`, `Failed`, and `TemporaryFailure` states\.  
Valid Values: `USE_DEFAULT_VALUE | REJECT_MESSAGE`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MailFromDomain`  <a name="cfn-ses-emailidentity-mailfromattributes-mailfromdomain"></a>
The custom MAIL FROM domain that you want the verified identity to use\. The MAIL FROM domain must meet the following criteria:  
+ It has to be a subdomain of the verified identity\.
+ It can't be used to receive email\.
+ It can't be used in a "From" address if the MAIL FROM domain is a destination for feedback forwarding emails\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)