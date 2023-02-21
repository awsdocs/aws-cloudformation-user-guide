# AWS::WAFv2::WebACL AllowAction<a name="aws-properties-wafv2-webacl-allowaction"></a>

Specifies that AWS WAF should allow the request and optionally defines additional custom handling for the request\.

This is used in the context of other settings, for example to specify values for a rule action or a web ACL default action\. 

## Syntax<a name="aws-properties-wafv2-webacl-allowaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-allowaction-syntax.json"></a>

```
{
  "[CustomRequestHandling](#cfn-wafv2-webacl-allowaction-customrequesthandling)" : CustomRequestHandling
}
```

### YAML<a name="aws-properties-wafv2-webacl-allowaction-syntax.yaml"></a>

```
  [CustomRequestHandling](#cfn-wafv2-webacl-allowaction-customrequesthandling): 
    CustomRequestHandling
```

## Properties<a name="aws-properties-wafv2-webacl-allowaction-properties"></a>

`CustomRequestHandling`  <a name="cfn-wafv2-webacl-allowaction-customrequesthandling"></a>
Defines custom handling for the web request\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomRequestHandling](aws-properties-wafv2-webacl-customrequesthandling.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-allowaction--examples"></a>



### Set an allow action<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_"></a>

The following shows an example allow action specification\. 

#### YAML<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_--yaml"></a>

```
Action:
  Allow: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_--json"></a>

```
"Action": {
  "Allow": {}
}
```

### Set an allow action with a custom request setting<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_with_a_custom_request_setting"></a>

The following shows an example allow action specification with custom request handling\. 

#### YAML<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_with_a_custom_request_setting--yaml"></a>

```
Allow:
  CustomRequestHandling:
    InsertHeaders:
      - Name: AllowActionHeader1Name
        Value: AllowActionHeader1Value
      - Name: AllowActionHeader2Name
        Value: AllowActionHeader2Value
```

#### JSON<a name="aws-properties-wafv2-webacl-allowaction--examples--Set_an_allow_action_with_a_custom_request_setting--json"></a>

```
"Allow": {
   "CustomRequestHandling": {
     "InsertHeaders": [
       {
         "Name": "AllowActionHeader1Name",
         "Value": "AllowActionHeader1Value"
       },
       {
         "Name": "AllowActionHeader2Name",
         "Value": "AllowActionHeader2Value"
       }
     ]
   }
}
```