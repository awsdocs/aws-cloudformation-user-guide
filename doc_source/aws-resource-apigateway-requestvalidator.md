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
The name of this RequestValidator  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-requestvalidator-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidateRequestBody`  <a name="cfn-apigateway-requestvalidator-validaterequestbody"></a>
A Boolean flag to indicate whether to validate a request body according to the configured Model schema\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidateRequestParameters`  <a name="cfn-apigateway-requestvalidator-validaterequestparameters"></a>
A Boolean flag to indicate whether to validate request parameters \(`true`\) or not \(`false`\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-requestvalidator-return-values"></a>

### Ref<a name="aws-resource-apigateway-requestvalidator-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the request validator, such as `abc123`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigateway-requestvalidator-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigateway-requestvalidator-return-values-fn--getatt-fn--getatt"></a>

`RequestValidatorId`  <a name="RequestValidatorId-fn::getatt"></a>
The ID for the request validator\. For example: `abc123`\.

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
+ [requestvalidator:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateRequestValidator.html) in the *Amazon API Gateway REST API Reference*

