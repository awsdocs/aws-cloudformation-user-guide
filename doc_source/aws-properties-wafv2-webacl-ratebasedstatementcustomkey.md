# AWS::WAFv2::WebACL RateBasedStatementCustomKey<a name="aws-properties-wafv2-webacl-ratebasedstatementcustomkey"></a>

Specifies a single custom aggregate key for a rate\-base rule\. 

**Note**  
Web requests that are missing any of the components specified in the aggregation keys are omitted from the rate\-based rule evaluation and handling\. 

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatementcustomkey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatementcustomkey-syntax.json"></a>

```
{
  "[Cookie](#cfn-wafv2-webacl-ratebasedstatementcustomkey-cookie)" : RateLimitCookie,
  "[ForwardedIP](#cfn-wafv2-webacl-ratebasedstatementcustomkey-forwardedip)" : Json,
  "[Header](#cfn-wafv2-webacl-ratebasedstatementcustomkey-header)" : RateLimitHeader,
  "[HTTPMethod](#cfn-wafv2-webacl-ratebasedstatementcustomkey-httpmethod)" : Json,
  "[IP](#cfn-wafv2-webacl-ratebasedstatementcustomkey-ip)" : Json,
  "[LabelNamespace](#cfn-wafv2-webacl-ratebasedstatementcustomkey-labelnamespace)" : RateLimitLabelNamespace,
  "[QueryArgument](#cfn-wafv2-webacl-ratebasedstatementcustomkey-queryargument)" : RateLimitQueryArgument,
  "[QueryString](#cfn-wafv2-webacl-ratebasedstatementcustomkey-querystring)" : RateLimitQueryString,
  "[UriPath](#cfn-wafv2-webacl-ratebasedstatementcustomkey-uripath)" : RateLimitUriPath
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatementcustomkey-syntax.yaml"></a>

```
  [Cookie](#cfn-wafv2-webacl-ratebasedstatementcustomkey-cookie): 
    RateLimitCookie
  [ForwardedIP](#cfn-wafv2-webacl-ratebasedstatementcustomkey-forwardedip): Json
  [Header](#cfn-wafv2-webacl-ratebasedstatementcustomkey-header): 
    RateLimitHeader
  [HTTPMethod](#cfn-wafv2-webacl-ratebasedstatementcustomkey-httpmethod): Json
  [IP](#cfn-wafv2-webacl-ratebasedstatementcustomkey-ip): Json
  [LabelNamespace](#cfn-wafv2-webacl-ratebasedstatementcustomkey-labelnamespace): 
    RateLimitLabelNamespace
  [QueryArgument](#cfn-wafv2-webacl-ratebasedstatementcustomkey-queryargument): 
    RateLimitQueryArgument
  [QueryString](#cfn-wafv2-webacl-ratebasedstatementcustomkey-querystring): 
    RateLimitQueryString
  [UriPath](#cfn-wafv2-webacl-ratebasedstatementcustomkey-uripath): 
    RateLimitUriPath
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatementcustomkey-properties"></a>

`Cookie`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-cookie"></a>
Use the value of a cookie in the request as an aggregate key\. Each distinct value in the cookie contributes to the aggregation instance\. If you use a single cookie as your custom key, then each value fully defines an aggregation instance\.   
*Required*: No  
*Type*: [RateLimitCookie](aws-properties-wafv2-webacl-ratelimitcookie.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIP`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-forwardedip"></a>
Use the first IP address in an HTTP header as an aggregate key\. Each distinct forwarded IP address contributes to the aggregation instance\.  
When you specify an IP or forwarded IP in the custom key settings, you must also specify at least one other key to use\. You can aggregate on only the forwarded IP address by specifying `FORWARDED_IP` in your rate\-based statement's `AggregateKeyType`\.   
With this option, you must specify the header to use in the rate\-based rule's `ForwardedIPConfig` property\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Header`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-header"></a>
Use the value of a header in the request as an aggregate key\. Each distinct value in the header contributes to the aggregation instance\. If you use a single header as your custom key, then each value fully defines an aggregation instance\.   
*Required*: No  
*Type*: [RateLimitHeader](aws-properties-wafv2-webacl-ratelimitheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTPMethod`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-httpmethod"></a>
Use the request's HTTP method as an aggregate key\. Each distinct HTTP method contributes to the aggregation instance\. If you use just the HTTP method as your custom key, then each method fully defines an aggregation instance\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IP`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-ip"></a>
Use the request's originating IP address as an aggregate key\. Each distinct IP address contributes to the aggregation instance\.  
When you specify an IP or forwarded IP in the custom key settings, you must also specify at least one other key to use\. You can aggregate on only the IP address by specifying `IP` in your rate\-based statement's `AggregateKeyType`\.   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelNamespace`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-labelnamespace"></a>
Use the specified label namespace as an aggregate key\. Each distinct fully qualified label name that has the specified label namespace contributes to the aggregation instance\. If you use just one label namespace as your custom key, then each label name fully defines an aggregation instance\.   
This uses only labels that have been added to the request by rules that are evaluated before this rate\-based rule in the web ACL\.   
For information about label namespaces and names, see [Label syntax and naming requirements](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-label-requirements.html) in the * AWS WAF Developer Guide*\.  
*Required*: No  
*Type*: [RateLimitLabelNamespace](aws-properties-wafv2-webacl-ratelimitlabelnamespace.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryArgument`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-queryargument"></a>
Use the specified query argument as an aggregate key\. Each distinct value for the named query argument contributes to the aggregation instance\. If you use a single query argument as your custom key, then each value fully defines an aggregation instance\.   
*Required*: No  
*Type*: [RateLimitQueryArgument](aws-properties-wafv2-webacl-ratelimitqueryargument.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-querystring"></a>
Use the request's query string as an aggregate key\. Each distinct string contributes to the aggregation instance\. If you use just the query string as your custom key, then each string fully defines an aggregation instance\.   
*Required*: No  
*Type*: [RateLimitQueryString](aws-properties-wafv2-webacl-ratelimitquerystring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPath`  <a name="cfn-wafv2-webacl-ratebasedstatementcustomkey-uripath"></a>
Use the request's URI path as an aggregate key\. Each distinct URI path contributes to the aggregation instance\. If you use just the URI path as your custom key, then each URI path fully defines an aggregation instance\.   
*Required*: No  
*Type*: [RateLimitUriPath](aws-properties-wafv2-webacl-ratelimituripath.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)