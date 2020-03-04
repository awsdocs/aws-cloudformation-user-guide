# AWS::WAFv2::RuleGroup QueryString<a name="aws-properties-wafv2-rulegroup-querystring"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The query string of a web request\. This is the part of a URL that appears after a `?` character, if any\.

This is used only to indicate the web request component for AWS WAF to inspect, in the `FieldToMatch` setting of a rule statement\. 