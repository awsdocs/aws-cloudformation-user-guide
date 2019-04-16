# AWS::ApiGatewayV2::Authorizer<a name="aws-resource-apigatewayv2-authorizer"></a>

The `AWS::ApiGatewayV2::Authorizer` resource creates an authorization layer for an Amazon API Gateway \(API Gateway\) API\. 

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
    "[Name](#cfn-apigatewayv2-authorizer-name)" : String  }
}
```

### YAML<a name="aws-resource-apigatewayv2-authorizer-syntax.yaml"></a>

```
Type: "AWS::ApiGatewayV2::Authorizer"
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
The ID of the `Api` resource that API Gateway creates the authorizer in\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AuthorizerCredentialsArn`  <a name="cfn-apigatewayv2-authorizer-authorizercredentialsarn"></a>
The credentials that are required for the authorizer\. To specify an AWS Identity and Access Management \(IAM\) role that API Gateway assumes, specify the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the AWS Lambda \(Lambda\) function, specify null\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthorizerResultTtlInSeconds`  <a name="cfn-apigatewayv2-authorizer-authorizerresultttlinseconds"></a>
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches authorizer results\. If you specify a value greater than `0`, API Gateway caches the authorizer responses\. By default, API Gateway sets this property to `300`\. The maximum value is `3600`, or 1 hour\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthorizerType`  <a name="cfn-apigatewayv2-authorizer-authorizertype"></a>
The authorizer type\. Currently the only valid value is `REQUEST`, for a Lambda function using incoming request parameters\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AuthorizerUri`  <a name="cfn-apigatewayv2-authorizer-authorizeruri"></a>
The authorizer's Uniform Resource Identifier \(URI\)\. If you specify `TOKEN` for the authorizer's `Type` property, specify a Lambda function URI that has the form `arn:aws:apigateway:region:lambda:path/path`\. The path usually has the form `/2015-03-31/functions/LambdaFunctionARN/invocations`\.  
 *Required*: Yes  
Specify this property for Lambda functions only\.  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IdentitySource`  <a name="cfn-apigatewayv2-authorizer-identitysource"></a>
The source of the identity in an incoming request\.   
If you specify `REQUEST` for the `Type` property, specify a comma\-separated string of one or more mapping expressions of the specified request parameter using the form `method.request.parameter.name`\.   
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IdentityValidationExpression`  <a name="cfn-apigatewayv2-authorizer-identityvalidationexpression"></a>
A validation expression for the incoming identity\. If you specify `TOKEN` for the authorizer's `Type` property, specify a regular expression\. API Gateway uses the expression to attempt to match the incoming client token, and proceeds if the token matches\. If the token doesn't match, API Gateway responds with a 401 \(unauthorized request\) error code\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-apigatewayv2-authorizer-name"></a>
The name of the authorizer\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-authorizer-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-authorizer-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::Authorizer` resource to the intrinsic `Ref` function, the function returns the authorizer's ID, such as `abcde1`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-authorizer-examples"></a>

### Authorizer creation example<a name="aws-resource-apigatewayv2-authorizer-example1"></a>

The following example creates a Lambda `authorizer` resource for the `MyApi` API\. 

#### JSON<a name="aws-resource-apigatewayv2-authorizer-example1.json"></a>

```
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
```

#### YAML<a name="aws-resource-apigatewayv2-authorizer-example1.yaml"></a>

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

## See Also<a name="aws-resource-apigatewayv2-authorizer-seealso"></a>
+  [CreateAuthorizer](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-authorizers.html#CreateAuthorizer) in the *Amazon API Gateway V2 API Reference* 