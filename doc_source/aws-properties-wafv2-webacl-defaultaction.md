# AWS::WAFv2::WebACL DefaultAction<a name="aws-properties-wafv2-webacl-defaultaction"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

In a `WebACL`, this is the action that you want AWS WAF to perform when a web request doesn't match any of the rules in the `WebACL`\. The default action must be a terminating action, so count is not allowed\.

## Syntax<a name="aws-properties-wafv2-webacl-defaultaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-defaultaction-syntax.json"></a>

```
{
  "[Allow](#cfn-wafv2-webacl-defaultaction-allow)" : Json,
  "[Block](#cfn-wafv2-webacl-defaultaction-block)" : Json
}
```

### YAML<a name="aws-properties-wafv2-webacl-defaultaction-syntax.yaml"></a>

```
  [Allow](#cfn-wafv2-webacl-defaultaction-allow): Json
  [Block](#cfn-wafv2-webacl-defaultaction-block): Json
```

## Properties<a name="aws-properties-wafv2-webacl-defaultaction-properties"></a>

`Allow`  <a name="cfn-wafv2-webacl-defaultaction-allow"></a>
Specifies that AWS WAF should allow requests by default\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Block`  <a name="cfn-wafv2-webacl-defaultaction-block"></a>
Specifies that AWS WAF should block requests by default\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-defaultaction--examples"></a>



### Set a web ACL default action<a name="aws-properties-wafv2-webacl-defaultaction--examples--Set_a_web_ACL_default_action"></a>

The following shows an example web ACL default action specification, that sets the default action to "Block"\. 

#### YAML<a name="aws-properties-wafv2-webacl-defaultaction--examples--Set_a_web_ACL_default_action--yaml"></a>

```
      DefaultAction:
        Block: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-defaultaction--examples--Set_a_web_ACL_default_action--json"></a>

```
      "DefaultAction": {
          "Block": {}
        }
```