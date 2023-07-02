# AWS::WAFv2::WebACL AssociationConfig<a name="aws-properties-wafv2-webacl-associationconfig"></a>

Specifies custom configurations for the associations between the web ACL and protected resources\. 

Use this to customize the maximum size of the request body that your protected CloudFront distributions forward to AWS WAF for inspection\. The default is 16 KB \(16,384 kilobytes\)\. 

**Note**  
You are charged additional fees when your protected resources forward body sizes that are larger than the default\. For more information, see [AWS WAF Pricing](http://aws.amazon.com/waf/pricing/)\.

## Syntax<a name="aws-properties-wafv2-webacl-associationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-associationconfig-syntax.json"></a>

```
{
  "[RequestBody](#cfn-wafv2-webacl-associationconfig-requestbody)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-wafv2-webacl-associationconfig-syntax.yaml"></a>

```
  [RequestBody](#cfn-wafv2-webacl-associationconfig-requestbody): 
    Key: Value
```

## Properties<a name="aws-properties-wafv2-webacl-associationconfig-properties"></a>

`RequestBody`  <a name="cfn-wafv2-webacl-associationconfig-requestbody"></a>
Customizes the maximum size of the request body that your protected CloudFront distributions forward to AWS WAF for inspection\. The default size is 16 KB \(16,384 kilobytes\)\.   
You are charged additional fees when your protected resources forward body sizes that are larger than the default\. For more information, see [AWS WAF Pricing](http://aws.amazon.com/waf/pricing/)\.
*Required*: No  
*Type*: Map of [RequestBodyAssociatedResourceTypeConfig](aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)