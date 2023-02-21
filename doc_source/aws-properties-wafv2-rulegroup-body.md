# AWS::WAFv2::RuleGroup Body<a name="aws-properties-wafv2-rulegroup-body"></a>

Inspect the body of the web request\. The body immediately follows the request headers\.

This is used to indicate the web request component to inspect, in the [FieldToMatch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-xssmatchstatement.html#cfn-wafv2-rulegroup-xssmatchstatement-fieldtomatch) specification\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-body-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-body-syntax.json"></a>

```
{
  "[OversizeHandling](#cfn-wafv2-rulegroup-body-oversizehandling)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-body-syntax.yaml"></a>

```
  [OversizeHandling](#cfn-wafv2-rulegroup-body-oversizehandling): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-body-properties"></a>

`OversizeHandling`  <a name="cfn-wafv2-rulegroup-body-oversizehandling"></a>
What AWS WAF should do if the body is larger than AWS WAF can inspect\. AWS WAF does not support inspecting the entire contents of the body of a web request when the body exceeds 8 KB \(8192 bytes\)\. Only the first 8 KB of the request body are forwarded to AWS WAF by the underlying host service\.   
The options for oversize handling are the following:  
+  `CONTINUE` \- Inspect the body normally, according to the rule inspection criteria\. 
+  `MATCH` \- Treat the web request as matching the rule statement\. AWS WAF applies the rule action to the request\.
+  `NO_MATCH` \- Treat the web request as not matching the rule statement\.
You can combine the `MATCH` or `NO_MATCH` settings for oversize handling with your rule and web ACL action settings, so that you block any request whose body is over 8 KB\.   
Default: `CONTINUE`   
*Required*: No  
*Type*: String  
*Allowed values*: `CONTINUE | MATCH | NO_MATCH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-rulegroup-body--examples"></a>



### Set the Body specification<a name="aws-properties-wafv2-rulegroup-body--examples--Set_the_Body_specification_"></a>

The following shows an example Body field to match specification\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-body--examples--Set_the_Body_specification_--yaml"></a>

```
FieldToMatch:
  Body:
    OversizeHandling: MATCH
```

#### JSON<a name="aws-properties-wafv2-rulegroup-body--examples--Set_the_Body_specification_--json"></a>

```
"FieldToMatch": {
  "Body": {
    "OversizeHandling": "MATCH" 
  }
}
```