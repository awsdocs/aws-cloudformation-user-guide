# Amazon API Gateway Stage MethodSetting<a name="aws-properties-apigateway-stage-methodsetting"></a>

The `MethodSetting` property type configures settings for all methods in an Amazon API Gateway \(API Gateway\) stage\.

The `MethodSettings` property of the [AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md) resource contains a list of `MethodSetting` property types\.

## Syntax<a name="w3ab2c21c14c36b7"></a>

### JSON<a name="aws-properties-apigateway-stage-methodsetting-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachedataencrypted)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachettlinseconds)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachingenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-datatraceenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-httpmethod)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-logginglevel)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-metricsenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-resourcepath)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-throttlingburstlimit)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-throttlingratelimit)" : Number
}
```

### YAML<a name="aws-properties-apigateway-stage-methodsetting-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachedataencrypted): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachettlinseconds): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-cachingenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-datatraceenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-httpmethod): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-logginglevel): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-metricsenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-resourcepath): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-throttlingburstlimit): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsetting-throttlingratelimit): Number
```

## Properties<a name="w3ab2c21c14c36b9"></a>

`CacheDataEncrypted`  
Indicates whether the cached responses are encrypted\.  
*Required: *No  
*Type*: Boolean

`CacheTtlInSeconds`  
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches responses\.  
*Required: *No  
*Type*: Integer

`CachingEnabled`  
Indicates whether responses are cached and returned for requests\. You must enable a cache cluster on the stage to cache responses\.  
*Required: *No  
*Type*: Boolean

`DataTraceEnabled`  
Indicates whether data trace logging is enabled for methods in the stage\. API Gateway pushes these logs to Amazon CloudWatch Logs\.  
*Required: *No  
*Type*: Boolean

`HttpMethod`  
The HTTP method\.  
*Required: *Yes  
*Type*: String

`LoggingLevel`  
The logging level for this method\. For valid values, see the `loggingLevel` property of the [Stage](http://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#loggingLevel) resource in the *Amazon API Gateway API Reference*\.  
*Required: *No  
*Type*: String

`MetricsEnabled`  
Indicates whether Amazon CloudWatch metrics are enabled for methods in the stage\.  
*Required: *No  
*Type*: Boolean

`ResourcePath`  
The resource path for this method\. Forward slashes \(`/`\) are encoded as `~1` and the initial slash must include a forward slash\. For example, the path value `/resource/subresource` must be encoded as `/~1resource~1subresource`\. To specify the root path, use only a slash \(`/`\)\.  
*Required: *Yes  
*Type*: String

`ThrottlingBurstLimit`  
The number of burst requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Integer

`ThrottlingRateLimit`  
The number of steady\-state requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Number