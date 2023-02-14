# AWS::WAFv2::LoggingConfiguration FieldToMatch<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch"></a>

The part of a web request that you want AWS WAF to inspect\. Include the single `FieldToMatch` type that you want to inspect, with additional specifications as needed, according to the type\. You specify a single request component in `FieldToMatch` for each rule statement that requires it\. To inspect more than one component of a web request, create a separate rule statement for each component\.

JSON specification for a `QueryString` field to match: 

 ` "FieldToMatch": { "QueryString": {} }` 

Example JSON for a `Method` field to match specification:

 ` "FieldToMatch": { "Method": { "Name": "DELETE" } }` 

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax.json"></a>

```
{
  "[JsonBody](#cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody)" : Json,
  "[Method](#cfn-wafv2-loggingconfiguration-fieldtomatch-method)" : Json,
  "[QueryString](#cfn-wafv2-loggingconfiguration-fieldtomatch-querystring)" : Json,
  "[SingleHeader](#cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader)" : Json,
  "[UriPath](#cfn-wafv2-loggingconfiguration-fieldtomatch-uripath)" : Json
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax.yaml"></a>

```
  [JsonBody](#cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody): 
    Json
  [Method](#cfn-wafv2-loggingconfiguration-fieldtomatch-method): Json
  [QueryString](#cfn-wafv2-loggingconfiguration-fieldtomatch-querystring): Json
  [SingleHeader](#cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader): Json
  [UriPath](#cfn-wafv2-loggingconfiguration-fieldtomatch-uripath): Json
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-properties"></a>

`JsonBody`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody"></a>
Inspect the request body as JSON\. The request body immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Note that only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection by the underlying host service\. If you don't need to inspect more than 8 KB, you can guarantee that you don't allow additional bytes in by combining a statement that inspects the body of the web request, such as [ByteMatchStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-statement.html#cfn-wafv2-rulegroup-statement-bytematchstatement) or [RegexPatternSetReferenceStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-statement.html#cfn-wafv2-rulegroup-statement-regexpatternsetreferencestatement), with a [SizeConstraintStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-statement.html#cfn-wafv2-rulegroup-statement-sizeconstraintstatement) that enforces an 8 KB size limit on the body of the request\. AWS WAF doesn't support inspecting the entire contents of web requests whose bodies exceed the 8 KB limit\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-method"></a>
Inspect the HTTP method\. The method indicates the type of operation that the request is asking the origin to perform\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-querystring"></a>
Inspect the query string\. This is the part of a URL that appears after a `?` character, if any\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleHeader`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader"></a>
Inspect a single header\. Provide the name of the header to inspect, for example, `User-Agent` or `Referer`\. This setting isn't case sensitive\.  
Example JSON: `"SingleHeader": { "Name": "haystack" }`   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-uripath"></a>
Inspect the request URI path\. This is the part of a web request that identifies a resource, for example, `/images/daily-ad.jpg`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)