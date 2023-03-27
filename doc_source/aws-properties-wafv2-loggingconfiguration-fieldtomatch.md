# AWS::WAFv2::LoggingConfiguration FieldToMatch<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch"></a>

The parts of the request that you want to keep out of the logs\. This is used in the logging configuration `RedactedFields` specification\. 

Example JSON for a `QueryString` field to match: 

 ` "FieldToMatch": { "QueryString": {} }` 

Example JSON for a `Method` field to match specification:

 ` "FieldToMatch": { "Method": { "Name": "DELETE" } }` 

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax.json"></a>

```
{
  "[JsonBody](#cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody)" : JsonBody,
  "[Method](#cfn-wafv2-loggingconfiguration-fieldtomatch-method)" : Json,
  "[QueryString](#cfn-wafv2-loggingconfiguration-fieldtomatch-querystring)" : Json,
  "[SingleHeader](#cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader)" : SingleHeader,
  "[UriPath](#cfn-wafv2-loggingconfiguration-fieldtomatch-uripath)" : Json
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-syntax.yaml"></a>

```
  [JsonBody](#cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody): 
    JsonBody
  [Method](#cfn-wafv2-loggingconfiguration-fieldtomatch-method): Json
  [QueryString](#cfn-wafv2-loggingconfiguration-fieldtomatch-querystring): Json
  [SingleHeader](#cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader): 
    SingleHeader
  [UriPath](#cfn-wafv2-loggingconfiguration-fieldtomatch-uripath): Json
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch-properties"></a>

`JsonBody`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-jsonbody"></a>
Redact the request body JSON\.   
*Required*: No  
*Type*: [JsonBody](aws-properties-wafv2-loggingconfiguration-jsonbody.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-method"></a>
Redact the indicated HTTP method\. The method indicates the type of operation that the request is asking the origin to perform\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-querystring"></a>
Redact the query string\. This is the part of a URL that appears after a `?` character, if any\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleHeader`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader"></a>
Redact a single header\. Provide the name of the header to inspect, for example, `User-Agent` or `Referer`\. This setting isn't case sensitive\.  
Example JSON: `"SingleHeader": { "Name": "haystack" }`   
*Required*: No  
*Type*: [SingleHeader](aws-properties-wafv2-loggingconfiguration-singleheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-uripath"></a>
Redact the request URI path\. This is the part of the web request that identifies a resource, for example, `/images/daily-ad.jpg`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)