# AWS::WAFv2::WebACL NoneAction<a name="aws-properties-wafv2-webacl-noneaction"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Specifies that AWS WAF should do nothing\. This is generally used to try out a rule without performing any actions\. You set the `OverrideAction` on the Rule, and override the actions that are set at the statement level\. 

This is used only in the context of other settings, for example to specify the value for the web ACL `OverrideAction`\. 