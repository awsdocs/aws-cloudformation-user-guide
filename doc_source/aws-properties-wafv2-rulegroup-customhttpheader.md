# AWS::WAFv2::RuleGroup CustomHTTPHeader<a name="aws-properties-wafv2-rulegroup-customhttpheader"></a>

A custom header for custom request and response handling\. This is used in `CustomResponse` and `CustomRequestHandling` 

## Syntax<a name="aws-properties-wafv2-rulegroup-customhttpheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-customhttpheader-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-rulegroup-customhttpheader-name)" : String,
  "[Value](#cfn-wafv2-rulegroup-customhttpheader-value)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-customhttpheader-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-rulegroup-customhttpheader-name): String
  [Value](#cfn-wafv2-rulegroup-customhttpheader-value): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-customhttpheader-properties"></a>

`Name`  <a name="cfn-wafv2-rulegroup-customhttpheader-name"></a>
The name of the custom header\.   
For custom request header insertion, when AWS WAF inserts the header into the request, it prefixes this name `x-amzn-waf-`, to avoid confusion with the headers that are already in the request\. For example, for the header name `sample`, AWS WAF inserts the header `x-amzn-waf-sample`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9._$-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-wafv2-rulegroup-customhttpheader-value"></a>
The value of the custom header\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)