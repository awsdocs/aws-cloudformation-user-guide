# AWS::WAFv2::LoggingConfiguration SingleHeader<a name="aws-properties-wafv2-loggingconfiguration-singleheader"></a>

Inspect one of the headers in the web request, identified by name, for example, `User-Agent` or `Referer`\. The name isn't case sensitive\.

You can filter and inspect all headers with the `FieldToMatch` setting `Headers`\.

This is used to indicate the web request component to inspect, in the `FieldToMatch` specification\. 

Example JSON: `"SingleHeader": { "Name": "haystack" }` 

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-singleheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-singleheader-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-loggingconfiguration-singleheader-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-singleheader-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-loggingconfiguration-singleheader-name): String
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-singleheader-properties"></a>

`Name`  <a name="cfn-wafv2-loggingconfiguration-singleheader-name"></a>
The name of the query header to inspect\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)