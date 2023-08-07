# AWS::WAFv2::WebACL AWSManagedRulesACFPRuleSet<a name="aws-properties-wafv2-webacl-awsmanagedrulesacfpruleset"></a>

Not currently supported by AWS CloudFormation\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableRegexInPath`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-enableregexinpath"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistrationPagePath`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-registrationpagepath"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-requestinspection"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [RequestInspectionACFP](aws-properties-wafv2-webacl-requestinspectionacfp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseInspection`  <a name="cfn-wafv2-webacl-awsmanagedrulesacfpruleset-responseinspection"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ResponseInspection](aws-properties-wafv2-webacl-responseinspection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)