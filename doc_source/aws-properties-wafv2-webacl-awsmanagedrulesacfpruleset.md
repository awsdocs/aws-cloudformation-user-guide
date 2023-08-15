# AWS::WAFv2::WebACL AWSManagedRulesACFPRuleSet<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset"></a>

Details for your use of the account creation fraud prevention managed rule group, `AWSManagedRulesACFPRuleSet`\. This configuration is used in `ManagedRuleGroupConfig`\. 

## Syntax<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset-syntax.json"></a>

```
{
  "[CreationPath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-creationpath)" : String,
  "[EnableRegexInPath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-enableregexinpath)" : Boolean,
  "[RegistrationPagePath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-registrationpagepath)" : String,
  "[RequestInspection](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-requestinspection)" : RequestInspectionACFP,
  "[ResponseInspection](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-responseinspection)" : ResponseInspection
}
```

### YAML<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset-syntax.yaml"></a>

```
  [CreationPath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-creationpath): String
  [EnableRegexInPath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-enableregexinpath): Boolean
  [RegistrationPagePath](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-registrationpagepath): String
  [RequestInspection](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-requestinspection): 
    RequestInspectionACFP
  [ResponseInspection](#cfn-wafv2-webacl-awsmanagedrulesacfpruleset-responseinspection): 
    ResponseInspection
```

## Properties<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset-properties"></a>

`CreationPath`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-creationpath"></a>
The path of the account creation endpoint for your application\. This is the page on your website that accepts the completed registration form for a new user\. This page must accept `POST` requests\.  
For example, for the URL `https://example.com/web/signup`, you would provide the path `/web/signup`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableRegexInPath`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-enableregexinpath"></a>
Allow the use of regular expressions in the registration page path and the account creation path\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistrationPagePath`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-registrationpagepath"></a>
The path of the account registration endpoint for your application\. This is the page on your website that presents the registration form to new users\.   
This page must accept `GET` text/html requests\.
For example, for the URL `https://example.com/web/register`, you would provide the path `/web/register`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-requestinspection"></a>
The criteria for inspecting account creation requests, used by the ACFP rule group to validate and track account creation attempts\.   
*Required*: Yes  
*Type*: [RequestInspectionACFP](aws-properties-wafv2-webacl-requestinspectionacfp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-responseinspection"></a>
The criteria for inspecting responses to account creation requests, used by the ACFP rule group to track account creation success rates\.   
Response inspection is available only in web ACLs that protect Amazon CloudFront distributions\.
The ACFP rule group evaluates the responses that your protected resources send back to client account creation attempts, keeping count of successful and failed attempts from each IP address and client session\. Using this information, the rule group labels and mitigates requests from client sessions and IP addresses that have had too many successful account creation attempts in a short amount of time\.   
*Required*: No  
*Type*: [ResponseInspection](aws-properties-wafv2-webacl-responseinspection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)