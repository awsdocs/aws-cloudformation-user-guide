# AWS::ApiGateway::Method IntegrationResponse<a name="aws-properties-apitgateway-method-integration-integrationresponse"></a>

`IntegrationResponse` is a property of the [Amazon API Gateway Method Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apitgateway-method-integration.html) property type that specifies the response that API Gateway sends after a method's backend finishes processing a request\.

## Syntax<a name="aws-properties-apitgateway-method-integration-integrationresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apitgateway-method-integration-integrationresponse-syntax.json"></a>

```
{
  "[ContentHandling](#cfn-apigateway-method-integrationresponse-contenthandling)" : String,
  "[ResponseParameters](#cfn-apigateway-method-integration-integrationresponse-responseparameters)" : {Key : Value, ...},
  "[ResponseTemplates](#cfn-apigateway-method-integration-integrationresponse-responsetemplates)" : {Key : Value, ...},
  "[SelectionPattern](#cfn-apigateway-method-integration-integrationresponse-selectionpattern)" : String,
  "[StatusCode](#cfn-apigateway-method-integration-integrationresponse-statuscode)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-integration-integrationresponse-syntax.yaml"></a>

```
  [ContentHandling](#cfn-apigateway-method-integrationresponse-contenthandling): String
  [ResponseParameters](#cfn-apigateway-method-integration-integrationresponse-responseparameters): 
    Key : Value
  [ResponseTemplates](#cfn-apigateway-method-integration-integrationresponse-responsetemplates): 
    Key : Value
  [SelectionPattern](#cfn-apigateway-method-integration-integrationresponse-selectionpattern): String
  [StatusCode](#cfn-apigateway-method-integration-integrationresponse-statuscode): String
```

## Properties<a name="aws-properties-apitgateway-method-integration-integrationresponse-properties"></a>

`ContentHandling`  <a name="cfn-apigateway-method-integrationresponse-contenthandling"></a>
Specifies how to handle request payload content type conversions\. Valid values are:  
+ `CONVERT_TO_BINARY`: Converts a request payload from a base64\-encoded string to a binary blob\.
+ `CONVERT_TO_TEXT`: Converts a request payload from a binary blob to a base64\-encoded string\.
If this property isn't defined, the request payload is passed through from the method request to the integration request without modification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseParameters`  <a name="cfn-apigateway-method-integration-integrationresponse-responseparameters"></a>
The response parameters from the backend response that API Gateway sends to the method response\. Specify response parameters as key\-value pairs \([string\-to\-string mappings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html)\)\.  
Use the destination as the key and the source as the value:  
+ The destination must be an existing response parameter in the [MethodResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apitgateway-method-methodresponse.html) property\.
+ The source must be an existing method request parameter or a static value\. You must enclose static values in single quotation marks and pre\-encode these values based on the destination specified in the request\.
For more information about templates, see [API Gateway Mapping Template and Access Logging Variable Reference](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseTemplates`  <a name="cfn-apigateway-method-integration-integrationresponse-responsetemplates"></a>
The templates that are used to transform the integration response body\. Specify templates as key\-value pairs \(string\-to\-string mappings\), with a content type as the key and a template as the value\. For more information, see [API Gateway Mapping Template and Access Logging Variable Reference](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectionPattern`  <a name="cfn-apigateway-method-integration-integrationresponse-selectionpattern"></a>
A [regular expression](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-regexes.html) that specifies which error strings or status codes from the backend map to the integration response\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusCode`  <a name="cfn-apigateway-method-integration-integrationresponse-statuscode"></a>
The status code that API Gateway uses to map the integration response to a [MethodResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apitgateway-method-methodresponse.html) status code\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apitgateway-method-integration-integrationresponse--seealso"></a>
+ [Method](https://docs.aws.amazon.com/apigateway/api-reference/resource/method/) in the *Amazon API Gateway REST API Reference*

