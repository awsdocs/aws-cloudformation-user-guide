# Amazon API Gateway Method Integration IntegrationResponse<a name="aws-properties-apitgateway-method-integration-integrationresponse"></a>

`IntegrationResponse` is a property of the [Amazon API Gateway Method Integration IntegrationResponse](#aws-properties-apitgateway-method-integration-integrationresponse) property that specifies the response that Amazon API Gateway \(API Gateway\) sends after a method's backend finishes processing a request\.

## Syntax<a name="w3ab2c21c14c27b5"></a>

### JSON<a name="aws-properties-apitgateway-method-integration-integrationresponse-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integrationresponse-contenthandling)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-responseparameters)" : { String:String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-responsetemplates)" : { String:String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-selectionpattern)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-statuscode)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-integration-integrationresponse-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integrationresponse-contenthandling): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-responseparameters):
  String: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-responsetemplates):
  String: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-selectionpattern): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-method-integration-integrationresponse-statuscode): String
```

## Properties<a name="w3ab2c21c14c27b7"></a>

`ContentHandling`  
Specifies how to handle request payload content type conversions\. Valid values are:  

+ `CONVERT_TO_BINARY`: Converts a request payload from a base64\-encoded string to a binary blob\.

+ `CONVERT_TO_TEXT`: Converts a request payload from a binary blob to a base64\-encoded string\.
If this property isn't defined, the request payload is passed through from the method request to the integration request without modification\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`ResponseParameters`  
The response parameters from the backend response that API Gateway sends to the method response\. Specify response parameters as key\-value pairs \(string\-to\-string mappings\)\.  
Use the destination as the key and the source as the value:  

+ The destination must be an existing response parameter in the `MethodResponse` property\.

+ The source must be an existing method request parameter or a static value\. You must enclose static values in single quotation marks and pre\-encode these values based on the destination specified in the request\.
For more information, see [API Gateway API Request and Response Parameter\-Mapping Reference](http://docs.aws.amazon.com/apigateway/latest/developerguide/request-response-data-mappings.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Mapping of key\-value pairs

`ResponseTemplates`  
The templates that are used to transform the integration response body\. Specify templates as key\-value pairs \(string\-to\-string mappings\), with a content type as the key and a template as the value\. For more information, see [API Gateway API Request and Response Payload\-Mapping Template Reference](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: Mapping of key\-value pairs

`SelectionPattern`  
A regular expression that specifies which error strings or status codes from the backend map to the integration response\.  
*Required: *No  
*Type*: String

`StatusCode`  
The status code that API Gateway uses to map the integration response to a `MethodResponse` status code\.  
*Required: *Yes  
*Type*: String