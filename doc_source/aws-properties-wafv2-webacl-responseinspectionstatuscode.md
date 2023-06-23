# AWS::WAFv2::WebACL ResponseInspectionStatusCode<a name="aws-properties-wafv2-webacl-responseinspectionstatuscode"></a>

Configures inspection of the response status code\. This is part of the `ResponseInspection` configuration for `AWSManagedRulesATPRuleSet`\. 

**Note**  
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.

## Syntax<a name="aws-properties-wafv2-webacl-responseinspectionstatuscode-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-responseinspectionstatuscode-syntax.json"></a>

```
{
  "[FailureCodes](#cfn-wafv2-webacl-responseinspectionstatuscode-failurecodes)" : [ Integer, ... ],
  "[SuccessCodes](#cfn-wafv2-webacl-responseinspectionstatuscode-successcodes)" : [ Integer, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-responseinspectionstatuscode-syntax.yaml"></a>

```
  [FailureCodes](#cfn-wafv2-webacl-responseinspectionstatuscode-failurecodes): 
    - Integer
  [SuccessCodes](#cfn-wafv2-webacl-responseinspectionstatuscode-successcodes): 
    - Integer
```

## Properties<a name="aws-properties-wafv2-webacl-responseinspectionstatuscode-properties"></a>

`FailureCodes`  <a name="cfn-wafv2-webacl-responseinspectionstatuscode-failurecodes"></a>
Status codes in the response that indicate a failed login attempt\. To be counted as a failed login, the response status code must match one of these\. Each code must be unique among the success and failure status codes\.   
JSON example: `"FailureCodes": [ 400, 404 ]`   
*Required*: Yes  
*Type*: List of Integer  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuccessCodes`  <a name="cfn-wafv2-webacl-responseinspectionstatuscode-successcodes"></a>
Status codes in the response that indicate a successful login attempt\. To be counted as a successful login, the response status code must match one of these\. Each code must be unique among the success and failure status codes\.   
JSON example: `"SuccessCodes": [ 200, 201 ]`   
*Required*: Yes  
*Type*: List of Integer  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)