# AWS::WAFv2::WebACL CountAction<a name="aws-properties-wafv2-webacl-countaction"></a>

Specifies that AWS WAF should count the request\. Optionally defines additional custom handling for the request\.

This is used in the context of other settings, for example to specify values for a rule action or a web ACL default action\. 

## Syntax<a name="aws-properties-wafv2-webacl-countaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-countaction-syntax.json"></a>

```
{
  "[CustomRequestHandling](#cfn-wafv2-webacl-countaction-customrequesthandling)" : CustomRequestHandling
}
```

### YAML<a name="aws-properties-wafv2-webacl-countaction-syntax.yaml"></a>

```
  [CustomRequestHandling](#cfn-wafv2-webacl-countaction-customrequesthandling): 
    CustomRequestHandling
```

## Properties<a name="aws-properties-wafv2-webacl-countaction-properties"></a>

`CustomRequestHandling`  <a name="cfn-wafv2-webacl-countaction-customrequesthandling"></a>
Defines custom handling for the web request\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomRequestHandling](aws-properties-wafv2-webacl-customrequesthandling.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-countaction--examples"></a>



### Set an count action<a name="aws-properties-wafv2-webacl-countaction--examples--Set_an_count_action_"></a>

The following shows an example count action specification\. 

#### YAML<a name="aws-properties-wafv2-webacl-countaction--examples--Set_an_count_action_--yaml"></a>

```
Action:
  Count: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-countaction--examples--Set_an_count_action_--json"></a>

```
"Action": {
  "Count": {}
}
```