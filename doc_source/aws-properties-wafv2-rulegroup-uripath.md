# AWS::WAFv2::RuleGroup UriPath<a name="aws-properties-wafv2-rulegroup-uripath"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The path component of the URI of a web request\. This is the part of a web request that identifies a resource, for example, `/images/daily-ad.jpg`\.

This is used only to indicate the web request component for AWS WAF to inspect, in the `FieldToMatch` setting of a rule statement\. 