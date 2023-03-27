# AWS::WAFv2::WebACL ResponseInspectionJson<a name="aws-properties-wafv2-webacl-responseinspectionjson"></a>

Configures inspection of the response JSON\. AWS WAF can inspect the first 65,536 bytes \(64 KB\) of the response JSON\. This is part of the `ResponseInspection` configuration for `AWSManagedRulesATPRuleSet`\. 

**Note**  
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.

## Syntax<a name="aws-properties-wafv2-webacl-responseinspectionjson-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-responseinspectionjson-syntax.json"></a>

```
{
  "[FailureValues](#cfn-wafv2-webacl-responseinspectionjson-failurevalues)" : [ String, ... ],
  "[Identifier](#cfn-wafv2-webacl-responseinspectionjson-identifier)" : String,
  "[SuccessValues](#cfn-wafv2-webacl-responseinspectionjson-successvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-responseinspectionjson-syntax.yaml"></a>

```
  [FailureValues](#cfn-wafv2-webacl-responseinspectionjson-failurevalues): 
    - String
  [Identifier](#cfn-wafv2-webacl-responseinspectionjson-identifier): String
  [SuccessValues](#cfn-wafv2-webacl-responseinspectionjson-successvalues): 
    - String
```

## Properties<a name="aws-properties-wafv2-webacl-responseinspectionjson-properties"></a>

`FailureValues`  <a name="cfn-wafv2-webacl-responseinspectionjson-failurevalues"></a>
Values for the specified identifier in the response JSON that indicate a failed login attempt\. To be counted as a failed login, the value must be an exact match, including case\. Each value must be unique among the success and failure values\.   
JSON example: `"FailureValues": [ "False", "Failed" ]`   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Identifier`  <a name="cfn-wafv2-webacl-responseinspectionjson-identifier"></a>
The identifier for the value to match against in the JSON\. The identifier must be an exact match, including case\.  
JSON example: `"Identifier": [ "/login/success" ]`   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessValues`  <a name="cfn-wafv2-webacl-responseinspectionjson-successvalues"></a>
Values for the specified identifier in the response JSON that indicate a successful login attempt\. To be counted as a successful login, the value must be an exact match, including case\. Each value must be unique among the success and failure values\.   
JSON example: `"SuccessValues": [ "True", "Succeeded" ]`   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)