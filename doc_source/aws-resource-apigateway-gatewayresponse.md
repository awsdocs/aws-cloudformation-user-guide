# AWS::ApiGateway::GatewayResponse<a name="aws-resource-apigateway-gatewayresponse"></a>

The `AWS::ApiGateway::GatewayResponse` resource creates a custom response for your API Gateway API\. For more information, see [API Gateway Responses ](http://docs.aws.amazon.com/apigateway/latest/developerguide/customize-gateway-responses.html#api-gateway-gatewayResponse-definition) in the *API Gateway Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-apigateway-gatewayresponse-syntax)
+ [Properties](#aws-resource-apigateway-gatewayresponse-properties)
+ [Examples](#aws-resource-apigateway-gatewayresponse-examples)

## Syntax<a name="aws-resource-apigateway-gatewayresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-gatewayresponse-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::GatewayResponse",
  "Properties" : {
    "[ResponseParameters](#cfn-apigateway-gatewayresponse-responseparameters)" : { String:String, ... },
    "[ResponseTemplates](#cfn-apigateway-gatewayresponse-responsetemplates)" : { String:String, ... },
    "[ResponseType](#cfn-apigateway-gatewayresponse-responsetype)" : String,
    "[RestApiId](#cfn-apigateway-gatewayresponse-restapiid)" : String,
    "[StatusCode](#cfn-apigateway-gatewayresponse-statuscode)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-gatewayresponse-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::GatewayResponse"
Properties:
  [ResponseParameters](#cfn-apigateway-gatewayresponse-responseparameters): 
    String: String
  [ResponseTemplates](#cfn-apigateway-gatewayresponse-responsetemplates): 
    String: String
  [ResponseType](#cfn-apigateway-gatewayresponse-responsetype): String
  [RestApiId](#cfn-apigateway-gatewayresponse-restapiid): String
  [StatusCode](#cfn-apigateway-gatewayresponse-statuscode): String
```

## Properties<a name="aws-resource-apigateway-gatewayresponse-properties"></a>

`ResponseParameters`  <a name="cfn-apigateway-gatewayresponse-responseparameters"></a>
The response parameters \(paths, query strings, and headers\) for the response\. Duplicates not allowed\.  
 *Required*: No  
 *Type*: String to string map  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseTemplates`  <a name="cfn-apigateway-gatewayresponse-responsetemplates"></a>
The response templates for the response\. Duplicates not allowed\.  
 *Required*: No  
 *Type*: String to string map  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseType`  <a name="cfn-apigateway-gatewayresponse-responsetype"></a>
The response type\. For valid values, see [GatewayResponse](http://docs.aws.amazon.com/apigateway/api-reference/resource/gateway-response/) in the *API Gateway API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RestApiId`  <a name="cfn-apigateway-gatewayresponse-restapiid"></a>
The identifier of the targeted API entity\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`StatusCode`  <a name="cfn-apigateway-gatewayresponse-statuscode"></a>
The HTTP status code for the response\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-apigateway-gatewayresponse-examples"></a>

### 404 Response<a name="aws-resource-apigateway-gatewayresponse-example2"></a>

The following example returns a 404 status code for resource not found instead of missing authentication token for a CORS request \(applicable to unsecured/unrestricted APIs\)\.

#### JSON<a name="aws-resource-apigateway-gatewayresponse-example2.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "RestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Name": "myRestApi"
            }
        },
        "GatewayResponse": {
            "Type": "AWS::ApiGateway::GatewayResponse",
            "Properties": {
                "ResponseParameters": {
                    "gatewayresponse.header.Access-Control-Allow-Origin": "'*'",
                    "gatewayresponse.header.Access-Control-Allow-Headers": "'*'"
                },
                "ResponseType": "MISSING_AUTHENTICATION_TOKEN",
                "RestApiId": {
                    "Ref": "RestApi"
                },
                "StatusCode": "404"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-gatewayresponse-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  RestApi:
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      Name: myRestApi
  GatewayResponse:
    Type: 'AWS::ApiGateway::GatewayResponse'
    Properties:
      ResponseParameters:
        gatewayresponse.header.Access-Control-Allow-Origin: "'*'"
        gatewayresponse.header.Access-Control-Allow-Headers: "'*'"
      ResponseType: MISSING_AUTHENTICATION_TOKEN
      RestApiId: !Ref RestApi
      StatusCode: '404'
```

### Parameterized Response<a name="aws-resource-apigateway-gatewayresponse-example1"></a>

The following example creates a response for an API based on the supplied parameters\.

#### JSON<a name="aws-resource-apigateway-gatewayresponse-example1.json"></a>

```
{
    "Parameters": {
        "apiName": {
            "Type": "String"
        },
        "responseParameter1": {
            "Type": "String"
        },
        "responseParameter2": {
            "Type": "String"
        },
        "responseType": {
            "Type": "String"
        },
        "statusCode": {
            "Type": "String"
        }
    },
    "Resources": {
        "RestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Name": {
                    "Ref": "apiName"
                }
            }
        },
        "GatewayResponse": {
            "Type": "AWS::ApiGateway::GatewayResponse",
            "Properties": {
                "ResponseParameters": {
                    "gatewayresponse.header.k1": {
                        "Ref": "responseParameter1"
                    },
                    "gatewayresponse.header.k2": {
                        "Ref": "responseParameter2"
                    }
                },
                "ResponseType": {
                    "Ref": "responseType"
                },
                "RestApiId": {
                    "Ref": "RestApi"
                },
                "StatusCode": {
                    "Ref": "statusCode"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-gatewayresponse-example1.yaml"></a>

```
Parameters:
    apiName :
        Type : String
    responseParameter1:
        Type : String
    responseParameter2:
        Type : String
    responseType:
        Type : String
    statusCode:
        Type : String
Resources :
    RestApi:
        Type: AWS::ApiGateway::RestApi
        Properties:
            Name: !Ref apiName
    GatewayResponse:
        Type: AWS::ApiGateway::GatewayResponse
        Properties:
            ResponseParameters:
                gatewayresponse.header.k1 : !Ref responseParameter1
                gatewayresponse.header.k2 : !Ref responseParameter2
            ResponseType: !Ref responseType
            RestApiId: !Ref RestApi
            StatusCode: !Ref statusCode
```