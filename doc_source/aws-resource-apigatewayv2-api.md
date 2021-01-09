# AWS::ApiGatewayV2::Api<a name="aws-resource-apigatewayv2-api"></a>

The `AWS::ApiGatewayV2::Api` resource creates an API\. WebSocket APIs and HTTP APIs are supported\. For more information about WebSocket APIs, see [About WebSocket APIs in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-overview.html) in the *API Gateway Developer Guide*\. For more information about HTTP APIs, see [HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api.html) in the *API Gateway Developer Guide\.*

## Syntax<a name="aws-resource-apigatewayv2-api-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-api-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Api",
  "Properties" : {
      "[ApiKeySelectionExpression](#cfn-apigatewayv2-api-apikeyselectionexpression)" : String,
      "[BasePath](#cfn-apigatewayv2-api-basepath)" : String,
      "[Body](#cfn-apigatewayv2-api-body)" : Json,
      "[BodyS3Location](#cfn-apigatewayv2-api-bodys3location)" : BodyS3Location,
      "[CorsConfiguration](#cfn-apigatewayv2-api-corsconfiguration)" : Cors,
      "[CredentialsArn](#cfn-apigatewayv2-api-credentialsarn)" : String,
      "[Description](#cfn-apigatewayv2-api-description)" : String,
      "[DisableExecuteApiEndpoint](#cfn-apigatewayv2-api-disableexecuteapiendpoint)" : Boolean,
      "[DisableSchemaValidation](#cfn-apigatewayv2-api-disableschemavalidation)" : Boolean,
      "[FailOnWarnings](#cfn-apigatewayv2-api-failonwarnings)" : Boolean,
      "[Name](#cfn-apigatewayv2-api-name)" : String,
      "[ProtocolType](#cfn-apigatewayv2-api-protocoltype)" : String,
      "[RouteKey](#cfn-apigatewayv2-api-routekey)" : String,
      "[RouteSelectionExpression](#cfn-apigatewayv2-api-routeselectionexpression)" : String,
      "[Tags](#cfn-apigatewayv2-api-tags)" : Json,
      "[Target](#cfn-apigatewayv2-api-target)" : String,
      "[Version](#cfn-apigatewayv2-api-version)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-api-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Api
Properties: 
  [ApiKeySelectionExpression](#cfn-apigatewayv2-api-apikeyselectionexpression): String
  [BasePath](#cfn-apigatewayv2-api-basepath): String
  [Body](#cfn-apigatewayv2-api-body): Json
  [BodyS3Location](#cfn-apigatewayv2-api-bodys3location): 
    BodyS3Location
  [CorsConfiguration](#cfn-apigatewayv2-api-corsconfiguration): 
    Cors
  [CredentialsArn](#cfn-apigatewayv2-api-credentialsarn): String
  [Description](#cfn-apigatewayv2-api-description): String
  [DisableExecuteApiEndpoint](#cfn-apigatewayv2-api-disableexecuteapiendpoint): Boolean
  [DisableSchemaValidation](#cfn-apigatewayv2-api-disableschemavalidation): Boolean
  [FailOnWarnings](#cfn-apigatewayv2-api-failonwarnings): Boolean
  [Name](#cfn-apigatewayv2-api-name): String
  [ProtocolType](#cfn-apigatewayv2-api-protocoltype): String
  [RouteKey](#cfn-apigatewayv2-api-routekey): String
  [RouteSelectionExpression](#cfn-apigatewayv2-api-routeselectionexpression): String
  [Tags](#cfn-apigatewayv2-api-tags): Json
  [Target](#cfn-apigatewayv2-api-target): String
  [Version](#cfn-apigatewayv2-api-version): String
```

## Properties<a name="aws-resource-apigatewayv2-api-properties"></a>

`ApiKeySelectionExpression`  <a name="cfn-apigatewayv2-api-apikeyselectionexpression"></a>
An API key selection expression\. Supported only for WebSocket APIs\. See [API Key Selection Expressions](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-selection-expressions.html#apigateway-websocket-api-apikey-selection-expressions)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasePath`  <a name="cfn-apigatewayv2-api-basepath"></a>
Specifies how to interpret the base path of the API during import\. Valid values are `ignore`, `prepend`, and `split`\. The default value is `ignore`\. To learn more, see [Set the OpenAPI basePath Property](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-import-api-basePath.html)\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Body`  <a name="cfn-apigatewayv2-api-body"></a>
The OpenAPI definition\. Supported only for HTTP APIs\. To import an HTTP API, you must specify a `Body` or `BodyS3Location`\.  
*Required*: Conditional  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BodyS3Location`  <a name="cfn-apigatewayv2-api-bodys3location"></a>
The S3 location of an OpenAPI definition\. Supported only for HTTP APIs\. To import an HTTP API, you must specify a `Body` or `BodyS3Location`\.  
*Required*: Conditional  
*Type*: [BodyS3Location](aws-properties-apigatewayv2-api-bodys3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CorsConfiguration`  <a name="cfn-apigatewayv2-api-corsconfiguration"></a>
A CORS configuration\. Supported only for HTTP APIs\. See [Configuring CORS](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-cors.html) for more information\.  
*Required*: No  
*Type*: [Cors](aws-properties-apigatewayv2-api-cors.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CredentialsArn`  <a name="cfn-apigatewayv2-api-credentialsarn"></a>
This property is part of quick create\. It specifies the credentials required for the integration, if any\. For a Lambda integration, three options are available\. To specify an IAM Role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To require that the caller's identity be passed through from the request, specify `arn:aws:iam::*:user/*`\. To use resource\-based permissions on supported AWS services, specify `null`\. Currently, this property is not used for HTTP integrations\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-api-description"></a>
The description of the API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableExecuteApiEndpoint`  <a name="cfn-apigatewayv2-api-disableexecuteapiendpoint"></a>
Specifies whether clients can invoke your API by using the default `execute-api` endpoint\. By default, clients can invoke your API with the default https://\{api\_id\}\.execute\-api\.\{region\}\.amazonaws\.com endpoint\. To require that clients use a custom domain name to invoke your API, disable the default endpoint\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableSchemaValidation`  <a name="cfn-apigatewayv2-api-disableschemavalidation"></a>
Avoid validating models when creating a deployment\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailOnWarnings`  <a name="cfn-apigatewayv2-api-failonwarnings"></a>
Specifies whether to rollback the API creation when a warning is encountered\. By default, API creation continues if a warning is encountered\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigatewayv2-api-name"></a>
The name of the API\. Required unless you specify an OpenAPI definition for `Body` or `S3BodyLocation`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtocolType`  <a name="cfn-apigatewayv2-api-protocoltype"></a>
The API protocol\. Valid values are `WEBSOCKET` or `HTTP`\. Required unless you specify an OpenAPI definition for `Body` or `S3BodyLocation`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteKey`  <a name="cfn-apigatewayv2-api-routekey"></a>
This property is part of quick create\. If you don't specify a `routeKey`, a default route of `$default` is created\. The `$default` route acts as a catch\-all for any request made to your API, for a particular stage\. The `$default` route key can't be modified\. You can add routes after creating the API, and you can update the route keys of additional routes\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteSelectionExpression`  <a name="cfn-apigatewayv2-api-routeselectionexpression"></a>
The route selection expression for the API\. For HTTP APIs, the `routeSelectionExpression` must be `${request.method} ${request.path}`\. If not provided, this will be the default for HTTP APIs\. This property is required for WebSocket APIs\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigatewayv2-api-tags"></a>
The collection of tags\. Each tag element is associated with a given resource\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-apigatewayv2-api-target"></a>
This property is part of quick create\. Quick create produces an API with an integration, a default catch\-all route, and a default stage which is configured to automatically deploy changes\. For HTTP integrations, specify a fully qualified URL\. For Lambda integrations, specify a function ARN\. The type of the integration will be HTTP\_PROXY or AWS\_PROXY, respectively\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-apigatewayv2-api-version"></a>
A version identifier for the API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-api-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-api-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the API ID, such as `a1bcdef2gh`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigatewayv2-api-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigatewayv2-api-return-values-fn--getatt-fn--getatt"></a>

`ApiEndpoint`  <a name="ApiEndpoint-fn::getatt"></a>
The default endpoint for an API\. For example: `https://abcdef.execute-api.us-west-2.amazonaws.com`\.

## Examples<a name="aws-resource-apigatewayv2-api--examples"></a>



### API creation example<a name="aws-resource-apigatewayv2-api--examples--API_creation_example"></a>

The following example creates a WebSocket `Api` resource called `MyApi`\.

#### JSON<a name="aws-resource-apigatewayv2-api--examples--API_creation_example--json"></a>

```
{
    "MyApi": {
      "Type": "AWS::ApiGatewayV2::Api",
      "Properties": {
        "Name": "MyApi",
        "ProtocolType": "WEBSOCKET",
        "RouteSelectionExpression": "$request.body.action",
        "ApiKeySelectionExpression": "$request.header.x-api-key"
      }
   }
}
```

#### YAML<a name="aws-resource-apigatewayv2-api--examples--API_creation_example--yaml"></a>

```
MyApi:
  Type: 'AWS::ApiGatewayV2::Api'
  Properties:
    Name: MyApi
    ProtocolType: WEBSOCKET
    RouteSelectionExpression: $request.body.action
    ApiKeySelectionExpression: $request.header.x-api-key
```

### Quick create HTTP API<a name="aws-resource-apigatewayv2-api--examples--Quick_create_HTTP_API"></a>

The following example uses quick create to launch an HTTP API `Api` resource called `HttpApi` that's integrated with a Lambda function\. Quick create produces an HTTP API with an integration, a default catch\-all route, and a default stage which is configured to automatically deploy changes\.

**Note**  
To invoke a Lambda integration, API Gateway must have the required permissions\. You can use a resource\-based policy or an IAM role to grant API Gateway permissions to invoke a Lambda function\. To learn more, see [AWS Lambda Permissions](https://docs.aws.amazon.com/lambda/latest/dg/lambda-permissions.html) in the * AWS Lambda Developer Guide*\.

#### JSON<a name="aws-resource-apigatewayv2-api--examples--Quick_create_HTTP_API--json"></a>

```
"HttpApi": {
    "Type": "AWS::ApiGatewayV2::Api",
    "Properties": {
        "Name": "Lambda Proxy",
        "Description": "Lambda proxy using quick create",
        "ProtocolType": "HTTP",
        "Target": "arn:aws:apigateway:{region}:lambda:path/2015-03-31/functions/arn:aws:lambda:{region}:{account-id}:function:{function-name}/invocations"
     }
}
```

#### YAML<a name="aws-resource-apigatewayv2-api--examples--Quick_create_HTTP_API--yaml"></a>

```
HttpApi:
  Type: AWS::ApiGatewayV2::Api
  Properties:
    Name: Lambda Proxy
    Description: Lambda proxy using quick create
    ProtocolType: HTTP
    Target: arn:aws:apigateway:{region}:lambda:path/2015-03-31/functions/arn:aws:lambda:{region}:{account-id}:function:{function-name}/invocations
```

## See also<a name="aws-resource-apigatewayv2-api--seealso"></a>
+ [CreateApi](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis.html#CreateApi) in the *Amazon API Gateway Version 2 API Reference*

