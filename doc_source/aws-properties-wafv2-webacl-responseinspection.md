# AWS::WAFv2::WebACL ResponseInspection<a name="aws-properties-wafv2-webacl-responseinspection"></a>

The criteria for inspecting responses to login requests, used by the ATP rule group to track login failure rates\. 

The ATP rule group evaluates the responses that your protected resources send back to client login attempts, keeping count of successful and failed attempts from each IP address and client session\. Using this information, the rule group labels and mitigates requests from client sessions and IP addresses that submit too many failed login attempts in a short amount of time\. 

**Note**  
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.

This is part of the `AWSManagedRulesATPRuleSet` configuration in `ManagedRuleGroupConfig`\.

Enable login response inspection by configuring exactly one component of the response to inspect\. You can't configure more than one\. If you don't configure any of the response inspection options, response inspection is disabled\. 

## Syntax<a name="aws-properties-wafv2-webacl-responseinspection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-responseinspection-syntax.json"></a>

```
{
  "[BodyContains](#cfn-wafv2-webacl-responseinspection-bodycontains)" : ResponseInspectionBodyContains,
  "[Header](#cfn-wafv2-webacl-responseinspection-header)" : ResponseInspectionHeader,
  "[Json](#cfn-wafv2-webacl-responseinspection-json)" : ResponseInspectionJson,
  "[StatusCode](#cfn-wafv2-webacl-responseinspection-statuscode)" : ResponseInspectionStatusCode
}
```

### YAML<a name="aws-properties-wafv2-webacl-responseinspection-syntax.yaml"></a>

```
  [BodyContains](#cfn-wafv2-webacl-responseinspection-bodycontains): 
    ResponseInspectionBodyContains
  [Header](#cfn-wafv2-webacl-responseinspection-header): 
    ResponseInspectionHeader
  [Json](#cfn-wafv2-webacl-responseinspection-json): 
    ResponseInspectionJson
  [StatusCode](#cfn-wafv2-webacl-responseinspection-statuscode): 
    ResponseInspectionStatusCode
```

## Properties<a name="aws-properties-wafv2-webacl-responseinspection-properties"></a>

`BodyContains`  <a name="cfn-wafv2-webacl-responseinspection-bodycontains"></a>
Configures inspection of the response body\. AWS WAF can inspect the first 65,536 bytes \(64 KB\) of the response body\.   
*Required*: No  
*Type*: [ResponseInspectionBodyContains](aws-properties-wafv2-webacl-responseinspectionbodycontains.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-wafv2-webacl-responseinspection-header"></a>
Configures inspection of the response header\.   
*Required*: No  
*Type*: [ResponseInspectionHeader](aws-properties-wafv2-webacl-responseinspectionheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Json`  <a name="cfn-wafv2-webacl-responseinspection-json"></a>
Configures inspection of the response JSON\. AWS WAF can inspect the first 65,536 bytes \(64 KB\) of the response JSON\.   
*Required*: No  
*Type*: [ResponseInspectionJson](aws-properties-wafv2-webacl-responseinspectionjson.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-wafv2-webacl-responseinspection-statuscode"></a>
Configures inspection of the response status code\.   
*Required*: No  
*Type*: [ResponseInspectionStatusCode](aws-properties-wafv2-webacl-responseinspectionstatuscode.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-responseinspection--examples"></a>



### Configure the response inspection fields for status code inspection<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_status_code_inspection"></a>

The following shows an example `ResponseInspection` for the status code component inspection\. 

#### YAML<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_status_code_inspection--yaml"></a>

```
ResponseInspection:
  StatusCode:
    SuccessCodes:
      - 200
      - 202
    FailureCodes:
      - 400
      - 404
```

#### JSON<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_status_code_inspection--json"></a>

```
"ResponseInspection":{
      "StatusCode":{
         "SuccessCodes":[
            200,
            202
         ],
         "FailureCodes":[
            400,
            404
         ]
      }
   }
```

### Configure the response inspection fields for inspection of the response body<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_inspection_of_the_response_body"></a>

The following shows an example `RequestInspection` for inspection of the response body\. 

#### YAML<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_inspection_of_the_response_body--yaml"></a>

```
ResponseInspection:
  BodyContains:
    SuccessStrings:
      - Successful
      - Logged In
    FailureStrings:
      - Loginfailed
      - Failed Attempt
```

#### JSON<a name="aws-properties-wafv2-webacl-responseinspection--examples--Configure_the_response_inspection_fields_for_inspection_of_the_response_body--json"></a>

```
"ResponseInspection":{
      "BodyContains":{
         "SuccessStrings":[
            "Successful",
            "Logged In"
         ],
         "FailureStrings":[
            "Login Failed",
            "Failed Attempt"
         ]
      }
   }
```