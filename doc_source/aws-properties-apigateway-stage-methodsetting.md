# AWS::ApiGateway::Stage MethodSetting<a name="aws-properties-apigateway-stage-methodsetting"></a>

The `MethodSetting` property type configures settings for all methods in a stage\.

The `MethodSettings` property of the `AWS::ApiGateway::Stage` resource contains a list of `MethodSetting` property types\.

## Syntax<a name="aws-properties-apigateway-stage-methodsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-stage-methodsetting-syntax.json"></a>

```
{
  "[CacheDataEncrypted](#cfn-apigateway-stage-methodsetting-cachedataencrypted)" : Boolean,
  "[CacheTtlInSeconds](#cfn-apigateway-stage-methodsetting-cachettlinseconds)" : Integer,
  "[CachingEnabled](#cfn-apigateway-stage-methodsetting-cachingenabled)" : Boolean,
  "[DataTraceEnabled](#cfn-apigateway-stage-methodsetting-datatraceenabled)" : Boolean,
  "[HttpMethod](#cfn-apigateway-stage-methodsetting-httpmethod)" : String,
  "[LoggingLevel](#cfn-apigateway-stage-methodsetting-logginglevel)" : String,
  "[MetricsEnabled](#cfn-apigateway-stage-methodsetting-metricsenabled)" : Boolean,
  "[ResourcePath](#cfn-apigateway-stage-methodsetting-resourcepath)" : String,
  "[ThrottlingBurstLimit](#cfn-apigateway-stage-methodsetting-throttlingburstlimit)" : Integer,
  "[ThrottlingRateLimit](#cfn-apigateway-stage-methodsetting-throttlingratelimit)" : Double
}
```

### YAML<a name="aws-properties-apigateway-stage-methodsetting-syntax.yaml"></a>

```
  [CacheDataEncrypted](#cfn-apigateway-stage-methodsetting-cachedataencrypted): Boolean
  [CacheTtlInSeconds](#cfn-apigateway-stage-methodsetting-cachettlinseconds): Integer
  [CachingEnabled](#cfn-apigateway-stage-methodsetting-cachingenabled): Boolean
  [DataTraceEnabled](#cfn-apigateway-stage-methodsetting-datatraceenabled): Boolean
  [HttpMethod](#cfn-apigateway-stage-methodsetting-httpmethod): String
  [LoggingLevel](#cfn-apigateway-stage-methodsetting-logginglevel): String
  [MetricsEnabled](#cfn-apigateway-stage-methodsetting-metricsenabled): Boolean
  [ResourcePath](#cfn-apigateway-stage-methodsetting-resourcepath): String
  [ThrottlingBurstLimit](#cfn-apigateway-stage-methodsetting-throttlingburstlimit): Integer
  [ThrottlingRateLimit](#cfn-apigateway-stage-methodsetting-throttlingratelimit): Double
```

## Properties<a name="aws-properties-apigateway-stage-methodsetting-properties"></a>

`CacheDataEncrypted`  <a name="cfn-apigateway-stage-methodsetting-cachedataencrypted"></a>
Specifies whether the cached responses are encrypted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheTtlInSeconds`  <a name="cfn-apigateway-stage-methodsetting-cachettlinseconds"></a>
Specifies the time to live \(TTL\), in seconds, for cached responses\. The higher the TTL, the longer the response will be cached\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CachingEnabled`  <a name="cfn-apigateway-stage-methodsetting-cachingenabled"></a>
Specifies whether responses should be cached and returned for requests\. A cache cluster must be enabled on the stage for responses to be cached\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataTraceEnabled`  <a name="cfn-apigateway-stage-methodsetting-datatraceenabled"></a>
Specifies whether data trace logging is enabled for this method, which affects the log entries pushed to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-apigateway-stage-methodsetting-httpmethod"></a>
The HTTP method\. To apply settings to multiple resources and methods, specify an asterisk \(`*`\) for the `HttpMethod` and `/*` for the `ResourcePath`\. This parameter is required when you specify a `MethodSetting`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingLevel`  <a name="cfn-apigateway-stage-methodsetting-logginglevel"></a>
Specifies the logging level for this method, which affects the log entries pushed to Amazon CloudWatch Logs\. Valid values are `OFF`, `ERROR`, and `INFO`\. Choose `ERROR` to write only error\-level entries to CloudWatch Logs, or choose `INFO` to include all `ERROR` events as well as extra informational events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricsEnabled`  <a name="cfn-apigateway-stage-methodsetting-metricsenabled"></a>
Specifies whether Amazon CloudWatch metrics are enabled for this method\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcePath`  <a name="cfn-apigateway-stage-methodsetting-resourcepath"></a>
The resource path for this method\. Forward slashes \(`/`\) are encoded as `~1` and the initial slash must include a forward slash\. For example, the path value `/resource/subresource` must be encoded as `/~1resource~1subresource`\. To specify the root path, use only a slash \(`/`\)\. To apply settings to multiple resources and methods, specify an asterisk \(`*`\) for the `HttpMethod` and `/*` for the `ResourcePath`\. This parameter is required when you specify a `MethodSetting`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingBurstLimit`  <a name="cfn-apigateway-stage-methodsetting-throttlingburstlimit"></a>
Specifies the throttling burst limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThrottlingRateLimit`  <a name="cfn-apigateway-stage-methodsetting-throttlingratelimit"></a>
Specifies the throttling rate limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apigateway-stage-methodsetting--seealso"></a>
+ [Stage](https://docs.aws.amazon.com/apigateway/latest/api/API_Stage.html) in the *Amazon API Gateway REST API Reference*

