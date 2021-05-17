# AWS::ApiGatewayV2::Authorizer<a name="aws-resource-apigatewayv2-authorizer"></a>

The `AWS::ApiGatewayV2::Authorizer` resource creates an authorizer for a WebSocket API or an HTTP API\. To learn more, see [Controlling and managing access to a WebSocket API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-control-access.html) and [Controlling and managing access to an HTTP API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-access-control.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Authorizer",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-authorizer-apiid)" : String,
      "[AuthorizerCredentialsArn](#cfn-apigatewayv2-authorizer-authorizercredentialsarn)" : String,
      "[AuthorizerPayloadFormatVersion](#cfn-apigatewayv2-authorizer-authorizerpayloadformatversion)" : String,
      "[AuthorizerResultTtlInSeconds](#cfn-apigatewayv2-authorizer-authorizerresultttlinseconds)" : Integer,
      "[AuthorizerType](#cfn-apigatewayv2-authorizer-authorizertype)" : String,
      "[AuthorizerUri](#cfn-apigatewayv2-authorizer-authorizeruri)" : String,
      "[EnableSimpleResponses](#cfn-apigatewayv2-authorizer-enablesimpleresponses)" : Boolean,
      "[IdentitySource](#cfn-apigatewayv2-authorizer-identitysource)" : [ String, ... ],
      "[IdentityValidationExpression](#cfn-apigatewayv2-authorizer-identityvalidationexpression)" : String,
      "[JwtConfiguration](#cfn-apigatewayv2-authorizer-jwtconfiguration)" : JWTConfiguration,
      "[Name](#cfn-apigatewayv2-authorizer-name)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-authorizer-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Authorizer
Properties: 
  [ApiId](#cfn-apigatewayv2-authorizer-apiid): String
  [AuthorizerCredentialsArn](#cfn-apigatewayv2-authorizer-authorizercredentialsarn): String
  [AuthorizerPayloadFormatVersion](#cfn-apigatewayv2-authorizer-authorizerpayloadformatversion): String
  [AuthorizerResultTtlInSeconds](#cfn-apigatewayv2-authorizer-authorizerresultttlinseconds): Integer
  [AuthorizerType](#cfn-apigatewayv2-authorizer-authorizertype): String
  [AuthorizerUri](#cfn-apigatewayv2-authorizer-authorizeruri): String
  [EnableSimpleResponses](#cfn-apigatewayv2-authorizer-enablesimpleresponses): Boolean
  [IdentitySource](#cfn-apigatewayv2-authorizer-identitysource): 
    - String
  [IdentityValidationExpression](#cfn-apigatewayv2-authorizer-identityvalidationexpression): String
  [JwtConfiguration](#cfn-apigatewayv2-authorizer-jwtconfiguration): 
    JWTConfiguration
  [Name](#cfn-apigatewayv2-authorizer-name): String
```

## Properties<a name="aws-resource-apigatewayv2-authorizer-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-authorizer-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthorizerCredentialsArn`  <a name="cfn-apigatewayv2-authorizer-authorizercredentialsarn"></a>
Specifies the required credentials as an IAM role for API Gateway to invoke the authorizer\. To specify an IAM role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the Lambda function, specify null\. Supported only for `REQUEST` authorizers\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerPayloadFormatVersion`  <a name="cfn-apigatewayv2-authorizer-authorizerpayloadformatversion"></a>
Specifies the format of the payload sent to an HTTP API Lambda authorizer\. Required for HTTP API Lambda authorizers\. Supported values are `1.0` and `2.0`\. To learn more, see [Working with AWS Lambda authorizers for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-lambda-authorizer.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerResultTtlInSeconds`  <a name="cfn-apigatewayv2-authorizer-authorizerresultttlinseconds"></a>
The time to live \(TTL\) for cached authorizer results, in seconds\. If it equals 0, authorization caching is disabled\. If it is greater than 0, API Gateway caches authorizer responses\. The maximum value is 3600, or 1 hour\. Supported only for HTTP API Lambda authorizers\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerType`  <a name="cfn-apigatewayv2-authorizer-authorizertype"></a>
The authorizer type\. Specify `REQUEST` for a Lambda function using incoming request parameters\. Specify `JWT` to use JSON Web Tokens \(supported only for HTTP APIs\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerUri`  <a name="cfn-apigatewayv2-authorizer-authorizeruri"></a>
The authorizer's Uniform Resource Identifier \(URI\)\. For `REQUEST` authorizers, this must be a well\-formed Lambda function URI, for example, `arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:us-west-2:{account_id}:function:{lambda_function_name}/invocations`\. In general, the URI has this form: `arn:aws:apigateway:{region}:lambda:path/{service_api} `, where *\{region\}* is the same as the region hosting the Lambda function, path indicates that the remaining substring in the URI should be treated as the path to the resource, including the initial `/`\. For Lambda functions, this is usually of the form `/2015-03-31/functions/[FunctionARN]/invocations`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableSimpleResponses`  <a name="cfn-apigatewayv2-authorizer-enablesimpleresponses"></a>
Specifies whether a Lambda authorizer returns a response in a simple format\. By default, a Lambda authorizer must return an IAM policy\. If enabled, the Lambda authorizer can return a boolean value instead of an IAM policy\. Supported only for HTTP APIs\. To learn more, see [Working with AWS Lambda authorizers for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-lambda-authorizer.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentitySource`  <a name="cfn-apigatewayv2-authorizer-identitysource"></a>
The identity source for which authorization is requested\.  
For a `REQUEST` authorizer, this is optional\. The value is a set of one or more mapping expressions of the specified request parameters\. The identity source can be headers, query string parameters, stage variables, and context parameters\. For example, if an Auth header and a Name query string parameter are defined as identity sources, this value is route\.request\.header\.Auth, route\.request\.querystring\.Name for WebSocket APIs\. For HTTP APIs, use selection expressions prefixed with `$`, for example, `$request.header.Auth`, `$request.querystring.Name`\. These parameters are used to perform runtime validation for Lambda\-based authorizers by verifying all of the identity\-related request parameters are present in the request, not null, and non\-empty\. Only when this is true does the authorizer invoke the authorizer Lambda function\. Otherwise, it returns a 401 Unauthorized response without calling the Lambda function\. For HTTP APIs, identity sources are also used as the cache key when caching is enabled\. To learn more, see [Working with AWS Lambda authorizers for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-lambda-authorizer.html)\.  
For `JWT`, a single entry that specifies where to extract the JSON Web Token \(JWT\) from inbound requests\. Currently only header\-based and query parameter\-based selections are supported, for example `$request.header.Authorization`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityValidationExpression`  <a name="cfn-apigatewayv2-authorizer-identityvalidationexpression"></a>
This parameter is not used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JwtConfiguration`  <a name="cfn-apigatewayv2-authorizer-jwtconfiguration"></a>
The `JWTConfiguration` property specifies the configuration of a JWT authorizer\. Required for the `JWT` authorizer type\. Supported only for HTTP APIs\.   
*Required*: No  
*Type*: [JWTConfiguration](aws-properties-apigatewayv2-authorizer-jwtconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigatewayv2-authorizer-name"></a>
The name of the authorizer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-authorizer-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-authorizer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the authorizer's ID, such as `abcde1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-authorizer--examples"></a>



### Authorizer creation example<a name="aws-resource-apigatewayv2-authorizer--examples--Authorizer_creation_example"></a>

The following example creates a Lambda `authorizer` resource for the `MyApi` API\.

#### JSON<a name="aws-resource-apigatewayv2-authorizer--examples--Authorizer_creation_example--json"></a>

```
{
    "Authorizer": {
        "Type": "AWS::ApiGatewayV2::Authorizer",
        "Properties": {
            "Name": "LambdaAuthorizer",
            "ApiId": {
                "Ref": "MyApi"
            },
            "AuthorizerType": "REQUEST",
            "AuthorizerCredentialsArn": "Arn",
            "AuthorizerUri": {
                "Fn::Join": [
                    "",
                    [
                        "arn:",
                        {
                            "Ref": "AWS::Partition"
                        },
                        ":apigateway:",
                        {
                            "Ref": "AWS::Region"
                        },
                        ":lambda:path/2015-03-31/functions/",
                        "/invocations"
                    ]
                ]
            },
            "AuthorizerResultTtlInSeconds": 500,
            "IdentitySource": [
                "route.request.header.Auth"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-authorizer--examples--Authorizer_creation_example--yaml"></a>

```
Authorizer:
  Type: 'AWS::ApiGatewayV2::Authorizer'
  Properties:
    Name: LambdaAuthorizer
    ApiId: !Ref MyApi
    AuthorizerType: REQUEST
    AuthorizerCredentialsArn: Arn
    AuthorizerUri: !Join 
      - ''
      - - 'arn:'
        - !Ref 'AWS::Partition'
        - ':apigateway:'
        - !Ref 'AWS::Region'
        - ':lambda:path/2015-03-31/functions/'
        - /invocations
    AuthorizerResultTtlInSeconds: 500
    IdentitySource:
      - route.request.header.Auth
```

## See also<a name="aws-resource-apigatewayv2-authorizer--seealso"></a>
+ [CreateAuthorizer](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-authorizers.html#CreateAuthorizer) in the *Amazon API Gateway Version 2 API Reference*

