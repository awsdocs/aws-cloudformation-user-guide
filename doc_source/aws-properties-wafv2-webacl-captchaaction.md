# AWS::WAFv2::WebACL CaptchaAction<a name="aws-properties-wafv2-webacl-captchaaction"></a>

Specifies that AWS WAF should run a `CAPTCHA` check against the request: 
+ If the request includes a valid, unexpired `CAPTCHA` token, AWS WAF allows the web request inspection to proceed to the next rule, similar to a `CountAction`\. 
+ If the request doesn't include a valid, unexpired `CAPTCHA` token, AWS WAF discontinues the web ACL evaluation of the request and blocks it from going to its intended destination\.

   AWS WAF generates a response that it sends back to the client, which includes the following: 
  + The header `x-amzn-waf-action` with a value of `captcha`\. 
  + The HTTP status code `405 Method Not Allowed`\. 
  + If the request contains an `Accept` header with a value of `text/html`, the response includes a `CAPTCHA` challenge\. 

You can configure the expiration time in the `CaptchaConfig` `ImmunityTimeProperty` setting at the rule and web ACL level\. The rule setting overrides the web ACL setting\. 

This action option is available for rules\. It isn't available for web ACL default actions\. 

## Syntax<a name="aws-properties-wafv2-webacl-captchaaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-captchaaction-syntax.json"></a>

```
{
  "[CustomRequestHandling](#cfn-wafv2-webacl-captchaaction-customrequesthandling)" : CustomRequestHandling
}
```

### YAML<a name="aws-properties-wafv2-webacl-captchaaction-syntax.yaml"></a>

```
  [CustomRequestHandling](#cfn-wafv2-webacl-captchaaction-customrequesthandling): 
    CustomRequestHandling
```

## Properties<a name="aws-properties-wafv2-webacl-captchaaction-properties"></a>

`CustomRequestHandling`  <a name="cfn-wafv2-webacl-captchaaction-customrequesthandling"></a>
Defines custom handling for the web request, used when the `CAPTCHA` inspection determines that the request's token is valid and unexpired\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomRequestHandling](aws-properties-wafv2-webacl-customrequesthandling.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)