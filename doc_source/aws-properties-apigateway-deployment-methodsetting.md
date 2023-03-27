# AWS::ApiGateway::Deployment MethodSetting<a name="aws-properties-apigateway-deployment-methodsetting"></a>

The `MethodSetting` property type configures settings for all methods in a stage\.

The `MethodSettings` property of the [Amazon API Gateway Deployment StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type contains a list of `MethodSetting` property types\. 

## Syntax<a name="aws-properties-apigateway-deployment-methodsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-deployment-methodsetting-syntax.json"></a>

```
{
  "[CacheDataEncrypted](#cfn-apigateway-deployment-methodsetting-cachedataencrypted)" : Boolean,
  "[CacheTtlInSeconds](#cfn-apigateway-deployment-methodsetting-cachettlinseconds)" : Integer,
  "[CachingEnabled](#cfn-apigateway-deployment-methodsetting-cachingenabled)" : Boolean,
  "[DataTraceEnabled](#cfn-apigateway-deployment-methodsetting-datatraceenabled)" : Boolean,
  "[HttpMethod](#cfn-apigateway-deployment-methodsetting-httpmethod)" : String,
  "[LoggingLevel](#cfn-apigateway-deployment-methodsetting-logginglevel)" : String,
  "[MetricsEnabled](#cfn-apigateway-deployment-methodsetting-metricsenabled)" : Boolean,
  "[ResourcePath](#cfn-apigateway-deployment-methodsetting-resourcepath)" : String,
  "[ThrottlingBurstLimit](#cfn-apigateway-deployment-methodsetting-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigateway-deployment-methodsetting-throttlingratelimit)" : Double
}
```

### YAML<a name="aws-properties-apigateway-deployment-methodsetting-syntax.yaml"></a>

```
  [CacheDataEncrypted](#cfn-apigateway-deployment-methodsetting-cachedataencrypted): Boolean
  [CacheTtlInSeconds](#cfn-apigateway-deployment-methodsetting-cachettlinseconds): Integer
  [CachingEnabled](#cfn-apigateway-deployment-methodsetting-cachingenabled): Boolean
  [DataTraceEnabled](#cfn-apigateway-deployment-methodsetting-datatraceenabled): Boolean
  [HttpMethod](#cfn-apigateway-deployment-methodsetting-httpmethod): String
  [LoggingLevel](#cfn-apigateway-deployment-methodsetting-logginglevel): String
  [MetricsEnabled](#cfn-apigateway-deployment-methodsetting-metricsenabled): Boolean
  [ResourcePath](#cfn-apigateway-deployment-methodsetting-resourcepath): String
  [ThrottlingBurstLimit](#cfn-apigateway-deployment-methodsetting-throttlingburstlimit): Integer
  [ThrottlingRateLimit](#cfn-apigateway-deployment-methodsetting-throttlingratelimit): Double
```

## Properties<a name="aws-properties-apigateway-deployment-methodsetting-properties"></a>

`CacheDataEncrypted`  <a name="cfn-apigateway-deployment-methodsetting-cachedataencrypted"></a>
Specifies whether the cached responses are encrypted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheTtlInSeconds`  <a name="cfn-apigateway-deployment-methodsetting-cachettlinseconds"></a>
Specifies the time to live \(TTL\), in seconds, for cached responses\. The higher the TTL, the longer the response will be cached\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CachingEnabled`  <a name="cfn-apigateway-deployment-methodsetting-cachingenabled"></a>
Specifies whether responses should be cached and returned for requests\. A cache cluster must be enabled on the stage for responses to be cached\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataTraceEnabled`  <a name="cfn-apigateway-deployment-methodsetting-datatraceenabled"></a>
Specifies whether data trace logging is enabled for this method, which affects the log entries pushed to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-apigateway-deployment-methodsetting-httpmethod"></a>
The HTTP method\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-apigateway-deployment-methodsetting-logginglevel"></a>
Specifies the logging level for this method, which affects the log entries pushed to Amazon CloudWatch Logs\. Valid values are `OFF`, `ERROR`, and `INFO`\. Choose `ERROR` to write only error\-level entries to CloudWatch Logs, or choose `INFO` to include all `ERROR` events as well as extra informational events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricsEnabled`  <a name="cfn-apigateway-deployment-methodsetting-metricsenabled"></a>
Specifies whether Amazon CloudWatch metrics are enabled for this method\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcePath`  <a name="cfn-apigateway-deployment-methodsetting-resourcepath"></a>
The resource path for this method\. Forward slashes \(`/`\) are encoded as `~1` and the initial slash must include a forward slash\. For example, the path value `/resource/subresource` must be encoded as `/~1resource~1subresource`\. To specify the root path, use only a slash \(`/`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingBurstLimit`  <a name="cfn-apigateway-deployment-methodsetting-throttlingburstlimit"></a>
Specifies the throttling burst limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingRateLimit`  <a name="cfn-apigateway-deployment-methodsetting-throttlingratelimit"></a>
Specifies the throttling rate limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-deployment-methodsetting--seealso"></a>
+ [Stage](https://docs.aws.amazon.com/apigateway/latest/api/API_Stage.html) in the *Amazon API Gateway REST API Reference*

