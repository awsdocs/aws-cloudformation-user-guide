# Amazon API Gateway Method Integration<a name="aws-properties-apitgateway-method-integration"></a>

`Integration` is a property of the [AWS::ApiGateway::Method](aws-resource-apigateway-method.md) resource that specifies information about the target backend that an Amazon API Gateway \(API Gateway\) method calls\.

## Syntax<a name="w3ab2c21c14c25b7"></a>

### JSON<a name="aws-properties-apitgateway-method-integration-syntax.json"></a>

```
{
  "[CacheKeyParameters](#cfn-apigateway-method-integration-cachekeyparameters)" : [ String, ... ],
  "[CacheNamespace](#cfn-apigateway-method-integration-cachenamespace)" : String,
  "[ContentHandling](#cfn-apigateway-method-integration-contenthandling)" : String,
  "[Credentials](#cfn-apigateway-method-integration-credentials)" : String,
  "[IntegrationHttpMethod](#cfn-apigateway-method-integration-integrationhttpmethod)" : String,
  "[IntegrationResponses](#cfn-apigateway-method-integration-integrationresponses)" : [ [IntegrationResponse](aws-properties-apitgateway-method-integration-integrationresponse.md), ... ],
  "[PassthroughBehavior](#cfn-apigateway-method-integration-passthroughbehavior)" : String,
  "[RequestParameters](#cfn-apigateway-method-integration-requestparameters)" : { String:String, ... },
  "[RequestTemplates](#cfn-apigateway-method-integration-requesttemplates)" : { String:String, ... },
  "[Type](#cfn-apigateway-method-integration-type)" : String,
  "[Uri](#cfn-apigateway-method-integration-uri)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-integration-syntax.yaml"></a>

```
[CacheKeyParameters](#cfn-apigateway-method-integration-cachekeyparameters):
  - String
[CacheNamespace](#cfn-apigateway-method-integration-cachenamespace): String
[ContentHandling](#cfn-apigateway-method-integration-contenthandling): String

[Credentials](#cfn-apigateway-method-integration-credentials): String
[IntegrationHttpMethod](#cfn-apigateway-method-integration-integrationhttpmethod): String
[IntegrationResponses](#cfn-apigateway-method-integration-integrationresponses):
  [IntegrationResponse](aws-properties-apitgateway-method-integration-integrationresponse.md)
[PassthroughBehavior](#cfn-apigateway-method-integration-passthroughbehavior): String
[RequestParameters](#cfn-apigateway-method-integration-requestparameters):
  String: String
[RequestTemplates](#cfn-apigateway-method-integration-requesttemplates):
  String: String
[Type](#cfn-apigateway-method-integration-type): String
[Uri](#cfn-apigateway-method-integration-uri): String
```

## Properties<a name="w3ab2c21c14c25b9"></a>

`CacheKeyParameters`  <a name="cfn-apigateway-method-integration-cachekeyparameters"></a>
A list of request parameters whose values API Gateway caches\.  
*Required*: No  
*Type*: List of String values

`CacheNamespace`  <a name="cfn-apigateway-method-integration-cachenamespace"></a>
An API\-specific tag group of related cached parameters\.  
*Required*: No  
*Type*: String

`ContentHandling`  <a name="cfn-apigateway-method-integration-contenthandling"></a>
Specifies how to handle request payload content type conversions\. Valid values are:  
+ `CONVERT_TO_BINARY`: Converts a request payload from a base64\-encoded string to a binary blob\.
+ `CONVERT_TO_TEXT`: Converts a request payload from a binary blob to a base64\-encoded string\.
If this property isn't defined, the request payload is passed through from the method request to the integration request without modification, provided that the `PassthroughBehaviors` property is configured to support payload pass\-through\.  
*Required: *No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Credentials`  <a name="cfn-apigateway-method-integration-credentials"></a>
The credentials that are required for the integration\. To specify an AWS Identity and Access Management \(IAM\) role that API Gateway assumes, specify the role's Amazon Resource Name \(ARN\)\. To require that the caller's identity be passed through from the request, specify `arn:aws:iam::*:user/*`\.  
To use resource\-based permissions on the AWS Lambda \(Lambda\) function, don't specify this property\. Use the [AWS::Lambda::Permission](aws-resource-lambda-permission.md) resource to permit API Gateway to call the function\. For more information, see [Allow Amazon API Gateway to Invoke a Lambda Function](http://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html#access-control-resource-based-example-apigateway-invoke-function) in the *AWS Lambda Developer Guide*\.  
*Required*: No  
*Type*: String

`IntegrationHttpMethod`  <a name="cfn-apigateway-method-integration-integrationhttpmethod"></a>
The integration's HTTP method type\.  
*Required*: Conditional\. For the `Type` property, if you specify `MOCK`, this property is optional\. For all other types, you must specify this property\.  
*Type*: String

`IntegrationResponses`  <a name="cfn-apigateway-method-integration-integrationresponses"></a>
The response that API Gateway provides after a method's backend completes processing a request\. API Gateway intercepts the response from the backend so that you can control how API Gateway surfaces backend responses\. For example, you can map the backend status codes to codes that you define\.  
*Required*: No  
*Type*: List of [Amazon API Gateway Method Integration IntegrationResponse](aws-properties-apitgateway-method-integration-integrationresponse.md) property types

`PassthroughBehavior`  <a name="cfn-apigateway-method-integration-passthroughbehavior"></a>
Indicates when API Gateway passes requests to the targeted backend\. This behavior depends on the request's `Content-Type` header and whether you defined a mapping template for it\.  
For more information and valid values, see the [http://docs.aws.amazon.com/apigateway/api-reference/link-relation/integration-put/#passthroughBehavior](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/integration-put/#passthroughBehavior) field in the *API Gateway API Reference*\.  
*Required*: No  
*Type*: String

`RequestParameters`  <a name="cfn-apigateway-method-integration-requestparameters"></a>
The request parameters that API Gateway sends with the backend request\. Specify request parameters as key\-value pairs \(string\-to\-string mappings\), with a destination as the key and a source as the value\.  
Specify the destination by using the following pattern `integration.request.location.name`, where `location` is `querystring`, `path`, or `header`, and `name` is a valid, unique parameter name\.  
The source must be an existing method request parameter or a static value\. You must enclose static values in single quotation marks and pre\-encode these values based on their destination in the request\.  
*Required*: No  
*Type*: Mapping of key\-value pairs

`RequestTemplates`  <a name="cfn-apigateway-method-integration-requesttemplates"></a>
A map of Apache Velocity templates that are applied on the request payload\. The template that API Gateway uses is based on the value of the Content\-Type header that's sent by the client\. The content type value is the key, and the template is the value \(specified as a string\), such as the following snippet:  

```
"application/json": "{\n    \"statusCode\": \"200\"\n}"
```
For more information about templates, see [API Gateway API Request and Response Payload\-Mapping Template Reference](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Mapping of key\-value pairs

`Type`  <a name="cfn-apigateway-method-integration-type"></a>
The type of backend that your method is running, such as `HTTP` or `MOCK`\. For all of the valid values, see the [http://docs.aws.amazon.com/apigateway/api-reference/resource/integration/#type](http://docs.aws.amazon.com/apigateway/api-reference/resource/integration/#type) property for the `Integration` resource in the *Amazon API Gateway REST API Reference*\.  
*Required*: Yes  
*Type*: String

`Uri`  <a name="cfn-apigateway-method-integration-uri"></a>
The Uniform Resource Identifier \(URI\) for the integration\.  
If you specify `HTTP` for the `Type` property, specify the API endpoint URL\.  
If you specify `MOCK` for the `Type` property, don't specify this property\.  
If you specify `AWS` for the `Type` property, specify an AWS service that follows this form: `arn:aws:apigateway:region:subdomain.service|service:path|action/service_api`\. For example, a Lambda function URI follows this form: `arn:aws:apigateway:region:lambda:path/path`\. The path is usually in the form `/2015-03-31/functions/LambdaFunctionARN/invocations`\. For more information, see the `uri` property of the [Integration](http://docs.aws.amazon.com/apigateway/api-reference/resource/integration/) resource in the *Amazon API Gateway REST API Reference*\.  
*Required*: Conditional\. If you specified `HTTP` or `AWS` for the `Type` property, you must specify this property\.  
*Type*: String