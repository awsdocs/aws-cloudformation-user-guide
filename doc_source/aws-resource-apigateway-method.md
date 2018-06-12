# AWS::ApiGateway::Method<a name="aws-resource-apigateway-method"></a>

The `AWS::ApiGateway::Method` resource creates Amazon API Gateway \(API Gateway\) methods that define the parameters and body that clients must send in their requests\.

**Topics**
+ [Syntax](#aws-resource-apigateway-method-syntax)
+ [Properties](#w3ab2c21c10c58b9)
+ [Return Value](#w3ab2c21c10c58c11)
+ [Examples](#aws-resource-apigateway-method-examples)
+ [See Also](#aws-resource-apigateway-method-seealso)

## Syntax<a name="aws-resource-apigateway-method-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-method-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Method",
  "Properties" : {
    "[ApiKeyRequired](#cfn-apigateway-method-apikeyrequired)" : Boolean,
    "[AuthorizationType](#cfn-apigateway-method-authorizationtype)" : String,
    "[AuthorizerId](#cfn-apigateway-method-authorizerid)" : String,
    "[HttpMethod](#cfn-apigateway-method-httpmethod)" : String,
    "[Integration](#cfn-apigateway-method-integration)" : [Integration](aws-properties-apitgateway-method-integration.md),
    "[MethodResponses](#cfn-apigateway-method-methodresponses)" : [ [MethodResponse](aws-properties-apitgateway-method-methodresponse.md), ... ],
    "[OperationName](#cfn-apigateway-method-operationname)" : String,
    "[RequestModels](#cfn-apigateway-method-requestmodels)" : { String:String, ... },
    "[RequestParameters](#cfn-apigateway-method-requestparameters)" : { String:Boolean, ... },
    "[RequestValidatorId](#cfn-apigateway-method-requestvalidatorid)" : String,
    "[ResourceId](#cfn-apigateway-method-resourceid)" : String,
    "[RestApiId](#cfn-apigateway-method-restapiid)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-method-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Method"
Properties:
  [ApiKeyRequired](#cfn-apigateway-method-apikeyrequired): Boolean
  [AuthorizationType](#cfn-apigateway-method-authorizationtype): String
  [AuthorizerId](#cfn-apigateway-method-authorizerid): String
  [HttpMethod](#cfn-apigateway-method-httpmethod): String
  [Integration](#cfn-apigateway-method-integration):
    [Integration](aws-properties-apitgateway-method-integration.md)
  [MethodResponses](#cfn-apigateway-method-methodresponses):
    - [MethodResponse](aws-properties-apitgateway-method-methodresponse.md)
  [OperationName](#cfn-apigateway-method-operationname): String
  [RequestModels](#cfn-apigateway-method-requestmodels):
    String: String
  [RequestParameters](#cfn-apigateway-method-requestparameters):
    String: Boolean
  [RequestValidatorId](#cfn-apigateway-method-requestvalidatorid): String
  [ResourceId](#cfn-apigateway-method-resourceid): String
  [RestApiId](#cfn-apigateway-method-restapiid): String
```

## Properties<a name="w3ab2c21c10c58b9"></a>

`ApiKeyRequired`  <a name="cfn-apigateway-method-apikeyrequired"></a>
Indicates whether the method requires clients to submit a valid API key\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizationType`  <a name="cfn-apigateway-method-authorizationtype"></a>
The method's authorization type\.  
*Required*: Yes\. If you specify the `AuthorizerId` property, specify `CUSTOM` for this property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AuthorizerId`  <a name="cfn-apigateway-method-authorizerid"></a>
The identifier of the [authorizer](aws-resource-apigateway-authorizer.md) to use on this method\. If you specify this property, specify `CUSTOM` for the `AuthorizationType` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HttpMethod`  <a name="cfn-apigateway-method-httpmethod"></a>
The HTTP method that clients use to call this method\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Integration`  <a name="cfn-apigateway-method-integration"></a>
The backend system that the method calls when it receives a request\.  
*Required*: No  
*Type*: [Amazon API Gateway Method Integration](aws-properties-apitgateway-method-integration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MethodResponses`  <a name="cfn-apigateway-method-methodresponses"></a>
The responses that can be sent to the client who calls the method\.  
*Required*: No  
*Type*: List of [Amazon API Gateway Method MethodResponse](aws-properties-apitgateway-method-methodresponse.md) property types\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OperationName`  <a name="cfn-apigateway-method-operationname"></a>
A friendly operation name for the method\. For example, you can assign the `OperationName` of *ListPets* for the `GET /pets` method\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RequestModels`  <a name="cfn-apigateway-method-requestmodels"></a>
The resources that are used for the response's content type\. Specify response models as key\-value pairs \(string\-to\-string mapping\), with a content type as the key and a `Model` resource name as the value\.  
*Required*: No  
*Type*: Mapping of key\-value pairs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RequestParameters`  <a name="cfn-apigateway-method-requestparameters"></a>
The request parameters that API Gateway accepts\. Specify request parameters as key\-value pairs \(string\-to\-Boolean mapping\), with a source as the key and a Boolean as the value\. The Boolean specifies whether a parameter is required\. A source must match the format `method.request.location.name`, where the *location* is `querystring`, `path`, or `header`, and *name* is a valid, unique parameter name\.  
*Required*: No  
*Type*: Mapping of key\-value pairs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RequestValidatorId`  <a name="cfn-apigateway-method-requestvalidatorid"></a>
The ID of the associated request validator\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceId`  <a name="cfn-apigateway-method-resourceid"></a>
The ID of an API Gateway [resource](aws-resource-apigateway-resource.md)\. For root resource methods, specify the RestApi root resource ID, such as `{ "Fn::GetAtt": ["MyRestApi", "RootResourceId"] }`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-method-restapiid"></a>
The ID of the [RestApi](aws-resource-apigateway-restapi.md) resource in which API Gateway creates the method\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10c58c11"></a>

### Ref<a name="w3ab2c21c10c58c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the method ID, such as `mysta-metho-01234b567890example`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-apigateway-method-examples"></a>

### Mock Method<a name="w3ab2c21c10c58c13b2"></a>

The following example creates a mock GET method for the `MyApi` API\.

#### JSON<a name="aws-resource-apigateway-method-example.json"></a>

```
"MockMethod": {
  "Type": "AWS::ApiGateway::Method",
  "Properties": {
    "RestApiId": { "Ref": "MyApi" },
    "ResourceId": { "Fn::GetAtt": ["RestApi", "RootResourceId"] },
    "HttpMethod": "GET",
    "AuthorizationType": "NONE",
    "Integration": { "Type": "MOCK" }
  }
}
```

#### YAML<a name="aws-resource-apigateway-method-example.yaml"></a>

```
MockMethod: 
  Type: "AWS::ApiGateway::Method"
  Properties: 
    RestApiId: 
      Ref: "MyApi"
    ResourceId: 
      Fn::GetAtt: 
        - "RestApi"
        - "RootResourceId"
    HttpMethod: "GET"
    AuthorizationType: "NONE"
    Integration: 
      Type: "MOCK"
```

### Lambda Proxy<a name="w3ab2c21c10c58c13b4"></a>

The following example creates a proxy resource to enable clients to call a Lambda function with a single integration setup on a catch\-all `ANY` method\. The `Uri` property specifies the Lambda function\. For more information about Lambda proxy integration and a sample Lambda function, see [Create an API with Lambda Proxy Integration through a Proxy Resource](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-create-api-as-simple-proxy-for-lambda.html) in the *API Gateway Developer Guide*\.

**Note**  
Use the [AWS::Lambda::Permission](aws-resource-lambda-permission.md) resource to grant API Gateway permission to invoke your Lambda function\.

#### JSON<a name="aws-resource-apigateway-method-example2.json"></a>

```
"ProxyResource": {
  "Type": "AWS::ApiGateway::Resource",
  "Properties": {
    "RestApiId": { "Ref":"LambdaSimpleProxy"},
    "ParentId": { "Fn::GetAtt" : [
      "LambdaSimpleProxy",
      "RootResourceId"
    ]},
    "PathPart": "{proxy+}"
  }
},
"ProxyResourceANY": {
  "Type": "AWS::ApiGateway::Method",
  "Properties": {
    "RestApiId": {"Ref":"LambdaSimpleProxy"},
    "ResourceId": {"Ref":"ProxyResource"},
    "HttpMethod": "ANY",
    "AuthorizationType": "NONE",
    "Integration": {
      "Type": "AWS_PROXY",
      "IntegrationHttpMethod": "POST",
      "Uri": { "Fn::Sub":"arn:aws:apigateway:${AWS::Region}:lambda:path/2015-03-31/functions/${LambdaForSimpleProxy.Arn}/invocations"}
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-method-example2.yaml"></a>

```
ProxyResource:
  Type: AWS::ApiGateway::Resource
  Properties:
    RestApiId: !Ref LambdaSimpleProxy
    ParentId: !GetAtt [LambdaSimpleProxy, RootResourceId]
    PathPart: '{proxy+}'
ProxyResourceANY:
  Type: AWS::ApiGateway::Method
  Properties:
    RestApiId: !Ref LambdaSimpleProxy
    ResourceId: !Ref ProxyResource
    HttpMethod: ANY      
    AuthorizationType: NONE
    Integration:
      Type: AWS_PROXY
      IntegrationHttpMethod: POST
      Uri: !Sub arn:aws:apigateway:${AWS::Region}:lambda:path/2015-03-31/functions/${LambdaForSimpleProxy.Arn}/invocations
```

### Associated Request Validator<a name="aws-resource-apigateway-method-example3"></a>

The following example creates a REST API, method, and request validator, and associates the request validator with the method\. It also lets you specify how to convert the request payload\.

#### JSON<a name="aws-resource-apigateway-method-example3.json"></a>

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

#### YAML<a name="aws-resource-apigateway-method-example3.yaml"></a>

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
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      Name: !Ref restApiName
  Method:
    Type: 'AWS::ApiGateway::Method'
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
    Type: 'AWS::ApiGateway::RequestValidator'
    Properties:
      Name: !Ref validatorName
      RestApiId: !Ref RestApi
      ValidateRequestBody: !Ref validateRequestBody
      ValidateRequestParameters: !Ref validateRequestParameters
Outputs:
  RootResourceId:
    Value: !GetAtt RestApi.RootResourceId
```

## See Also<a name="aws-resource-apigateway-method-seealso"></a>
+ [Method](http://docs.aws.amazon.com/apigateway/api-reference/resource/method/) in the *Amazon API Gateway REST API Reference* 