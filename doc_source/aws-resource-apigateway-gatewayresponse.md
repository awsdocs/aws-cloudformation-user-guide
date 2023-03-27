# AWS::ApiGateway::GatewayResponse<a name="aws-resource-apigateway-gatewayresponse"></a>

The `AWS::ApiGateway::GatewayResponse` resource creates a gateway response for your API\. For more information, see [API Gateway Responses](https://docs.aws.amazon.com/apigateway/latest/developerguide/customize-gateway-responses.html#api-gateway-gatewayResponse-definition) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigateway-gatewayresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-gatewayresponse-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::GatewayResponse",
  "Properties" : {
      "[ResponseParameters](#cfn-apigateway-gatewayresponse-responseparameters)" : {Key : Value, ...},
      "[ResponseTemplates](#cfn-apigateway-gatewayresponse-responsetemplates)" : {Key : Value, ...},
      "[ResponseType](#cfn-apigateway-gatewayresponse-responsetype)" : String,
      "[RestApiId](#cfn-apigateway-gatewayresponse-restapiid)" : String,
      "[StatusCode](#cfn-apigateway-gatewayresponse-statuscode)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-gatewayresponse-syntax.yaml"></a>

```
Type: AWS::ApiGateway::GatewayResponse
Properties: 
  [ResponseParameters](#cfn-apigateway-gatewayresponse-responseparameters): 
    Key : Value
  [ResponseTemplates](#cfn-apigateway-gatewayresponse-responsetemplates): 
    Key : Value
  [ResponseType](#cfn-apigateway-gatewayresponse-responsetype): String
  [RestApiId](#cfn-apigateway-gatewayresponse-restapiid): String
  [StatusCode](#cfn-apigateway-gatewayresponse-statuscode): String
```

## Properties<a name="aws-resource-apigateway-gatewayresponse-properties"></a>

`ResponseParameters`  <a name="cfn-apigateway-gatewayresponse-responseparameters"></a>
Response parameters \(paths, query strings and headers\) of the GatewayResponse as a string\-to\-string map of key\-value pairs\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseTemplates`  <a name="cfn-apigateway-gatewayresponse-responsetemplates"></a>
Response templates of the GatewayResponse as a string\-to\-string map of key\-value pairs\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseType`  <a name="cfn-apigateway-gatewayresponse-responsetype"></a>
The response type of the associated GatewayResponse\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ACCESS_DENIED | API_CONFIGURATION_ERROR | AUTHORIZER_CONFIGURATION_ERROR | AUTHORIZER_FAILURE | BAD_REQUEST_BODY | BAD_REQUEST_PARAMETERS | DEFAULT_4XX | DEFAULT_5XX | EXPIRED_TOKEN | INTEGRATION_FAILURE | INTEGRATION_TIMEOUT | INVALID_API_KEY | INVALID_SIGNATURE | MISSING_AUTHENTICATION_TOKEN | QUOTA_EXCEEDED | REQUEST_TOO_LARGE | RESOURCE_NOT_FOUND | THROTTLED | UNAUTHORIZED | UNSUPPORTED_MEDIA_TYPE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-gatewayresponse-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StatusCode`  <a name="cfn-apigateway-gatewayresponse-statuscode"></a>
The HTTP status code for this GatewayResponse\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-gatewayresponse-return-values"></a>

### Fn::GetAtt<a name="aws-resource-apigateway-gatewayresponse-return-values-fn--getatt"></a>

#### <a name="aws-resource-apigateway-gatewayresponse-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID for the gateway response\. For example: `abc123`\.

## Examples<a name="aws-resource-apigateway-gatewayresponse--examples"></a>



### 404 Response<a name="aws-resource-apigateway-gatewayresponse--examples--404_Response"></a>

The following example returns a 404 status code for resource not found instead of missing authentication token for a CORS request \(applicable to unsecured/unrestricted APIs\)\.

#### JSON<a name="aws-resource-apigateway-gatewayresponse--examples--404_Response--json"></a>

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

#### YAML<a name="aws-resource-apigateway-gatewayresponse--examples--404_Response--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  RestApi:
    Type: AWS::ApiGateway::RestApi
    Properties:
      Name: myRestApi
  GatewayResponse:
    Type: AWS::ApiGateway::GatewayResponse
    Properties:
      ResponseParameters:
        gatewayresponse.header.Access-Control-Allow-Origin: "'*'"
        gatewayresponse.header.Access-Control-Allow-Headers: "'*'"
      ResponseType: MISSING_AUTHENTICATION_TOKEN
      RestApiId: !Ref RestApi
      StatusCode: '404'
```

### Parameterized Response<a name="aws-resource-apigateway-gatewayresponse--examples--Parameterized_Response"></a>

The following example creates a response for an API based on the supplied parameters\.

#### JSON<a name="aws-resource-apigateway-gatewayresponse--examples--Parameterized_Response--json"></a>

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

#### YAML<a name="aws-resource-apigateway-gatewayresponse--examples--Parameterized_Response--yaml"></a>

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

## See also<a name="aws-resource-apigateway-gatewayresponse--seealso"></a>
+ [gatewayresponse:put](https://docs.aws.amazon.com/apigateway/latest/api/API_PutGatewayResponse.html) in the *Amazon API Gateway REST API Reference*

