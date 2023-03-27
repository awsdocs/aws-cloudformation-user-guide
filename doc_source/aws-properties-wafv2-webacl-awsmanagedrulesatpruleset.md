# AWS::WAFv2::WebACL AWSManagedRulesATPRuleSet<a name="aws-properties-wafv2-webacl-awsmanagedrulesatpruleset"></a>

Details for your use of the account takeover prevention managed rule group, `AWSManagedRulesATPRuleSet`\. This configuration is used in `ManagedRuleGroupConfig`\. 

## Syntax<a name="aws-properties-wafv2-webacl-awsmanagedrulesatpruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-awsmanagedrulesatpruleset-syntax.json"></a>

```
{
  "[LoginPath](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-loginpath)" : String,
  "[RequestInspection](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-requestinspection)" : RequestInspection,
  "[ResponseInspection](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-responseinspection)" : ResponseInspection
}
```

### YAML<a name="aws-properties-wafv2-webacl-awsmanagedrulesatpruleset-syntax.yaml"></a>

```
  [LoginPath](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-loginpath): String
  [RequestInspection](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-requestinspection): 
    RequestInspection
  [ResponseInspection](#cfn-wafv2-webacl-awsmanagedrulesatpruleset-responseinspection): 
    ResponseInspection
```

## Properties<a name="aws-properties-wafv2-webacl-awsmanagedrulesatpruleset-properties"></a>

`LoginPath`  <a name="cfn-wafv2-webacl-awsmanagedrulesatpruleset-loginpath"></a>
The path of the login endpoint for your application\. For example, for the URL `https://example.com/web/login`, you would provide the path `/web/login`\.  
The rule group inspects only HTTP `POST` requests to your specified login endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesatpruleset-requestinspection"></a>
The criteria for inspecting login requests, used by the ATP rule group to validate credentials usage\.   
*Required*: No  
*Type*: [RequestInspection](aws-properties-wafv2-webacl-requestinspection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesatpruleset-responseinspection"></a>
The criteria for inspecting responses to login requests, used by the ATP rule group to track login failure rates\.   
The ATP rule group evaluates the responses that your protected resources send back to client login attempts, keeping count of successful and failed attempts from each IP address and client session\. Using this information, the rule group labels and mitigates requests from client sessions and IP addresses that submit too many failed login attempts in a short amount of time\.   
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.
*Required*: No  
*Type*: [ResponseInspection](aws-properties-wafv2-webacl-responseinspection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)