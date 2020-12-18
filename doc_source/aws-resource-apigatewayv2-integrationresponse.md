# AWS::ApiGatewayV2::IntegrationResponse<a name="aws-resource-apigatewayv2-integrationresponse"></a>

The `AWS::ApiGatewayV2::IntegrationResponse` resource updates an integration response for an WebSocket API\. For more information, see [Set up WebSocket API Integration Responses in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-integration-responses.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-integrationresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-integrationresponse-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::IntegrationResponse",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-integrationresponse-apiid)" : String,
      "[ContentHandlingStrategy](#cfn-apigatewayv2-integrationresponse-contenthandlingstrategy)" : String,
      "[IntegrationId](#cfn-apigatewayv2-integrationresponse-integrationid)" : String,
      "[IntegrationResponseKey](#cfn-apigatewayv2-integrationresponse-integrationresponsekey)" : String,
      "[ResponseParameters](#cfn-apigatewayv2-integrationresponse-responseparameters)" : Json,
      "[ResponseTemplates](#cfn-apigatewayv2-integrationresponse-responsetemplates)" : Json,
      "[TemplateSelectionExpression](#cfn-apigatewayv2-integrationresponse-templateselectionexpression)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-integrationresponse-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::IntegrationResponse
Properties: 
  [ApiId](#cfn-apigatewayv2-integrationresponse-apiid): String
  [ContentHandlingStrategy](#cfn-apigatewayv2-integrationresponse-contenthandlingstrategy): String
  [IntegrationId](#cfn-apigatewayv2-integrationresponse-integrationid): String
  [IntegrationResponseKey](#cfn-apigatewayv2-integrationresponse-integrationresponsekey): String
  [ResponseParameters](#cfn-apigatewayv2-integrationresponse-responseparameters): Json
  [ResponseTemplates](#cfn-apigatewayv2-integrationresponse-responsetemplates): Json
  [TemplateSelectionExpression](#cfn-apigatewayv2-integrationresponse-templateselectionexpression): String
```

## Properties<a name="aws-resource-apigatewayv2-integrationresponse-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-integrationresponse-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentHandlingStrategy`  <a name="cfn-apigatewayv2-integrationresponse-contenthandlingstrategy"></a>
Supported only for WebSocket APIs\. Specifies how to handle response payload content type conversions\. Supported values are `CONVERT_TO_BINARY` and `CONVERT_TO_TEXT`, with the following behaviors:  
 `CONVERT_TO_BINARY`: Converts a response payload from a Base64\-encoded string to the corresponding binary blob\.  
 `CONVERT_TO_TEXT`: Converts a response payload from a binary blob to a Base64\-encoded string\.  
If this property is not defined, the response payload will be passed through from the integration response to the route response or method response without modification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationId`  <a name="cfn-apigatewayv2-integrationresponse-integrationid"></a>
The integration ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationResponseKey`  <a name="cfn-apigatewayv2-integrationresponse-integrationresponsekey"></a>
The integration response key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseParameters`  <a name="cfn-apigatewayv2-integrationresponse-responseparameters"></a>
A key\-value map specifying response parameters that are passed to the method response from the backend\. The key is a method response header parameter name and the mapped value is an integration response header value, a static value enclosed within a pair of single quotes, or a JSON expression from the integration response body\. The mapping key must match the pattern of `method.response.header.{name} `, where name is a valid and unique header name\. The mapped non\-static value must match the pattern of `integration.response.header.{name} ` or `integration.response.body.{JSON-expression} `, where ` {name} ` is a valid and unique response header name and ` {JSON-expression} ` is a valid JSON expression without the `$` prefix\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseTemplates`  <a name="cfn-apigatewayv2-integrationresponse-responsetemplates"></a>
The collection of response templates for the integration response as a string\-to\-string map of key\-value pairs\. Response templates are represented as a key/value map, with a content\-type as the key and a template as the value\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateSelectionExpression`  <a name="cfn-apigatewayv2-integrationresponse-templateselectionexpression"></a>
The template selection expression for the integration response\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-integrationresponse-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-integrationresponse-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the integration response resource ID, such as `abcd123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-integrationresponse--examples"></a>



### Integration response creation example<a name="aws-resource-apigatewayv2-integrationresponse--examples--Integration_response_creation_example"></a>

The following example creates an `IntegrationResponse` resource for an API named `MyApi` that has an `integration` resource called `MyIntegration`\.

#### JSON<a name="aws-resource-apigatewayv2-integrationresponse--examples--Integration_response_creation_example--json"></a>

```
{
    "IntegrationResponse": {
        "Type": "AWS::ApiGatewayV2::IntegrationResponse",
        "Properties": {
            "IntegrationId": {
                "Ref": "MyIntegration"
            },
            "IntegrationResponseKey": "/400/",
            "ApiId": {
                "Ref": "MyApi"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-integrationresponse--examples--Integration_response_creation_example--yaml"></a>

```
IntegrationResponse:
  Type: 'AWS::ApiGatewayV2::IntegrationResponse'
  Properties:
    IntegrationId: !Ref MyIntegration
    IntegrationResponseKey: /400/
    ApiId: !Ref MyApi
```

## See also<a name="aws-resource-apigatewayv2-integrationresponse--seealso"></a>
+ [CreateIntegrationResponse](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-integrations-integrationid-integrationresponses.html#CreateIntegrationResponse) in the *Amazon API Gateway Version 2 API Reference*

