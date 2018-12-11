# AWS::ApiGateway::Authorizer<a name="aws-resource-apigateway-authorizer"></a>

The `AWS::ApiGateway::Authorizer` resource creates an authorization layer that Amazon API Gateway \(API Gateway\) activates for methods that have authorization enabled\. API Gateway activates the authorizer when a client calls those methods\.

**Topics**
+ [Syntax](#aws-resource-apigateway-authorizer-syntax)
+ [Properties](#w4ab1c21c10c30b9)
+ [Return Value](#w4ab1c21c10c30c11)
+ [Examples](#w4ab1c21c10c30c13)

## Syntax<a name="aws-resource-apigateway-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Authorizer",
  "Properties" : {
    "[AuthType](#cfn-apigateway-authorizer-authtype)" : String,
    "[AuthorizerCredentials](#cfn-apigateway-authorizer-authorizercredentials)" : String,
    "[AuthorizerResultTtlInSeconds](#cfn-apigateway-authorizer-authorizerresultttlinseconds)" : Integer,
    "[AuthorizerUri](#cfn-apigateway-authorizer-authorizeruri)" : String,
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
  [AuthType](#cfn-apigateway-authorizer-authtype): String
  [AuthorizerCredentials](#cfn-apigateway-authorizer-authorizercredentials): String
  [AuthorizerResultTtlInSeconds](#cfn-apigateway-authorizer-authorizerresultttlinseconds): Integer
  [AuthorizerUri](#cfn-apigateway-authorizer-authorizeruri): String
  [IdentitySource](#cfn-apigateway-authorizer-identitysource): String
  [IdentityValidationExpression](#cfn-apigateway-authorizer-identityvalidationexpression): String
  [Name](#cfn-apigateway-authorizer-name): String
  [ProviderARNs](#cfn-apigateway-authorizer-providerarns):
    - String
  [RestApiId](#cfn-apigateway-authorizer-restapiid): String
  [Type](#cfn-apigateway-authorizer-type): String
```

## Properties<a name="w4ab1c21c10c30b9"></a>

For more information, including valid values, constraints, and examples of specifying each property, see [Authorizer](https://docs.aws.amazon.com/apigateway/api-reference/resource/authorizer) in the *API Gateway API Reference*\.

`AuthType`  <a name="cfn-apigateway-authorizer-authtype"></a>
An optional customer\-defined field that's used in Swagger imports and exports without functional impact\.  
*Required: *No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizerCredentials`  <a name="cfn-apigateway-authorizer-authorizercredentials"></a>
The credentials that are required for the authorizer\. To specify an AWS Identity and Access Management \(IAM\) role that API Gateway assumes, specify the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the AWS Lambda \(Lambda\) function, specify null\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizerResultTtlInSeconds`  <a name="cfn-apigateway-authorizer-authorizerresultttlinseconds"></a>
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches authorizer results\. If you specify a value greater than `0`, API Gateway caches the authorizer responses\. By default, API Gateway sets this property to `300`\. The maximum value is `3600`, or 1 hour\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizerUri`  <a name="cfn-apigateway-authorizer-authorizeruri"></a>
The authorizer's Uniform Resource Identifier \(URI\)\. If you specify `TOKEN` for the authorizer's `Type` property, specify a Lambda function URI that has the form `arn:aws:apigateway:region:lambda:path/path`\. The path usually has the form `/2015-03-31/functions/LambdaFunctionARN/invocations`\.  
*Required*: Conditional\. Specify this property for Lambda functions only\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IdentitySource`  <a name="cfn-apigateway-authorizer-identitysource"></a>
The source of the identity in an incoming request\.   
If you specify `TOKEN` or `COGNITO_USER_POOLS` for the `Type` property, specify a header mapping expression using the form `method.request.header.name`, where *name* is the name of a custom authorization header that clients submit as part of their requests\.   
If you specify `REQUEST` for the `Type` property, specify a comma\-separated string of one or more mapping expressions of the specified request parameter using the form `method.request.parameter.name`\. For supported parameter types, see [Configure Lambda Authorizer Using the API Gateway Console](https://docs.aws.amazon.com/apigateway/latest/developerguide/configure-api-gateway-lambda-authorization-with-console.html) in the *API Gateway Developer Guide*\. The expression may also have the form `context.identity.name` where *name* is one of the provided context variables. 
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IdentityValidationExpression`  <a name="cfn-apigateway-authorizer-identityvalidationexpression"></a>
A validation expression for the incoming identity\. If you specify `TOKEN` for the authorizer's `Type` property, specify a regular expression\. API Gateway uses the expression to attempt to match the incoming client token, and proceeds if the token matches\. If the token doesn't match, API Gateway responds with a 401 \(unauthorized request\) error code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-apigateway-authorizer-name"></a>
The name of the authorizer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ProviderARNs`  <a name="cfn-apigateway-authorizer-providerarns"></a>
A list of the Amazon Cognito user pool Amazon Resource Names \(ARNs\) to associate with this authorizer\. For more information, see [Use Amazon Cognito User Pools](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.html#apigateway-enable-cognito-user-pool) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-authorizer-restapiid"></a>
The ID of the `RestApi` resource that API Gateway creates the authorizer in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Type`  <a name="cfn-apigateway-authorizer-type"></a>
<<<<<<< HEAD
The type of authorizer\. Valid values include:   
+ `TOKEN`: A custom authorizer that uses a Lambda function\.
+ `COGNITO_USER_POOLS`: An authorizer that uses Amazon Cognito user pools\.
+ `REQUEST`: An authorizer that uses a Lambda function using incoming request parameters\.
*Required*: Yes  
=======
The type of authorizer:  

+ For a custom authorizer that uses a Lambda function, use `TOKEN` or `REQUEST` to specify the Lambda Event Payload\.

+ For an authorizer that uses Amazon Cognito user pools, use `COGNITO_USER_POOLS`\.
*Required: *Yes  
>>>>>>> Added some information on Type: REQUEST
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w4ab1c21c10c30c11"></a>

### Ref<a name="w4ab1c21c10c30c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the authorizer's ID, such as `abcde1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w4ab1c21c10c30c13"></a>

The following examples create a custom authorizer that is an AWS Lambda function\.

### JSON<a name="aws-resource-apigateway-authorizer-example.json"></a>

```
"Authorizer": {
  "Type": "AWS::ApiGateway::Authorizer",
  "Properties": {
    "AuthorizerCredentials": { "Fn::GetAtt": ["LambdaInvocationRole", "Arn"] },
    "AuthorizerResultTtlInSeconds": "300",
    "AuthorizerUri" : {"Fn::Join" : ["", [
      "arn:aws:apigateway:",
      {"Ref" : "AWS::Region"},
      ":lambda:path/2015-03-31/functions/",
      {"Fn::GetAtt" : ["LambdaAuthorizer", "Arn"]}, "/invocations"
    ]]},
    "Type": "TOKEN",
    "IdentitySource": "method.request.header.Auth",
    "Name": "DefaultAuthorizer",
    "RestApiId": {
      "Ref": "RestApi"
    }
  }
}
```

### YAML<a name="aws-resource-apigateway-authorizer-example.yaml"></a>

```
Authorizer: 
  Type: AWS::ApiGateway::Authorizer
  Properties: 
    AuthorizerCredentials: 
      Fn::GetAtt: 
        - "LambdaInvocationRole"
        - "Arn"
    AuthorizerResultTtlInSeconds: "300"
    AuthorizerUri: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:apigateway:"
          - Ref: "AWS::Region"
          - ":lambda:path/2015-03-31/functions/"
          - Fn::GetAtt: 
              - "LambdaAuthorizer"
              - "Arn"
          - "/invocations"
    Type: "TOKEN"
    IdentitySource: "method.request.header.Auth"
    Name: "DefaultAuthorizer"
    RestApiId: 
      Ref: "RestApi"
```
