# AWS::WAFv2::LoggingConfiguration FieldToMatch<a name="aws-properties-wafv2-loggingconfiguration-fieldtomatch"></a>

The parts of the request that you want to keep out of the logs\. For example, if you redact the `SingleHeader` field, the `HEADER` field in the firehose will be `xxx`\. 

JSON specification for a `QueryString` field to match: 

 `"FieldToMatch": { "QueryString": {} }` 

Example JSON for a `Method` field to match specification:

 `"FieldToMatch": { "Method": { "Name": "DELETE" } }` 

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
Redact the JSON body from the logs\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-method"></a>
Redact the method from the logs\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-querystring"></a>
Redact the query string from the logs\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleHeader`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-singleheader"></a>
Redact the header from the logs\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-loggingconfiguration-fieldtomatch-uripath"></a>
Redact the URI path from the logs\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)