# AWS::ApiGateway::RequestValidator<a name="aws-resource-apigateway-requestvalidator"></a>

The `AWS::ApiGateway::RequestValidator` resource sets up basic validation rules for incoming requests to your API\. For more information, see [Enable Basic Request Validation for an API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-method-request-validation.html) in the *API Gateway Developer Guide*\.

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
Type: AWS::ApiGateway::RequestValidator
Properties: 
  [Name](#cfn-apigateway-requestvalidator-name): String
  [RestApiId](#cfn-apigateway-requestvalidator-restapiid): String
  [ValidateRequestBody](#cfn-apigateway-requestvalidator-validaterequestbody): Boolean
  [ValidateRequestParameters](#cfn-apigateway-requestvalidator-validaterequestparameters): Boolean
```

## Properties<a name="aws-resource-apigateway-requestvalidator-properties"></a>

`Name`  <a name="cfn-apigateway-requestvalidator-name"></a>
The name of this request validator\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-requestvalidator-restapiid"></a>
The identifier of the targeted API entity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidateRequestBody`  <a name="cfn-apigateway-requestvalidator-validaterequestbody"></a>
Indicates whether to validate the request body according to the configured schema for the targeted API and method\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidateRequestParameters`  <a name="cfn-apigateway-requestvalidator-validaterequestparameters"></a>
Indicates whether to validate request parameters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-requestvalidator-return-values"></a>

### Ref<a name="aws-resource-apigateway-requestvalidator-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the request validator, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-requestvalidator--examples"></a>



### Create request validator<a name="aws-resource-apigateway-requestvalidator--examples--Create_request_validator"></a>

The following example creates an API Gateway API with an associated request validator, based on the supplied parameters\.

#### JSON<a name="aws-resource-apigateway-requestvalidator--examples--Create_request_validator--json"></a>

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

#### YAML<a name="aws-resource-apigateway-requestvalidator--examples--Create_request_validator--yaml"></a>

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
    Type: AWS::ApiGateway::RestApi
    Properties:
      Name: !Ref apiName
  RequestValidator:
    Type: AWS::ApiGateway::RequestValidator
    Properties:
      Name: !Ref validatorName
      RestApiId: !Ref RestApi
      ValidateRequestBody: !Ref validateRequestBody
      ValidateRequestParameters: !Ref validateRequestParameters
```

## See also<a name="aws-resource-apigateway-requestvalidator--seealso"></a>
+ [requestvalidator:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/requestvalidator-create/) in the *Amazon API Gateway REST API Reference*

