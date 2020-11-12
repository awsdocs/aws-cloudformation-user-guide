# AWS::WAFv2::WebACL FieldToMatch<a name="aws-properties-wafv2-webacl-fieldtomatch"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The part of a web request that you want AWS WAF to inspect\. Include the `FieldToMatch` types that you want to inspect, with additional specifications as needed, according to the type\. 

## Syntax<a name="aws-properties-wafv2-webacl-fieldtomatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-fieldtomatch-syntax.json"></a>

```
{
  "[AllQueryArguments](#cfn-wafv2-webacl-fieldtomatch-allqueryarguments)" : Json,
  "[Body](#cfn-wafv2-webacl-fieldtomatch-body)" : Json,
  "[Method](#cfn-wafv2-webacl-fieldtomatch-method)" : Json,
  "[QueryString](#cfn-wafv2-webacl-fieldtomatch-querystring)" : Json,
  "[SingleHeader](#cfn-wafv2-webacl-fieldtomatch-singleheader)" : Json,
  "[SingleQueryArgument](#cfn-wafv2-webacl-fieldtomatch-singlequeryargument)" : Json,
  "[UriPath](#cfn-wafv2-webacl-fieldtomatch-uripath)" : Json
}
```

### YAML<a name="aws-properties-wafv2-webacl-fieldtomatch-syntax.yaml"></a>

```
  [AllQueryArguments](#cfn-wafv2-webacl-fieldtomatch-allqueryarguments): Json
  [Body](#cfn-wafv2-webacl-fieldtomatch-body): Json
  [Method](#cfn-wafv2-webacl-fieldtomatch-method): Json
  [QueryString](#cfn-wafv2-webacl-fieldtomatch-querystring): Json
  [SingleHeader](#cfn-wafv2-webacl-fieldtomatch-singleheader): Json
  [SingleQueryArgument](#cfn-wafv2-webacl-fieldtomatch-singlequeryargument): Json
  [UriPath](#cfn-wafv2-webacl-fieldtomatch-uripath): Json
```

## Properties<a name="aws-properties-wafv2-webacl-fieldtomatch-properties"></a>

`AllQueryArguments`  <a name="cfn-wafv2-webacl-fieldtomatch-allqueryarguments"></a>
Inspect all query arguments\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-wafv2-webacl-fieldtomatch-body"></a>
Inspect the request body, which immediately follows the request headers\. This is the part of a request that contains any additional data that you want to send to your web server as the HTTP request body, such as data from a form\.   
Note that only the first 8 KB \(8192 bytes\) of the request body are forwarded to AWS WAF for inspection\. If you don't need to inspect more than 8 KB, you can guarantee that you don't allow additional bytes in by combining a statement that inspects the body of the web request, such as ByteMatchStatement or RegexPatternSetReferenceStatement, with a SizeConstraintStatement that enforces an 8 KB size limit on the body of the request\. AWS WAF doesn't support inspecting the entire contents of web requests whose bodies exceed the 8 KB limit\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-wafv2-webacl-fieldtomatch-method"></a>
Inspect the HTTP method\. The method indicates the type of operation that the request is asking the origin to perform\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-webacl-fieldtomatch-querystring"></a>
Inspect the query string\. This is the part of a URL that appears after a `?` character, if any\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleHeader`  <a name="cfn-wafv2-webacl-fieldtomatch-singleheader"></a>
Inspect a single header\. Provide the name of the header to inspect, for example, `User-Agent` or `Referer`\. This setting isn't case sensitive\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleQueryArgument`  <a name="cfn-wafv2-webacl-fieldtomatch-singlequeryargument"></a>
Inspect a single query argument\. Provide the name of the query argument to inspect, such as *UserName* or *SalesRegion*\. The name can be up to 30 characters long and isn't case sensitive\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-webacl-fieldtomatch-uripath"></a>
Inspect the request URI path\. This is the part of a web request that identifies a resource, for example, `/images/daily-ad.jpg`\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)