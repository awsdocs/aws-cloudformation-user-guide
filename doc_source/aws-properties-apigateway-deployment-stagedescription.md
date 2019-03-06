# Amazon API Gateway Deployment StageDescription<a name="aws-properties-apigateway-deployment-stagedescription"></a>

`StageDescription` is a property of the [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md) resource that configures an Amazon API Gateway \(API Gateway\) deployment stage\.

## Syntax<a name="w13ab1c21c10c20c33c23b5"></a>

### JSON<a name="aws-properties-apigateway-deployment-stagedescription-syntax.json"></a>

```
{
  "[AccessLogSetting](#cfn-apigateway-deployment-stagedescription-accesslogsetting)" : [AccessLogSetting](aws-properties-apigateway-deployment-accesslogsetting.md),
  "[CacheClusterEnabled](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled)" : Boolean,
  "[CacheClusterSize](#cfn-apigateway-deployment-stagedescription-cacheclustersize)" : String,
  "[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-cachedataencrypted)" : Boolean,
  "[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-cachettlinseconds)" : Integer,
  "[CachingEnabled](#cfn-apigateway-deployment-stagedescription-cachingenabled)" : Boolean,
  "[CanarySetting](#cfn-apigateway-deployment-stagedescription-canarysetting)" : [CanarySetting](aws-properties-apigateway-deployment-canarysetting.md),
  "[ClientCertificateId](#cfn-apigateway-deployment-stagedescription-clientcertificateid)" : String,
  "[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-datatraceenabled)" : Boolean,
  "[Description](#cfn-apigateway-deployment-stagedescription-description)" : String,
  "[DocumentationVersion](#cfn-apigateway-deployment-stagedescription-documentationversion)" : String,
  "[LoggingLevel](#cfn-apigateway-deployment-stagedescription-logginglevel)" : String,
  "[MethodSettings](#cfn-apigateway-deployment-stagedescription-methodsettings)" : [ [*MethodSetting*](aws-properties-apigateway-deployment-stagedescription-methodsetting.md), ... ],
  "[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-metricsenabled)" : Boolean,
  "[Tags](#cfn-apigateway-deployment-tags)" : [ [Resource Tag](aws-properties-resource-tags.md), ... ],
  "[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-throttlingratelimit)" : Number,
  "[TracingEnabled](#cfn-apigateway-deployment-stagedescription-tracingenabled)" : Boolean,
  "[Variables](#cfn-apigateway-deployment-stagedescription-variables)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-apigateway-deployment-stagedescription-syntax.yaml"></a>

```
[AccessLogSetting](#cfn-apigateway-deployment-stagedescription-accesslogsetting): [AccessLogSetting](aws-properties-apigateway-deployment-accesslogsetting.md)
[CacheClusterEnabled](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled): Boolean
[CacheClusterSize](#cfn-apigateway-deployment-stagedescription-cacheclustersize): String
[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-cachedataencrypted): Boolean
[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-cachettlinseconds): Integer
[CachingEnabled](#cfn-apigateway-deployment-stagedescription-cachingenabled): Boolean
[CanarySetting](#cfn-apigateway-deployment-stagedescription-canarysetting): [CanarySetting](aws-properties-apigateway-deployment-canarysetting.md)
[ClientCertificateId](#cfn-apigateway-deployment-stagedescription-clientcertificateid): String
[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-datatraceenabled): Boolean
[Description](#cfn-apigateway-deployment-stagedescription-description): String
[LoggingLevel](#cfn-apigateway-deployment-stagedescription-logginglevel): String
[MethodSettings](#cfn-apigateway-deployment-stagedescription-methodsettings):
  - [*MethodSetting*](aws-properties-apigateway-deployment-stagedescription-methodsetting.md)
[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-metricsenabled): Boolean
[Tags](#cfn-apigateway-deployment-tags): 
  - [Resource Tag](aws-properties-resource-tags.md)
[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit): Integer
[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-throttlingratelimit): Number
[TracingEnabled](#cfn-apigateway-deployment-stagedescription-tracingenabled): Boolean
[Variables](#cfn-apigateway-deployment-stagedescription-variables):
  String: String
```

## Properties<a name="w13ab1c21c10c20c33c23b7"></a>

`AccessLogSetting`  <a name="cfn-apigateway-deployment-stagedescription-accesslogsetting"></a>
Specifies settings for logging access in this stage\.  
*Required*: No  
*Type*: [AccessLogSetting](aws-properties-apigateway-deployment-accesslogsetting.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CacheClusterEnabled`  <a name="cfn-apigateway-deployment-stagedescription-cacheclusterenabled"></a>
Indicates whether cache clustering is enabled for the stage\.  
*Required*: No  
*Type*: Boolean

`CacheClusterSize`  <a name="cfn-apigateway-deployment-stagedescription-cacheclustersize"></a>
The size of the stage's cache cluster\.  
*Required*: No  
*Type*: String

`CacheDataEncrypted`  <a name="cfn-apigateway-deployment-stagedescription-cachedataencrypted"></a>
Indicates whether the cached responses are encrypted\.  
*Required*: No  
*Type*: Boolean

`CacheTtlInSeconds`  <a name="cfn-apigateway-deployment-stagedescription-cachettlinseconds"></a>
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches responses\.  
*Required*: No  
*Type*: Integer

`CachingEnabled`  <a name="cfn-apigateway-deployment-stagedescription-cachingenabled"></a>
Indicates whether responses are cached and returned for requests\. You must enable a cache cluster on the stage to cache responses\. For more information, see [Enable API Gateway Caching in a Stage to Enhance API Performance](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Boolean

`CanarySetting`  <a name="cfn-apigateway-deployment-stagedescription-canarysetting"></a>
Specifies settings for the canary deployment in this stage\.  
*Required*: No  
*Type*: [CanarySetting](aws-properties-apigateway-deployment-canarysetting.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ClientCertificateId`  <a name="cfn-apigateway-deployment-stagedescription-clientcertificateid"></a>
The identifier of the client certificate that API Gateway uses to call your integration endpoints in the stage\.  
*Required*: No  
*Type*: String

`DataTraceEnabled`  <a name="cfn-apigateway-deployment-stagedescription-datatraceenabled"></a>
Indicates whether data trace logging is enabled for methods in the stage\. API Gateway pushes these logs to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean

`Description`  <a name="cfn-apigateway-deployment-stagedescription-description"></a>
A description of the purpose of the stage\.  
*Required*: No  
*Type*: String

`DocumentationVersion`  <a name="cfn-apigateway-deployment-stagedescription-documentationversion"></a>
The version identifier of the API documentation snapshot\.  
*Required*: No  
*Type*: String

`LoggingLevel`  <a name="cfn-apigateway-deployment-stagedescription-logginglevel"></a>
The logging level for this method\. For valid values, see the `loggingLevel` property of the [Stage](https://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#loggingLevel) resource in the *Amazon API Gateway API Reference*\.  
*Required*: No  
*Type*: String

`MethodSettings`  <a name="cfn-apigateway-deployment-stagedescription-methodsettings"></a>
Configures settings for all of the stage's methods\.  
*Required*: No  
*Type*: List of [MethodSetting](aws-properties-apigateway-deployment-stagedescription-methodsetting.md)

`MetricsEnabled`  <a name="cfn-apigateway-deployment-stagedescription-metricsenabled"></a>
Indicates whether Amazon CloudWatch metrics are enabled for methods in the stage\.  
*Required*: No  
*Type*: Boolean

`Tags`  <a name="cfn-apigateway-deployment-tags"></a>
An array of arbitrary tags \(key\-value pairs\) to associate with the stage\.  
*Required*: No  
*Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ThrottlingBurstLimit`  <a name="cfn-apigateway-deployment-stagedescription-throttlingburstlimit"></a>
The number of burst requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Integer

`ThrottlingRateLimit`  <a name="cfn-apigateway-deployment-stagedescription-throttlingratelimit"></a>
The number of steady\-state requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Number

`TracingEnabled`  <a name="cfn-apigateway-deployment-stagedescription-tracingenabled"></a>
Specifies whether active tracing with X\-ray is enabled for this stage\.  
For more information, see [Trace API Gateway API Execution with AWS X\-Ray](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-xray.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Variables`  <a name="cfn-apigateway-deployment-stagedescription-variables"></a>
A map that defines the stage variables\. Variable names must consist of alphanumeric characters, and the values must match the following regular expression: `[A-Za-z0-9-._~:/?#&amp;=,]+`\.  
*Required*: No  
*Type*: Mapping of key\-value pairs