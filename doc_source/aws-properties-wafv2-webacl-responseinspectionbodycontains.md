# AWS::WAFv2::WebACL ResponseInspectionBodyContains<a name="aws-properties-wafv2-webacl-responseinspectionbodycontains"></a>

Configures inspection of the response body\. AWS WAF can inspect the first 65,536 bytes \(64 KB\) of the response body\. This is part of the `ResponseInspection` configuration for `AWSManagedRulesATPRuleSet`\. 

**Note**  
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.

## Syntax<a name="aws-properties-wafv2-webacl-responseinspectionbodycontains-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-responseinspectionbodycontains-syntax.json"></a>

```
{
  "[FailureStrings](#cfn-wafv2-webacl-responseinspectionbodycontains-failurestrings)" : [ String, ... ],
  "[SuccessStrings](#cfn-wafv2-webacl-responseinspectionbodycontains-successstrings)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-responseinspectionbodycontains-syntax.yaml"></a>

```
  [FailureStrings](#cfn-wafv2-webacl-responseinspectionbodycontains-failurestrings): 
    - String
  [SuccessStrings](#cfn-wafv2-webacl-responseinspectionbodycontains-successstrings): 
    - String
```

## Properties<a name="aws-properties-wafv2-webacl-responseinspectionbodycontains-properties"></a>

`FailureStrings`  <a name="cfn-wafv2-webacl-responseinspectionbodycontains-failurestrings"></a>
Strings in the body of the response that indicate a failed login attempt\. To be counted as a failed login, the string can be anywhere in the body and must be an exact match, including case\. Each string must be unique among the success and failure strings\.   
JSON example: `"FailureStrings": [ "Login failed" ]`   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessStrings`  <a name="cfn-wafv2-webacl-responseinspectionbodycontains-successstrings"></a>
Strings in the body of the response that indicate a successful login attempt\. To be counted as a successful login, the string can be anywhere in the body and must be an exact match, including case\. Each string must be unique among the success and failure strings\.   
JSON example: `"SuccessStrings": [ "Login successful", "Welcome to our site!" ]`   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)