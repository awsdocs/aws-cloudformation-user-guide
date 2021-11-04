# AWS::ApiGateway::Method MethodResponse<a name="aws-properties-apitgateway-method-methodresponse"></a>

`MethodResponse` is a property of the [AWS::ApiGateway::Method](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html) resource that defines the responses that can be sent to the client that calls a method\.

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
The resources used for the response's content type\. Specify response models as key\-value pairs \(string\-to\-string maps\), with a content type as the key and a [Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-model.html) resource name as the value\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseParameters`  <a name="cfn-apigateway-method-methodresponse-responseparameters"></a>
Response parameters that API Gateway sends to the client that called a method\. Specify response parameters as key\-value pairs \(string\-to\-Boolean maps\), with a destination as the key and a Boolean as the value\. Specify the destination using the following pattern: `method.response.header.name`, where *name* is a valid, unique header name\. The Boolean specifies whether a parameter is required\.  
*Required*: No  
*Type*: Map of Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-apigateway-method-methodresponse-statuscode"></a>
The method response's status code, which you map to an [IntegrationResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apitgateway-method-integration-integrationresponse.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apitgateway-method-methodresponse--seealso"></a>
+ [Method](https://docs.aws.amazon.com/apigateway/api-reference/resource/method/) in the *Amazon API Gateway REST API Reference*

