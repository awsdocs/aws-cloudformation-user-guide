# AWS::WAFv2::RuleGroup RuleAction<a name="aws-properties-wafv2-rulegroup-ruleaction"></a>

The action that AWS WAF should take on a web request when it matches a rule's statement\. Settings at the web ACL level can override the rule action setting\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax.json"></a>

```
{
  "[Allow](#cfn-wafv2-rulegroup-ruleaction-allow)" : Json,
  "[Block](#cfn-wafv2-rulegroup-ruleaction-block)" : Json,
  "[Captcha](#cfn-wafv2-rulegroup-ruleaction-captcha)" : Json,
  "[Count](#cfn-wafv2-rulegroup-ruleaction-count)" : Json
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax.yaml"></a>

```
  [Allow](#cfn-wafv2-rulegroup-ruleaction-allow): Json
  [Block](#cfn-wafv2-rulegroup-ruleaction-block): Json
  [Captcha](#cfn-wafv2-rulegroup-ruleaction-captcha): Json
  [Count](#cfn-wafv2-rulegroup-ruleaction-count): Json
```

## Properties<a name="aws-properties-wafv2-rulegroup-ruleaction-properties"></a>

`Allow`  <a name="cfn-wafv2-rulegroup-ruleaction-allow"></a>
Instructs AWS WAF to allow the web request\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Block`  <a name="cfn-wafv2-rulegroup-ruleaction-block"></a>
Instructs AWS WAF to block the web request\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Captcha`  <a name="cfn-wafv2-rulegroup-ruleaction-captcha"></a>
Specifies that AWS WAF should run a `CAPTCHA` check against the request:   
+ If the request includes a valid, unexpired `CAPTCHA` token, AWS WAF allows the web request inspection to proceed to the next rule, similar to a `CountAction`\. 
+ If the request doesn't include a valid, unexpired `CAPTCHA` token, AWS WAF discontinues the web ACL evaluation of the request and blocks it from going to its intended destination\.

   AWS WAF generates a response that it sends back to the client, which includes the following: 
  + The header `x-amzn-waf-action` with a value of `captcha`\. 
  + The HTTP status code `405 Method Not Allowed`\. 
  + If the request contains an `Accept` header with a value of `text/html`, the response includes a `CAPTCHA` challenge\. 
You can configure the expiration time in the `CaptchaConfig` `ImmunityTimeProperty` setting at the rule and web ACL level\. The rule setting overrides the web ACL setting\.   
This action option is available for rules\. It isn't available for web ACL default actions\.   
This is used in the context of other settings, for example to specify values for `RuleAction` and web ACL `DefaultAction`\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-wafv2-rulegroup-ruleaction-count"></a>
Instructs AWS WAF to count the web request and allow it\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-rulegroup-ruleaction--examples"></a>



### Set an allow action<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_"></a>

The following shows an example allow action specification\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_--yaml"></a>

```
Action:
  Allow: {}
```

#### JSON<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_--json"></a>

```
"Action": {
  "Allow": {}
}
```

### Set an allow action with a custom request setting<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_with_a_custom_request_setting"></a>

The following shows an example allow action specification with custom request handling\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_with_a_custom_request_setting--yaml"></a>

```
Action:
  Allow:
    CustomRequestHandling:
      InsertHeaders:
        - Name: AllowActionHeader1Name
          Value: AllowActionHeader1Value
        - Name: AllowActionHeader2Name
          Value: AllowActionHeader2Value
```

#### JSON<a name="aws-properties-wafv2-rulegroup-ruleaction--examples--Set_an_allow_action_with_a_custom_request_setting--json"></a>

```
"Action": {
  "Allow": {
    "CustomRequestHandling": {
      "InsertHeaders": [
        {
          "Name": "AllowActionHeader1Name",
          "Value": "AllowActionHeader1Value"
        },
        {
          "Name": "AllowActionHeader2Name",
          "Value": "AllowActionHeader2Value"
        }
      ]
    }
  }
}
```