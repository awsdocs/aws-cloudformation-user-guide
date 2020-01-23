# AWS::WAFv2::RuleGroup SingleHeader<a name="aws-properties-wafv2-rulegroup-singleheader"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

One of the headers in a web request, identified by name, for example, `User-Agent` or `Referer`\. This setting isn't case sensitive\.

This is used only to indicate the web request component for AWS WAF to inspect, in the `FieldToMatch` setting of a rule statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-singleheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-singleheader-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-rulegroup-singleheader-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-singleheader-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-rulegroup-singleheader-name): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-singleheader-properties"></a>

`Name`  <a name="cfn-wafv2-rulegroup-singleheader-name"></a>
The name of the query header to inspect\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)