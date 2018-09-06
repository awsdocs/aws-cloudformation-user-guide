# Amazon API Gateway Deployment MethodSetting<a name="aws-properties-apigateway-deployment-stagedescription-methodsetting"></a>

The `MethodSetting` property type configures settings for all methods in an Amazon API Gateway \(API Gateway\) stage\.

The `MethodSettings` property of the [Amazon API Gateway Deployment StageDescription](aws-properties-apigateway-deployment-stagedescription.md) property type contains a list of `MethodSetting` property types\.

## Syntax<a name="w3ab2c21c14c17b7"></a>

### JSON<a name="aws-properties-apigateway-deployment-stagedescription-methodsetting-syntax.json"></a>

```
{
  "[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-methodsetting-cachedataencrypted)" : Boolean,
  "[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-methodsetting-cachettlinseconds)" : Integer,
  "[CachingEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-cachingenabled)" : Boolean,
  "[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-datatraceenabled)" : Boolean,
  "[HttpMethod](#cfn-apigateway-deployment-stagedescription-methodsetting-httpmethod)" : String,
  "[LoggingLevel](#cfn-apigateway-deployment-stagedescription-methodsetting-logginglevel)" : String,
  "[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-metricsenabled)" : Boolean,
  "[ResourcePath](#cfn-apigateway-deployment-stagedescription-methodsetting-resourcepath)" : String,
  "[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-methodsetting-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-methodsetting-throttlingratelimit)" : Number
}
```

### YAML<a name="aws-properties-apigateway-deployment-stagedescription-methodsetting-syntax.yaml"></a>

```
[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-methodsetting-cachedataencrypted): Boolean
[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-methodsetting-cachettlinseconds): Integer
[CachingEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-cachingenabled): Boolean
[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-datatraceenabled): Boolean
[HttpMethod](#cfn-apigateway-deployment-stagedescription-methodsetting-httpmethod): String
[LoggingLevel](#cfn-apigateway-deployment-stagedescription-methodsetting-logginglevel): String
[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-methodsetting-metricsenabled): Boolean
[ResourcePath](#cfn-apigateway-deployment-stagedescription-methodsetting-resourcepath): String
[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-methodsetting-throttlingburstlimit): Integer
[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-methodsetting-throttlingratelimit): Number
```

## Properties<a name="w3ab2c21c14c17b9"></a>

`CacheDataEncrypted`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-cachedataencrypted"></a>
Indicates whether the cached responses are encrypted\.  
*Required*: No  
*Type*: Boolean

`CacheTtlInSeconds`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-cachettlinseconds"></a>
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches responses\.  
*Required*: No  
*Type*: Integer

`CachingEnabled`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-cachingenabled"></a>
Indicates whether responses are cached and returned for requests\. You must enable a cache cluster on the stage to cache responses\. For more information, see [Enable API Gateway Caching in a Stage to Enhance API Performance](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Boolean

`DataTraceEnabled`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-datatraceenabled"></a>
Indicates whether data trace logging is enabled for methods in the stage\. API Gateway pushes these logs to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean

`HttpMethod`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-httpmethod"></a>
The HTTP method\.  
*Required*: No  
*Type*: String

`LoggingLevel`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-logginglevel"></a>
The logging level for this method\. For valid values, see the `loggingLevel` property of the [Stage](http://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#loggingLevel) resource in the *Amazon API Gateway API Reference*\.  
*Required*: No  
*Type*: String

`MetricsEnabled`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-metricsenabled"></a>
Indicates whether Amazon CloudWatch metrics are enabled for methods in the stage\.  
*Required*: No  
*Type*: Boolean

`ResourcePath`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-resourcepath"></a>
The resource path for this method\. Forward slashes \(`/`\) are encoded as `~1` and the initial slash must include a forward slash\. For example, the path value `/resource/subresource` must be encoded as `/~1resource~1subresource`\. To specify the root path, use only a slash \(`/`\)\.  
*Required*: No  
*Type*: String

`ThrottlingBurstLimit`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-throttlingburstlimit"></a>
The number of burst requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Integer

`ThrottlingRateLimit`  <a name="cfn-apigateway-deployment-stagedescription-methodsetting-throttlingratelimit"></a>
The number of steady\-state requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Number