# AWS::ApiGateway::RequestValidator<a name="aws-resource-apigateway-requestvalidator"></a>

The `AWS::ApiGateway::RequestValidator` resource sets up basic validation rules for incoming requests to your API Gateway API\. For more information, see [ Enable Basic Request Validation for an API in API Gateway](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-method-request-validation.html) in the *API Gateway Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-apigateway-requestvalidator-syntax)
+ [Properties](#w3ab2c21c10c68b9)
+ [Return Value](#aws-resource-apigateway-requestvalidator-returnvalues)
+ [Example](#aws-resource-apigateway-requestvalidator-examples)

## Syntax<a name="aws-resource-apigateway-requestvalidator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-requestvalidator-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::RequestValidator",
  "Properties" : {
    "[Name](#cfn-apigateway-requestvalidator-name)" : String,
    "[RestApiId](#cfn-apigateway-requestvalidator-restapiid)" : String,
    "[ValidateRequestBody](#cfn-apigateway-requestvalidator-validaterequestbody)" : Boolean,
    "[ValidateRequestParameters](#cfn-apigateway-requestvalidator-validaterequestparameters)" : Boolean
  }
}
```

### YAML<a name="aws-resource-apigateway-requestvalidator-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::RequestValidator"
Properties:
  [Name](#cfn-apigateway-requestvalidator-name): String
  [RestApiId](#cfn-apigateway-requestvalidator-restapiid): String
  [ValidateRequestBody](#cfn-apigateway-requestvalidator-validaterequestbody): Boolean
  [ValidateRequestParameters](#cfn-apigateway-requestvalidator-validaterequestparameters): Boolean
```

## Properties<a name="w3ab2c21c10c68b9"></a>

**Note**  
For more information about each property, see [ RequestValidator](http://docs.aws.amazon.com/apigateway/api-reference/resource/request-validator) in the *Amazon API Gateway REST API Reference*\.

`Name`  <a name="cfn-apigateway-requestvalidator-name"></a>
The name of this request validator\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RestApiId`  <a name="cfn-apigateway-requestvalidator-restapiid"></a>
The identifier of the targeted API entity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ValidateRequestBody`  <a name="cfn-apigateway-requestvalidator-validaterequestbody"></a>
Indicates whether to validate the request body according to the configured schema for the targeted API and method\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ValidateRequestParameters`  <a name="cfn-apigateway-requestvalidator-validaterequestparameters"></a>
Indicates whether to validate request parameters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-apigateway-requestvalidator-returnvalues"></a>

### Ref<a name="aws-resource-apigateway-requestvalidator-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ID of the request validator, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-apigateway-requestvalidator-examples"></a>

### <a name="w3ab2c21c10c68c13b3"></a>

The following example creates an API Gateway API with an associated request validator, based on the supplied parameters\.

#### JSON<a name="aws-resource-apigateway-requestvalidator-example1.json"></a>

```
{
    "Parameters": {
        "apiName": {
            "Type": "String"
        },
        "validatorName": {
            "Type": "String"
        },
        "validateRequestBody": {
            "Type": "String"
        },
        "validateRequestParameters": {
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
    }
}
```

#### YAML<a name="aws-resource-apigateway-requestvalidator-example1.yaml"></a>

```
Parameters:
  apiName:
    Type: String
  validatorName:
    Type: String
  validateRequestBody:
    Type: String
  validateRequestParameters:
    Type: String
Resources:
  RestApi:
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      Name: !Ref apiName
  RequestValidator:
    Type: 'AWS::ApiGateway::RequestValidator'
    Properties:
      Name: !Ref validatorName
      RestApiId: !Ref RestApi
      ValidateRequestBody: !Ref validateRequestBody
      ValidateRequestParameters: !Ref validateRequestParameters
```