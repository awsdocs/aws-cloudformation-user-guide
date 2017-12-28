# Amazon API Gateway Method MethodResponse<a name="aws-properties-apitgateway-method-methodresponse"></a>

`MethodResponse` is a property of the [AWS::ApiGateway::Method](aws-resource-apigateway-method.md) resource that defines the responses that can be sent to the client who calls an Amazon API Gateway \(API Gateway\) method\.

## Syntax<a name="w3ab2c21c14c30b5"></a>

### JSON<a name="aws-properties-apitgateway-method-methodresponse-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-responsemodels)" : { String:String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-responseparameters)" : { String:Boolean, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-statuscode)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-methodresponse-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-responsemodels):
  String: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-responseparameters):
  String: Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-methodresponse-statuscode): String
```

## Properties<a name="w3ab2c21c14c30b7"></a>

`ResponseModels`  
The resources used for the response's content type\. Specify response models as key\-value pairs \(string\-to\-string maps\), with a content type as the key and a `Model` resource name as the value\.  
*Required: *No  
*Type*: Mapping of key\-value pairs

`ResponseParameters`  
Response parameters that API Gateway sends to the client that called a method\. Specify response parameters as key\-value pairs \(string\-to\-Boolean maps\), with a destination as the key and a Boolean as the value\. Specify the destination using the following pattern: `method.response.header.name`, where the `name` is a valid, unique header name\. The Boolean specifies whether a parameter is required\.  
*Required: *No  
*Type*: Mapping of key\-value pairs

`StatusCode`  
The method response's status code, which you map to an `IntegrationResponse`\.  
*Required: *Yes  
*Type*: String