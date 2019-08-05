# AWS::ApiGatewayV2::Authorizer<a name="aws-resource-apigatewayv2-authorizer"></a>

The `AWS::ApiGatewayV2::Authorizer` resource updates a Lambda authorizer function\. For more information about Lambda authorizer functions for WebSocket APIs, see [Create a Lambda REQUEST Authorizer Function](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-lambda-auth.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Authorizer",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-authorizer-apiid)" : String,
      "[AuthorizerCredentialsArn](#cfn-apigatewayv2-authorizer-authorizercredentialsarn)" : String,
      "[AuthorizerResultTtlInSeconds](#cfn-apigatewayv2-authorizer-authorizerresultttlinseconds)" : Integer,
      "[AuthorizerType](#cfn-apigatewayv2-authorizer-authorizertype)" : String,
      "[AuthorizerUri](#cfn-apigatewayv2-authorizer-authorizeruri)" : String,
      "[IdentitySource](#cfn-apigatewayv2-authorizer-identitysource)" : [ String, ... ],
      "[IdentityValidationExpression](#cfn-apigatewayv2-authorizer-identityvalidationexpression)" : String,
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
  [AuthorizerResultTtlInSeconds](#cfn-apigatewayv2-authorizer-authorizerresultttlinseconds): Integer
  [AuthorizerType](#cfn-apigatewayv2-authorizer-authorizertype): String
  [AuthorizerUri](#cfn-apigatewayv2-authorizer-authorizeruri): String
  [IdentitySource](#cfn-apigatewayv2-authorizer-identitysource):
    - String
  [IdentityValidationExpression](#cfn-apigatewayv2-authorizer-identityvalidationexpression): String
  [Name](#cfn-apigatewayv2-authorizer-name): String
```

## Properties<a name="aws-resource-apigatewayv2-authorizer-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-authorizer-apiid"></a>
The API identifier\.
*Required*: Yes
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthorizerCredentialsArn`  <a name="cfn-apigatewayv2-authorizer-authorizercredentialsarn"></a>
Specifies the required credentials as an IAM role for API Gateway to invoke the authorizer\. To specify an IAM role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the Lambda function, specify null\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerResultTtlInSeconds`  <a name="cfn-apigatewayv2-authorizer-authorizerresultttlinseconds"></a>
The time to live \(TTL\), in seconds, of cached authorizer results\. If it is zero, authorization caching is disabled\. If it is greater than zero, API Gateway will cache authorizer responses\. If this field is not set, the default value is 300\. The maximum value is 3600, or 1 hour\.
*Required*: No
*Type*: Integer
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerType`  <a name="cfn-apigatewayv2-authorizer-authorizertype"></a>
The authorizer type\. Currently the only valid value is `REQUEST`, for a Lambda function using incoming request parameters\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerUri`  <a name="cfn-apigatewayv2-authorizer-authorizeruri"></a>
The authorizer's Uniform Resource Identifier \(URI\)\. For `REQUEST` authorizers, this must be a well\-formed Lambda function URI, for example, `arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:us-west-2:{account_id}:function:{lambda_function_name}/invocations`\. In general, the URI has this form: `arn:aws:apigateway:{region}:lambda:path/{service_api} `, where *\{region\}* is the same as the region hosting the Lambda function, path indicates that the remaining substring in the URI should be treated as the path to the resource, including the initial `/`\. For Lambda functions, this is usually of the form `/2015-03-31/functions/[FunctionARN]/invocations`\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentitySource`  <a name="cfn-apigatewayv2-authorizer-identitysource"></a>
The identity source for which authorization is requested\.
For the `REQUEST` authorizer, this is required when authorization caching is enabled\. The value is a comma\-separated string of one or more mapping expressions of the specified request parameters\. For example, if an Auth header, a Name query string parameter are defined as identity sources, this value is `$method.request.header.Auth, $method.request.querystring.Name`\. These parameters will be used to derive the authorization caching key and to perform runtime validation of the `REQUEST` authorizer by verifying all of the identity\-related request parameters are present, not null and non\-empty\. Only when this is true does the authorizer invoke the authorizer Lambda function, otherwise, it returns a `401 Unauthorized` response without calling the Lambda function\. The valid value is a string of comma\-separated mapping expressions of the specified request parameters\. When the authorization caching is not enabled, this property is optional\.
*Required*: Yes
*Type*: List of String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityValidationExpression`  <a name="cfn-apigatewayv2-authorizer-identityvalidationexpression"></a>
The validation expression does not apply to the `REQUEST` authorizer\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigatewayv2-authorizer-name"></a>
The name of the authorizer\.
*Required*: Yes
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-apigatewayv2-authorizer-return-values"></a>

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

## See Also<a name="aws-resource-apigatewayv2-authorizer--seealso"></a>
+ [CreateAuthorizer](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-authorizers.html#CreateAuthorizer) in the *Amazon API Gateway Version 2 API Reference*
