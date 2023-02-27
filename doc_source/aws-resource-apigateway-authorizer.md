# AWS::ApiGateway::Authorizer<a name="aws-resource-apigateway-authorizer"></a>

The `AWS::ApiGateway::Authorizer` resource creates an authorization layer that API Gateway activates for methods that have authorization enabled\. API Gateway activates the authorizer when a client calls those methods\.

## Syntax<a name="aws-resource-apigateway-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Authorizer",
  "Properties" : {
      "[AuthorizerCredentials](#cfn-apigateway-authorizer-authorizercredentials)" : String,
      "[AuthorizerResultTtlInSeconds](#cfn-apigateway-authorizer-authorizerresultttlinseconds)" : Integer,
      "[AuthorizerUri](#cfn-apigateway-authorizer-authorizeruri)" : String,
      "[AuthType](#cfn-apigateway-authorizer-authtype)" : String,
      "[IdentitySource](#cfn-apigateway-authorizer-identitysource)" : String,
      "[IdentityValidationExpression](#cfn-apigateway-authorizer-identityvalidationexpression)" : String,
      "[Name](#cfn-apigateway-authorizer-name)" : String,
      "[ProviderARNs](#cfn-apigateway-authorizer-providerarns)" : [ String, ... ],
      "[RestApiId](#cfn-apigateway-authorizer-restapiid)" : String,
      "[Type](#cfn-apigateway-authorizer-type)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-authorizer-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Authorizer
Properties: 
  [AuthorizerCredentials](#cfn-apigateway-authorizer-authorizercredentials): String
  [AuthorizerResultTtlInSeconds](#cfn-apigateway-authorizer-authorizerresultttlinseconds): Integer
  [AuthorizerUri](#cfn-apigateway-authorizer-authorizeruri): String
  [AuthType](#cfn-apigateway-authorizer-authtype): String
  [IdentitySource](#cfn-apigateway-authorizer-identitysource): String
  [IdentityValidationExpression](#cfn-apigateway-authorizer-identityvalidationexpression): String
  [Name](#cfn-apigateway-authorizer-name): String
  [ProviderARNs](#cfn-apigateway-authorizer-providerarns): 
    - String
  [RestApiId](#cfn-apigateway-authorizer-restapiid): String
  [Type](#cfn-apigateway-authorizer-type): String
```

## Properties<a name="aws-resource-apigateway-authorizer-properties"></a>

`AuthorizerCredentials`  <a name="cfn-apigateway-authorizer-authorizercredentials"></a>
Specifies the required credentials as an IAM role for API Gateway to invoke the authorizer\. To specify an IAM role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the Lambda function, specify null\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerResultTtlInSeconds`  <a name="cfn-apigateway-authorizer-authorizerresultttlinseconds"></a>
The TTL in seconds of cached authorizer results\. If it equals 0, authorization caching is disabled\. If it is greater than 0, API Gateway will cache authorizer responses\. If this field is not set, the default value is 300\. The maximum value is 3600, or 1 hour\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerUri`  <a name="cfn-apigateway-authorizer-authorizeruri"></a>
Specifies the authorizer's Uniform Resource Identifier \(URI\)\. For `TOKEN` or `REQUEST` authorizers, this must be a well\-formed Lambda function URI, for example, `arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:us-west-2:{account_id}:function:{lambda_function_name}/invocations`\. In general, the URI has this form `arn:aws:apigateway:{region}:lambda:path/{service_api}`, where `{region}` is the same as the region hosting the Lambda function, `path` indicates that the remaining substring in the URI should be treated as the path to the resource, including the initial `/`\. For Lambda functions, this is usually of the form `/2015-03-31/functions/[FunctionARN]/invocations`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthType`  <a name="cfn-apigateway-authorizer-authtype"></a>
Optional customer\-defined field, used in OpenAPI imports and exports without functional impact\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentitySource`  <a name="cfn-apigateway-authorizer-identitysource"></a>
The identity source for which authorization is requested\. For a `TOKEN` or `COGNITO_USER_POOLS` authorizer, this is required and specifies the request header mapping expression for the custom header holding the authorization token submitted by the client\. For example, if the token header name is `Auth`, the header mapping expression is `method.request.header.Auth`\. For the `REQUEST` authorizer, this is required when authorization caching is enabled\. The value is a comma\-separated string of one or more mapping expressions of the specified request parameters\. For example, if an `Auth` header, a `Name` query string parameter are defined as identity sources, this value is `method.request.header.Auth, method.request.querystring.Name`\. These parameters will be used to derive the authorization caching key and to perform runtime validation of the `REQUEST` authorizer by verifying all of the identity\-related request parameters are present, not null and non\-empty\. Only when this is true does the authorizer invoke the authorizer Lambda function, otherwise, it returns a 401 Unauthorized response without calling the Lambda function\. The valid value is a string of comma\-separated mapping expressions of the specified request parameters\. When the authorization caching is not enabled, this property is optional\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityValidationExpression`  <a name="cfn-apigateway-authorizer-identityvalidationexpression"></a>
A validation expression for the incoming identity token\. For `TOKEN` authorizers, this value is a regular expression\. For `COGNITO_USER_POOLS` authorizers, API Gateway will match the `aud` field of the incoming token from the client against the specified regular expression\. It will invoke the authorizer's Lambda function when there is a match\. Otherwise, it will return a 401 Unauthorized response without calling the Lambda function\. The validation expression does not apply to the `REQUEST` authorizer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigateway-authorizer-name"></a>
The name of the authorizer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProviderARNs`  <a name="cfn-apigateway-authorizer-providerarns"></a>
A list of the Amazon Cognito user pool ARNs for the `COGNITO_USER_POOLS` authorizer\. Each element is of this format: `arn:aws:cognito-idp:{region}:{account_id}:userpool/{user_pool_id}`\. For a `TOKEN` or `REQUEST` authorizer, this is not defined\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-authorizer-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-apigateway-authorizer-type"></a>
The authorizer type\. Valid values are `TOKEN` for a Lambda function using a single authorization token submitted in a custom header, `REQUEST` for a Lambda function using incoming request parameters, and `COGNITO_USER_POOLS` for using an Amazon Cognito user pool\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-authorizer-return-values"></a>

### Ref<a name="aws-resource-apigateway-authorizer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the authorizer's ID, such as `abcde1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigateway-authorizer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigateway-authorizer-return-values-fn--getatt-fn--getatt"></a>

`AuthorizerId`  <a name="AuthorizerId-fn::getatt"></a>
The ID for the authorizer\. For example: `abc123`\.

## Examples<a name="aws-resource-apigateway-authorizer--examples"></a>



### Create authorizer<a name="aws-resource-apigateway-authorizer--examples--Create_authorizer"></a>

The following examples create a custom authorizer that is an AWS Lambda function\.

#### JSON<a name="aws-resource-apigateway-authorizer--examples--Create_authorizer--json"></a>

```
{
    "Authorizer": {
        "Type": "AWS::ApiGateway::Authorizer",
        "Properties": {
            "AuthorizerCredentials": {
                "Fn::GetAtt": [
                    "LambdaInvocationRole",
                    "Arn"
                ]
            },
            "AuthorizerResultTtlInSeconds": "300",
            "AuthorizerUri": {
                "Fn::Join": [
                    "",
                    [
                        "arn:aws:apigateway:",
                        {
                            "Ref": "AWS::Region"
                        },
                        ":lambda:path/2015-03-31/functions/",
                        {
                            "Fn::GetAtt": [
                                "LambdaAuthorizer",
                                "Arn"
                            ]
                        },
                        "/invocations"
                    ]
                ]
            },
            "Type": "TOKEN",
            "IdentitySource": "method.request.header.Auth",
            "Name": "DefaultAuthorizer",
            "RestApiId": {
                "Ref": "RestApi"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-authorizer--examples--Create_authorizer--yaml"></a>

```
Authorizer:
  Type: 'AWS::ApiGateway::Authorizer'
  Properties:
    AuthorizerCredentials: !GetAtt 
      - LambdaInvocationRole
      - Arn
    AuthorizerResultTtlInSeconds: '300'
    AuthorizerUri: !Join 
      - ''
      - - 'arn:aws:apigateway:'
        - !Ref 'AWS::Region'
        - ':lambda:path/2015-03-31/functions/'
        - !GetAtt 
          - LambdaAuthorizer
          - Arn
        - /invocations
    Type: TOKEN
    IdentitySource: method.request.header.Auth
    Name: DefaultAuthorizer
    RestApiId: !Ref RestApi
```

## See also<a name="aws-resource-apigateway-authorizer--seealso"></a>
+ [authorizer:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateAuthorizer.html) in the *Amazon API Gateway REST API Reference*

