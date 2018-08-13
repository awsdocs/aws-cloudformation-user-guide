# Amazon API Gateway Deployment StageDescription<a name="aws-properties-apigateway-deployment-stagedescription"></a>

`StageDescription` is a property of the [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md) resource that configures an Amazon API Gateway \(API Gateway\) deployment stage\.

## Syntax<a name="w3ab2c21c14c15b5"></a>

### JSON<a name="aws-properties-apigateway-deployment-stagedescription-syntax.json"></a>

```
{
  "[CacheClusterEnabled](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled)" : Boolean,
  "[CacheClusterSize](#cfn-apigateway-deployment-stagedescription-cacheclustersize)" : String,
  "[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-cachedataencrypted)" : Boolean,
  "[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-cachettlinseconds)" : Integer,
  "[CachingEnabled](#cfn-apigateway-deployment-stagedescription-cachingenabled)" : Boolean,
  "[ClientCertificateId](#cfn-apigateway-deployment-stagedescription-clientcertificateid)" : String,
  "[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-datatraceenabled)" : Boolean,
  "[Description](#cfn-apigateway-deployment-stagedescription-description)" : String,
  "[DocumentationVersion](#cfn-apigateway-deployment-stagedescription-documentationversion)" : String,
  "[LoggingLevel](#cfn-apigateway-deployment-stagedescription-logginglevel)" : String,
  "[MethodSettings](#cfn-apigateway-deployment-stagedescription-methodsettings)" : [ [*MethodSetting*](aws-properties-apigateway-deployment-stagedescription-methodsetting.md), ... ],
  "[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-metricsenabled)" : Boolean,
  "[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-throttlingratelimit)" : Number,
  "[Variables](#cfn-apigateway-deployment-stagedescription-variables)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-apigateway-deployment-stagedescription-syntax.yaml"></a>

```
[CacheClusterEnabled](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled): Boolean
[CacheClusterSize](#cfn-apigateway-deployment-stagedescription-cacheclustersize): String
[CacheDataEncrypted](#cfn-apigateway-deployment-stagedescription-cachedataencrypted): Boolean
[CacheTtlInSeconds](#cfn-apigateway-deployment-stagedescription-cachettlinseconds): Integer
[CachingEnabled](#cfn-apigateway-deployment-stagedescription-cachingenabled): Boolean
[ClientCertificateId](#cfn-apigateway-deployment-stagedescription-clientcertificateid): String
[DataTraceEnabled](#cfn-apigateway-deployment-stagedescription-datatraceenabled): Boolean
[Description](#cfn-apigateway-deployment-stagedescription-description): String
[LoggingLevel](#cfn-apigateway-deployment-stagedescription-logginglevel): String
[MethodSettings](#cfn-apigateway-deployment-stagedescription-methodsettings):
  - [*MethodSetting*](aws-properties-apigateway-deployment-stagedescription-methodsetting.md)
[MetricsEnabled](#cfn-apigateway-deployment-stagedescription-metricsenabled): Boolean
[ThrottlingBurstLimit](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit): Integer
[ThrottlingRateLimit](#cfn-apigateway-deployment-stagedescription-throttlingratelimit): Number
[Variables](#cfn-apigateway-deployment-stagedescription-variables):
  String: String
```

## Properties<a name="w3ab2c21c14c15b7"></a>

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
Indicates whether responses are cached and returned for requests\. You must enable a cache cluster on the stage to cache responses\. For more information, see [Enable API Gateway Caching in a Stage to Enhance API Performance](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Boolean

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
The logging level for this method\. For valid values, see the `loggingLevel` property of the [Stage](http://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#loggingLevel) resource in the *Amazon API Gateway API Reference*\.  
*Required*: No  
*Type*: String

`MethodSettings`  <a name="cfn-apigateway-deployment-stagedescription-methodsettings"></a>
Configures settings for all of the stage's methods\.  
*Required*: No  
*Type*: List of [API Gateway Deployment MethodSetting](aws-properties-apigateway-deployment-stagedescription-methodsetting.md)

`MetricsEnabled`  <a name="cfn-apigateway-deployment-stagedescription-metricsenabled"></a>
Indicates whether Amazon CloudWatch metrics are enabled for methods in the stage\.  
*Required*: No  
*Type*: Boolean

`ThrottlingBurstLimit`  <a name="cfn-apigateway-deployment-stagedescription-throttlingburstlimit"></a>
The number of burst requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Integer

`ThrottlingRateLimit`  <a name="cfn-apigateway-deployment-stagedescription-throttlingratelimit"></a>
The number of steady\-state requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Number

`Variables`  <a name="cfn-apigateway-deployment-stagedescription-variables"></a>
A map that defines the stage variables\. Variable names must consist of alphanumeric characters, and the values must match the following regular expression: `[A-Za-z0-9-._~:/?#&amp;=,]+`\.  
*Required*: No  
*Type*: Mapping of key\-value pairs