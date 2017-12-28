# Amazon API Gateway Deployment StageDescription<a name="aws-properties-apigateway-deployment-stagedescription"></a>

`StageDescription` is a property of the [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md) resource that configures an Amazon API Gateway \(API Gateway\) deployment stage\.

## Syntax<a name="w3ab2c21c14c14b5"></a>

### JSON<a name="aws-properties-apigateway-deployment-stagedescription-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cacheclustersize)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachedataencrypted)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachettlinseconds)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachingenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-clientcertificateid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-datatraceenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-documentationversion)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-logginglevel)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-methodsettings)" : [ MethodSetting, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-metricsenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-throttlingratelimit)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-variables)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-apigateway-deployment-stagedescription-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cacheclusterenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cacheclustersize): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachedataencrypted): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachettlinseconds): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-cachingenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-clientcertificateid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-datatraceenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-logginglevel): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-methodsettings):
  - MethodSetting
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-metricsenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-throttlingburstlimit): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-throttlingratelimit): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-deployment-stagedescription-variables):
  String: String
```

## Properties<a name="w3ab2c21c14c14b7"></a>

`CacheClusterEnabled`  
Indicates whether cache clustering is enabled for the stage\.  
*Required: *No  
*Type*: Boolean

`CacheClusterSize`  
The size of the stage's cache cluster\.  
*Required: *No  
*Type*: String

`CacheDataEncrypted`  
Indicates whether the cached responses are encrypted\.  
*Required: *No  
*Type*: Boolean

`CacheTtlInSeconds`  
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches responses\.  
*Required: *No  
*Type*: Integer

`CachingEnabled`  
Indicates whether responses are cached and returned for requests\. You must enable a cache cluster on the stage to cache responses\. For more information, see [Enable API Gateway Caching in a Stage to Enhance API Performance](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Boolean

`ClientCertificateId`  
The identifier of the client certificate that API Gateway uses to call your integration endpoints in the stage\.  
*Required: *No  
*Type*: String

`DataTraceEnabled`  
Indicates whether data trace logging is enabled for methods in the stage\. API Gateway pushes these logs to Amazon CloudWatch Logs\.  
*Required: *No  
*Type*: Boolean

`Description`  
A description of the purpose of the stage\.  
*Required: *No  
*Type*: String

`DocumentationVersion`  
The version identifier of the API documentation snapshot\.  
*Required: *No  
*Type*: String

`LoggingLevel`  
The logging level for this method\. For valid values, see the `loggingLevel` property of the [Stage](http://docs.aws.amazon.com/apigateway/api-reference/resource/stage/#loggingLevel) resource in the *Amazon API Gateway API Reference*\.  
*Required: *No  
*Type*: String

`MethodSettings`  
Configures settings for all of the stage's methods\.  
*Required: *No  
*Type*: List of [API Gateway Deployment MethodSetting](aws-properties-apigateway-deployment-stagedescription-methodsetting.md)

`MetricsEnabled`  
Indicates whether Amazon CloudWatch metrics are enabled for methods in the stage\.  
*Required: *No  
*Type*: Boolean

`ThrottlingBurstLimit`  
The number of burst requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Integer

`ThrottlingRateLimit`  
The number of steady\-state requests per second that API Gateway permits across all APIs, stages, and methods in your AWS account\. For more information, see [Manage API Request Throttling](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Number

`Variables`  
A map that defines the stage variables\. Variable names must consist of alphanumeric characters, and the values must match the following regular expression: `[A-Za-z0-9-._~:/?#&amp;=,]+`\.  
*Required: *No  
*Type*: Mapping of key\-value pairs