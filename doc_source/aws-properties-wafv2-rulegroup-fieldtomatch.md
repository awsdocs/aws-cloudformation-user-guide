# AWS::WAFv2::RuleGroup FieldToMatch<a name="aws-properties-wafv2-rulegroup-fieldtomatch"></a>

The part of the web request that you want AWS WAF to inspect\. Include the single `FieldToMatch` type that you want to inspect, with additional specifications as needed, according to the type\. You specify a single request component in `FieldToMatch` for each rule statement that requires it\. To inspect more than one component of the web request, create a separate rule statement for each component\.

Example JSON for a `QueryString` field to match: 

 ` "FieldToMatch": { "QueryString": {} }` 

Example JSON for a `Method` field to match specification:

 ` "FieldToMatch": { "Method": { "Name": "DELETE" } }` 

## Syntax<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax.json"></a>

```
{
  "[AllQueryArguments](#cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments)" : Json,
  "[Body](#cfn-wafv2-rulegroup-fieldtomatch-body)" : Body,
  "[Cookies](#cfn-wafv2-rulegroup-fieldtomatch-cookies)" : Cookies,
  "[Headers](#cfn-wafv2-rulegroup-fieldtomatch-headers)" : Headers,
  "[JsonBody](#cfn-wafv2-rulegroup-fieldtomatch-jsonbody)" : JsonBody,
  "[Method](#cfn-wafv2-rulegroup-fieldtomatch-method)" : Json,
  "[QueryString](#cfn-wafv2-rulegroup-fieldtomatch-querystring)" : Json,
  "[SingleHeader](#cfn-wafv2-rulegroup-fieldtomatch-singleheader)" : SingleHeader,
  "[SingleQueryArgument](#cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument)" : SingleQueryArgument,
  "[UriPath](#cfn-wafv2-rulegroup-fieldtomatch-uripath)" : Json
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-fieldtomatch-syntax.yaml"></a>

```
  [AllQueryArguments](#cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments): Json
  [Body](#cfn-wafv2-rulegroup-fieldtomatch-body): 
    Body
  [Cookies](#cfn-wafv2-rulegroup-fieldtomatch-cookies): 
    Cookies
  [Headers](#cfn-wafv2-rulegroup-fieldtomatch-headers): 
    Headers
  [JsonBody](#cfn-wafv2-rulegroup-fieldtomatch-jsonbody): 
    JsonBody
  [Method](#cfn-wafv2-rulegroup-fieldtomatch-method): Json
  [QueryString](#cfn-wafv2-rulegroup-fieldtomatch-querystring): Json
  [SingleHeader](#cfn-wafv2-rulegroup-fieldtomatch-singleheader): 
    SingleHeader
  [SingleQueryArgument](#cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument): 
    SingleQueryArgument
  [UriPath](#cfn-wafv2-rulegroup-fieldtomatch-uripath): Json
```

## Properties<a name="aws-properties-wafv2-rulegroup-fieldtomatch-properties"></a>

`AllQueryArguments`  <a name="cfn-wafv2-rulegroup-fieldtomatch-allqueryarguments"></a>
Inspect all query arguments\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-wafv2-rulegroup-fieldtomatch-body"></a>
Inspect the request body as plain text\. The request body immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection by the underlying host service\. For information about how to handle oversized request bodies, see the `Body` object configuration\.   
*Required*: No  
*Type*: [Body](aws-properties-wafv2-rulegroup-body.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cookies`  <a name="cfn-wafv2-rulegroup-fieldtomatch-cookies"></a>
Inspect the request cookies\. You must configure scope and pattern matching filters in the `Cookies` object, to define the set of cookies and the parts of the cookies that AWS WAF inspects\.   
Only the first 8 KB \(8192 bytes\) of a request's cookies and only the first 200 cookies are forwarded to AWS WAF for inspection by the underlying host service\. You must configure how to handle any oversize cookie content in the `Cookies` object\. AWS WAF applies the pattern matching filters to the cookies that it receives from the underlying host service\.   
*Required*: No  
*Type*: [Cookies](aws-properties-wafv2-rulegroup-cookies.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Headers`  <a name="cfn-wafv2-rulegroup-fieldtomatch-headers"></a>
Inspect the request headers\. You must configure scope and pattern matching filters in the `Headers` object, to define the set of headers to and the parts of the headers that AWS WAF inspects\.   
Only the first 8 KB \(8192 bytes\) of a request's headers and only the first 200 headers are forwarded to AWS WAF for inspection by the underlying host service\. You must configure how to handle any oversize header content in the `Headers` object\. AWS WAF applies the pattern matching filters to the headers that it receives from the underlying host service\.   
*Required*: No  
*Type*: [Headers](aws-properties-wafv2-rulegroup-headers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonBody`  <a name="cfn-wafv2-rulegroup-fieldtomatch-jsonbody"></a>
Inspect the request body as JSON\. The request body immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection by the underlying host service\. For information about how to handle oversized request bodies, see the `JsonBody` object configuration\.   
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
Example JSON: `"SingleHeader": { "Name": "haystack" }`   
Alternately, you can filter and inspect all headers with the `Headers` `FieldToMatch` setting\.   
*Required*: No  
*Type*: [SingleHeader](aws-properties-wafv2-rulegroup-singleheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleQueryArgument`  <a name="cfn-wafv2-rulegroup-fieldtomatch-singlequeryargument"></a>
Inspect a single query argument\. Provide the name of the query argument to inspect, such as *UserName* or *SalesRegion*\. The name can be up to 30 characters long and isn't case sensitive\.   
Example JSON: `"SingleQueryArgument": { "Name": "myArgument" }`   
*Required*: No  
*Type*: [SingleQueryArgument](aws-properties-wafv2-rulegroup-singlequeryargument.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-rulegroup-fieldtomatch-uripath"></a>
Inspect the request URI path\. This is the part of the web request that identifies a resource, for example, `/images/daily-ad.jpg`\.  
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