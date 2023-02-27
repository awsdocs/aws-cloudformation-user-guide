# AWS::WAFv2::WebACL CustomResponseBody<a name="aws-properties-wafv2-webacl-customresponsebody"></a>

The response body to use in a custom response to a web request\. This is referenced by key from [CustomResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-blockaction.html#cfn-wafv2-webacl-blockaction-customresponse) `CustomResponseBodyKey`\.

## Syntax<a name="aws-properties-wafv2-webacl-customresponsebody-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-customresponsebody-syntax.json"></a>

```
{
  "[Content](#cfn-wafv2-webacl-customresponsebody-content)" : String,
  "[ContentType](#cfn-wafv2-webacl-customresponsebody-contenttype)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-customresponsebody-syntax.yaml"></a>

```
  [Content](#cfn-wafv2-webacl-customresponsebody-content): String
  [ContentType](#cfn-wafv2-webacl-customresponsebody-contenttype): String
```

## Properties<a name="aws-properties-wafv2-webacl-customresponsebody-properties"></a>

`Content`  <a name="cfn-wafv2-webacl-customresponsebody-content"></a>
The payload of the custom response\.   
You can use JSON escape strings in JSON content\. To do this, you must specify JSON content in the `ContentType` setting\.   
For information about the limits on count and size for custom request and response settings, see [AWS WAF quotas](https://docs.aws.amazon.com/waf/latest/developerguide/limits.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `10240`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentType`  <a name="cfn-wafv2-webacl-customresponsebody-contenttype"></a>
The type of content in the payload that you are defining in the `Content` string\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `APPLICATION_JSON | TEXT_HTML | TEXT_PLAIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)