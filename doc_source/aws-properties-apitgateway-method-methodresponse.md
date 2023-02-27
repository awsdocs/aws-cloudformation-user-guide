# AWS::ApiGateway::Method MethodResponse<a name="aws-properties-apitgateway-method-methodresponse"></a>

Represents a method response of a given HTTP status code returned to the client\. The method response is passed from the back end through the associated integration response that can be transformed using a mapping template\. 

## Syntax<a name="aws-properties-apitgateway-method-methodresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apitgateway-method-methodresponse-syntax.json"></a>

```
{
  "[ResponseModels](#cfn-apigateway-method-methodresponse-responsemodels)" : {Key : Value, ...},
  "[ResponseParameters](#cfn-apigateway-method-methodresponse-responseparameters)" : {Key : Value, ...},
  "[StatusCode](#cfn-apigateway-method-methodresponse-statuscode)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-methodresponse-syntax.yaml"></a>

```
  [ResponseModels](#cfn-apigateway-method-methodresponse-responsemodels): 
    Key : Value
  [ResponseParameters](#cfn-apigateway-method-methodresponse-responseparameters): 
    Key : Value
  [StatusCode](#cfn-apigateway-method-methodresponse-statuscode): String
```

## Properties<a name="aws-properties-apitgateway-method-methodresponse-properties"></a>

`ResponseModels`  <a name="cfn-apigateway-method-methodresponse-responsemodels"></a>
Specifies the Model resources used for the response's content\-type\. Response models are represented as a key/value map, with a content\-type as the key and a Model name as the value\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseParameters`  <a name="cfn-apigateway-method-methodresponse-responseparameters"></a>
A key\-value map specifying required or optional response parameters that API Gateway can send back to the caller\. A key defines a method response header and the value specifies whether the associated method response header is required or not\. The expression of the key must match the pattern `method.response.header.{name}`, where `name` is a valid and unique header name\. API Gateway passes certain integration response data to the method response headers specified here according to the mapping you prescribe in the API's IntegrationResponse\. The integration response data that can be mapped include an integration response header expressed in `integration.response.header.{name}`, a static value enclosed within a pair of single quotes \(e\.g\., `'application/json'`\), or a JSON expression from the back\-end response payload in the form of `integration.response.body.{JSON-expression}`, where `JSON-expression` is a valid JSON expression without the `$` prefix\.\)  
*Required*: No  
*Type*: Map of Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-apigateway-method-methodresponse-statuscode"></a>
The method response's status code\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apitgateway-method-methodresponse--seealso"></a>
+ [Method](https://docs.aws.amazon.com/apigateway/latest/api/API_Method.html) in the *Amazon API Gateway REST API Reference*

