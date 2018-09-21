# Amazon Simple Email Service ReceiptRule AddHeaderAction<a name="aws-properties-ses-receiptrule-addheaderaction"></a>

<a name="aws-properties-ses-receiptrule-addheaderaction-description"></a>The `AddHeaderAction` property type add a header to email it recieves on behalf of one or more email addresses or domains that you own\.

<a name="aws-properties-ses-receiptrule-addheaderaction-inheritance"></a> `AddHeaderAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-addheaderaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-addheaderaction-syntax.json"></a>

```
{
  "[HeaderValue](#cfn-ses-receiptrule-addheaderaction-headervalue)" : String,
  "[HeaderName](#cfn-ses-receiptrule-addheaderaction-headername)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-addheaderaction-syntax.yaml"></a>

```
[HeaderValue](#cfn-ses-receiptrule-addheaderaction-headervalue): String
[HeaderName](#cfn-ses-receiptrule-addheaderaction-headername): String
```

## Properties<a name="aws-properties-ses-receiptrule-addheaderaction-properties"></a>

`HeaderName`  <a name="cfn-ses-receiptrule-addheaderaction-headername"></a>
The name of the header to add\. Must be between 1 and 50 characters, inclusive, and consist of alphanumeric \(a\-z, A\-Z, 0\-9\) characters and dashes only\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HeaderValue`  <a name="cfn-ses-receiptrule-addheaderaction-headervalue"></a>
Must be less than 2048 characters, and must not contain newline characters \("\\r" or "\\n"\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-addheaderaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateReceiptRule](url-ses-api;API_CreateReceiptRule.html) in the *Amazon Simple Email Service API Reference*
+ [AddHeaderAction](url-ses-api;API_AddHeaderAction.html) in the *Amazon Simple Email Service API Reference*