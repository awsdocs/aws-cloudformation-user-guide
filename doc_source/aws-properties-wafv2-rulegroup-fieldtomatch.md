# AWS::WAFv2::RuleGroup FieldToMatch<a name="aws-properties-wafv2-rulegroup-fieldtomatch"></a>

The part of a web request that you want AWS WAF to inspect\. Include the single `FieldToMatch` type that you want to inspect, with additional specifications as needed, according to the type\. You specify a single request component in `FieldToMatch` for each rule statement that requires it\. To inspect more than one component of a web request, create a separate rule statement for each component\.

## Syntax<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax.json"></a>

```
{
  "[AllQueryArguments](#cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments)" : Json,
  "[Body](#cfn-wafv2-rulegroup-fieldtomatch-body)" : Json,
  "[JsonBody](#cfn-wafv2-rulegroup-fieldtomatch-jsonbody)" : JsonBody,
  "[Method](#cfn-wafv2-rulegroup-fieldtomatch-method)" : Json,
  "[QueryString](#cfn-wafv2-rulegroup-fieldtomatch-querystring)" : Json,
  "[SingleHeader](#cfn-wafv2-rulegroup-fieldtomatch-singleheader)" : Json,
  "[SingleQueryArgument](#cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument)" : Json,
  "[UriPath](#cfn-wafv2-rulegroup-fieldtomatch-uripath)" : Json
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax.yaml"></a>

```
  [AllQueryArguments](#cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments): Json
  [Body](#cfn-wafv2-rulegroup-fieldtomatch-body): Json
  [JsonBody](#cfn-wafv2-rulegroup-fieldtomatch-jsonbody): 
    JsonBody
  [Method](#cfn-wafv2-rulegroup-fieldtomatch-method): Json
  [QueryString](#cfn-wafv2-rulegroup-fieldtomatch-querystring): Json
  [SingleHeader](#cfn-wafv2-rulegroup-fieldtomatch-singleheader): Json
  [SingleQueryArgument](#cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument): Json
  [UriPath](#cfn-wafv2-rulegroup-fieldtomatch-uripath): Json
```

## Properties<a name="aws-properties-wafv2-rulegroup-fieldtomatch-properties"></a>

`AllQueryArguments`  <a name="cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments"></a>
Inspect all query arguments\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-wafv2-rulegroup-fieldtomatch-body"></a>
Inspect the request body, which immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Note that only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection by the underlying host service\. If you don't need to inspect more than 8 KB, you can guarantee that you don't allow additional bytes in by combining a statement that inspects the body of the web request, such as the `ByteMatchStatement` or `RegexPatternSetReferenceStatement`, with a `SizeConstraintStatement` that enforces an 8 KB size limit on the body of the request\. AWS WAF doesn't support inspecting the entire contents of web requests whose bodies exceed the 8 KB limit\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonBody`  <a name="cfn-wafv2-rulegroup-fieldtomatch-jsonbody"></a>
Inspect the request body as JSON\. The request body immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Note that only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection by the underlying host service\. If you don't need to inspect more than 8 KB, you can guarantee that you don't allow additional bytes in by combining a statement that inspects the body of the web request, such as the `ByteMatchStatement` or `RegexPatternSetReferenceStatement`, with a `SizeConstraintStatement` that enforces an 8 KB size limit on the body of the request\. AWS WAF doesn't support inspecting the entire contents of web requests whose bodies exceed the 8 KB limit\.  
*Required*: No  
*Type*: [JsonBody](aws-properties-wafv2-rulegroup-jsonbody.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-wafv2-rulegroup-fieldtomatch-method"></a>
Inspect the HTTP method\. The method indicates the type of operation that the request is asking the origin to perform\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-rulegroup-fieldtomatch-querystring"></a>
Inspect the query string\. This is the part of a URL that appears after a `?` character, if any\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleHeader`  <a name="cfn-wafv2-rulegroup-fieldtomatch-singleheader"></a>
Inspect a single header\. Provide the name of the header to inspect, for example, `User-Agent` or `Referer`\. This setting isn't case sensitive\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleQueryArgument`  <a name="cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument"></a>
Inspect a single query argument\. Provide the name of the query argument to inspect, such as *UserName* or *SalesRegion*\. The name can be up to 30 characters long and isn't case sensitive\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-rulegroup-fieldtomatch-uripath"></a>
Inspect the request URI path\. This is the part of a web request that identifies a resource, for example, `/images/daily-ad.jpg`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples"></a>



### Set the field to match to `QueryString`<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_QueryString_"></a>

The following shows an example field to match specification for a setting that doesn't requires additional configuration\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_QueryString_--yaml"></a>

```
FieldToMatch:
  QueryString: {}
```

#### JSON<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_QueryString_--json"></a>

```
"FieldToMatch": 
    { 
         "QueryString": {} 
    }
```

### Set the field to match to `Method`<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_Method_"></a>

The following shows an example field to match specification for a setting that has additional configuration requirements\. 

#### YAML<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_Method_--yaml"></a>

```
FieldToMatch:
  Method:
     Name: DELETE
```

#### JSON<a name="aws-properties-wafv2-rulegroup-fieldtomatch--examples--Set_the_field_to_match_to_Method_--json"></a>

```
"FieldToMatch": 
{ 
    "Method": 
    { 
         "Name": "DELETE" 
    } 
}
```