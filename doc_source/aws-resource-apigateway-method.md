# AWS::ApiGateway::Method<a name="aws-resource-apigateway-method"></a>

The `AWS::ApiGateway::Method` resource creates API Gateway methods that define the parameters and body that clients must send in their requests\.

## Syntax<a name="aws-resource-apigateway-method-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-method-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Method",
  "Properties" : {
      "[ApiKeyRequired](#cfn-apigateway-method-apikeyrequired)" : Boolean,
      "[AuthorizationScopes](#cfn-apigateway-method-authorizationscopes)" : [ String, ... ],
      "[AuthorizationType](#cfn-apigateway-method-authorizationtype)" : String,
      "[AuthorizerId](#cfn-apigateway-method-authorizerid)" : String,
      "[HttpMethod](#cfn-apigateway-method-httpmethod)" : String,
      "[Integration](#cfn-apigateway-method-integration)" : Integration,
      "[MethodResponses](#cfn-apigateway-method-methodresponses)" : [ MethodResponse, ... ],
      "[OperationName](#cfn-apigateway-method-operationname)" : String,
      "[RequestModels](#cfn-apigateway-method-requestmodels)" : {Key : Value, ...},
      "[RequestParameters](#cfn-apigateway-method-requestparameters)" : {Key : Value, ...},
      "[RequestValidatorId](#cfn-apigateway-method-requestvalidatorid)" : String,
      "[ResourceId](#cfn-apigateway-method-resourceid)" : String,
      "[RestApiId](#cfn-apigateway-method-restapiid)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-method-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Method
Properties: 
  [ApiKeyRequired](#cfn-apigateway-method-apikeyrequired): Boolean
  [AuthorizationScopes](#cfn-apigateway-method-authorizationscopes): 
    - String
  [AuthorizationType](#cfn-apigateway-method-authorizationtype): String
  [AuthorizerId](#cfn-apigateway-method-authorizerid): String
  [HttpMethod](#cfn-apigateway-method-httpmethod): String
  [Integration](#cfn-apigateway-method-integration): 
    Integration
  [MethodResponses](#cfn-apigateway-method-methodresponses): 
    - MethodResponse
  [OperationName](#cfn-apigateway-method-operationname): String
  [RequestModels](#cfn-apigateway-method-requestmodels): 
    Key : Value
  [RequestParameters](#cfn-apigateway-method-requestparameters): 
    Key : Value
  [RequestValidatorId](#cfn-apigateway-method-requestvalidatorid): String
  [ResourceId](#cfn-apigateway-method-resourceid): String
  [RestApiId](#cfn-apigateway-method-restapiid): String
```

## Properties<a name="aws-resource-apigateway-method-properties"></a>

`ApiKeyRequired`  <a name="cfn-apigateway-method-apikeyrequired"></a>
Indicates whether the method requires clients to submit a valid API key\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizationScopes`  <a name="cfn-apigateway-method-authorizationscopes"></a>
A list of authorization scopes configured on the method\. The scopes are used with a `COGNITO_USER_POOLS` authorizer to authorize the method invocation\. The authorization works by matching the method scopes against the scopes parsed from the access token in the incoming request\. The method invocation is authorized if any method scopes match a claimed scope in the access token\. Otherwise, the invocation is not authorized\. When the method scope is configured, the client must provide an access token instead of an identity token for authorization purposes\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizationType`  <a name="cfn-apigateway-method-authorizationtype"></a>
The method's authorization type\. This parameter is required\. For valid values, see [Method](https://docs.aws.amazon.com/apigateway/api-reference/resource/method/) in the *API Gateway API Reference*\.  
If you specify the `AuthorizerId` property, specify `CUSTOM` or `COGNITO_USER_POOLS` for this property\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerId`  <a name="cfn-apigateway-method-authorizerid"></a>
The identifier of the [authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-authorizer.html) to use on this method\. If you specify this property, specify `CUSTOM` or `COGNITO_USER_POOLS` for the `AuthorizationType` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-apigateway-method-httpmethod"></a>
The HTTP method that clients use to call this method\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Integration`  <a name="cfn-apigateway-method-integration"></a>
The backend system that the method calls when it receives a request\.  
*Required*: No  
*Type*: [Integration](aws-properties-apitgateway-method-integration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MethodResponses`  <a name="cfn-apigateway-method-methodresponses"></a>
The responses that can be sent to the client who calls the method\.  
*Required*: No  
*Type*: List of [MethodResponse](aws-properties-apitgateway-method-methodresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperationName`  <a name="cfn-apigateway-method-operationname"></a>
A friendly operation name for the method\. For example, you can assign the `OperationName` of `ListPets` for the `GET /pets` method\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestModels`  <a name="cfn-apigateway-method-requestmodels"></a>
The resources that are used for the request's content type\. Specify request models as key\-value pairs \(string\-to\-string mapping\), with a content type as the key and a `Model` resource name as the value\.   
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestParameters`  <a name="cfn-apigateway-method-requestparameters"></a>
The request parameters that API Gateway accepts\. Specify request parameters as key\-value pairs \(string\-to\-Boolean mapping\), with a source as the key and a Boolean as the value\. The Boolean specifies whether a parameter is required\. A source must match the format `method.request.location.name`, where the location is querystring, path, or header, and *name* is a valid, unique parameter name\.  
*Required*: No  
*Type*: Map of Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestValidatorId`  <a name="cfn-apigateway-method-requestvalidatorid"></a>
The ID of the associated request validator\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-apigateway-method-resourceid"></a>
The ID of an API Gateway [resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-resource.html)\. For root resource methods, specify the `RestApi` root resource ID, such as `{ "Fn::GetAtt": ["MyRestApi", "RootResourceId"] }`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-method-restapiid"></a>
The ID of the [RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) resource in which API Gateway creates the method\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-method-return-values"></a>

### Ref<a name="aws-resource-apigateway-method-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the method ID, such as `mysta-metho-01234b567890example`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-method--examples"></a>



### Mock Method<a name="aws-resource-apigateway-method--examples--Mock_Method"></a>

The following example creates a mock GET method for the `MyApi` API\.

#### JSON<a name="aws-resource-apigateway-method--examples--Mock_Method--json"></a>

```
{
    "MockMethod": {
        "Type": "AWS::ApiGateway::Method",
        "Properties": {
            "RestApiId": {
                "Ref": "MyApi"
            },
            "ResourceId": {
                "Fn::GetAtt": [
                    "MyApi",
                    "RootResourceId"
                ]
            },
            "HttpMethod": "GET",
            "AuthorizationType": "NONE",
            "Integration": {
                "Type": "MOCK"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-method--examples--Mock_Method--yaml"></a>

```
MockMethod:
  Type: 'AWS::ApiGateway::Method'
  Properties:
    RestApiId: !Ref MyApi
    ResourceId: !GetAtt 
      - MyApi
      - RootResourceId
    HttpMethod: GET
    AuthorizationType: NONE
    Integration:
      Type: MOCK
```

### Lambda Proxy<a name="aws-resource-apigateway-method--examples--Lambda_Proxy"></a>

The following example creates a proxy resource to enable clients to call a Lambda function with a single integration setup on a catch\-all ANY method\. The `Uri` property specifies the Lambda function\. For more information about Lambda proxy integration and a sample Lambda function, see [Create an API with Lambda Proxy Integration through a Proxy Resource](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-create-api-as-simple-proxy-for-lambda.html) in the *API Gateway Developer Guide*\.

**Note**  
Use the [AWS::Lambda::Permission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-permission.html) resource to grant API Gateway permission to invoke your Lambda function\.

#### JSON<a name="aws-resource-apigateway-method--examples--Lambda_Proxy--json"></a>

```
{
    "ProxyResource": {
        "Type": "AWS::ApiGateway::Resource",
        "Properties": {
            "RestApiId": {
                "Ref": "LambdaSimpleProxy"
            },
            "ParentId": {
                "Fn::GetAtt": [
                    "LambdaSimpleProxy",
                    "RootResourceId"
                ]
            },
            "PathPart": "{proxy+}"
        }
    },
    "ProxyResourceANY": {
        "Type": "AWS::ApiGateway::Method",
        "Properties": {
            "RestApiId": {
                "Ref": "LambdaSimpleProxy"
            },
            "ResourceId": {
                "Ref": "ProxyResource"
            },
            "HttpMethod": "ANY",
            "AuthorizationType": "NONE",
            "Integration": {
                "Type": "AWS_PROXY",
                "IntegrationHttpMethod": "POST",
                "Uri": {
                    "Fn::Sub": "arn:aws:apigateway:${AWS::Region}:lambda:path/2015-03-31/functions/${LambdaForSimpleProxy.Arn}/invocations"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-method--examples--Lambda_Proxy--yaml"></a>

```
ProxyResource:
  Type: 'AWS::ApiGateway::Resource'
  Properties:
    RestApiId: !Ref LambdaSimpleProxy
    ParentId: !GetAtt 
      - LambdaSimpleProxy
      - RootResourceId
    PathPart: '{proxy+}'
ProxyResourceANY:
  Type: 'AWS::ApiGateway::Method'
  Properties:
    RestApiId: !Ref LambdaSimpleProxy
    ResourceId: !Ref ProxyResource
    HttpMethod: ANY
    AuthorizationType: NONE
    Integration:
      Type: AWS_PROXY
      IntegrationHttpMethod: POST
      Uri: !Sub >-
        arn:aws:apigateway:${AWS::Region}:lambda:path/2015-03-31/functions/${LambdaForSimpleProxy.Arn}/invocations
```

### Associated Request Validator<a name="aws-resource-apigateway-method--examples--Associated_Request_Validator"></a>

The following example creates a REST API, method, and request validator, and associates the request validator with the method\. It also lets you specify how to convert the request payload\.

#### JSON<a name="aws-resource-apigateway-method--examples--Associated_Request_Validator--json"></a>

```
{
  "Parameters": {
    "contentHandling": {
      "Type": "String"
    },
    "operationName": {
      "Type": "String",
      "Default": "testoperationName"
    },
    "restApiName": {
      "Type": "String",
      "Default": "testrestApiName"
    },
    "validatorName": {
      "Type": "String",
      "Default": "testvalidatorName"
    },
    "validateRequestBody": {
      "Type": "String",
      "Default": "testvalidateRequestBody"
    },
    "validateRequestParameters": {
      "Type": "String",
      "Default": true
    }
  },
  "Resources": {
    "RestApi": {
      "Type": "AWS::ApiGateway::RestApi",
      "Properties": {
        "Name": {
          "Ref": "restApiName"
        }
      }
    },
    "Method": {
      "Type": "AWS::ApiGateway::Method",
      "Properties": {
        "HttpMethod": "POST",
        "ResourceId": {
          "Fn::GetAtt": [
            "RestApi",
            "RootResourceId"
          ]
        },
        "RestApiId": {
          "Ref": "RestApi"
        },
        "AuthorizationType": "NONE",
        "Integration": {
          "Type": "MOCK",
          "ContentHandling": {
            "Ref": "contentHandling"
          },
          "IntegrationResponses": [
            {
              "ContentHandling": {
                "Ref": "contentHandling"
              },
              "StatusCode": 400
            }
          ]
        },
        "RequestValidatorId": {
          "Ref": "RequestValidator"
        },
        "OperationName": {
          "Ref": "operationName"
        }
      }
    },
    "RequestValidator": {
      "Type": "AWS::ApiGateway::RequestValidator",
      "Properties": {
        "Name": {
          "Ref": "validatorName"
        },
        "RestApiId": {
          "Ref": "RestApi"
        },
        "ValidateRequestBody": {
          "Ref": "validateRequestBody"
        },
        "ValidateRequestParameters": {
          "Ref": "validateRequestParameters"
        }
      }
    }
  },
  "Outputs": {
    "RootResourceId": {
      "Value": {
        "Fn::GetAtt": [
          "RestApi",
          "RootResourceId"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-method--examples--Associated_Request_Validator--yaml"></a>

```
Parameters:
  contentHandling:
    Type: String
  operationName:
    Type: String
    Default: testoperationName
  restApiName:
    Type: String
    Default: testrestApiName
  validatorName:
    Type: String
    Default: testvalidatorName
  validateRequestBody:
    Type: String
    Default: testvalidateRequestBody
  validateRequestParameters:
    Type: String
    Default: true
Resources:
  RestApi:
    Type: AWS::ApiGateway::RestApi
    Properties:
      Name: !Ref restApiName
  Method:
    Type: AWS::ApiGateway::Method
    Properties:
      HttpMethod: POST
      ResourceId: !GetAtt RestApi.RootResourceId
      RestApiId: !Ref RestApi
      AuthorizationType: NONE
      Integration:
        Type: MOCK
        ContentHandling: !Ref contentHandling
        IntegrationResponses:
          - ContentHandling: !Ref contentHandling
            StatusCode: 400
      RequestValidatorId: !Ref RequestValidator
      OperationName: !Ref operationName
  RequestValidator:
    Type: AWS::ApiGateway::RequestValidator
    Properties:
      Name: !Ref validatorName
      RestApiId: !Ref RestApi
      ValidateRequestBody: !Ref validateRequestBody
      ValidateRequestParameters: !Ref validateRequestParameters
Outputs:
  RootResourceId:
    Value: !GetAtt RestApi.RootResourceId
```

## See also<a name="aws-resource-apigateway-method--seealso"></a>
+ [method:put](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/method-put/) in the *Amazon API Gateway REST API Reference*

