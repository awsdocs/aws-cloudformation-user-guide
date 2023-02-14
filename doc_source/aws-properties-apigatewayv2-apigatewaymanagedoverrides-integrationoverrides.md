# AWS::ApiGatewayV2::ApiGatewayManagedOverrides IntegrationOverrides<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides"></a>

The `IntegrationOverrides` property overrides the integration settings for an API Gateway\-managed integration\. If you remove this property, API Gateway restores the default values\.

## Syntax<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-syntax.json"></a>

```
{
  "[Description](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-description)" : String,
  "[IntegrationMethod](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-integrationmethod)" : String,
  "[PayloadFormatVersion](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-payloadformatversion)" : String,
  "[TimeoutInMillis](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-timeoutinmillis)" : Integer
}
```

### YAML<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-syntax.yaml"></a>

```
  [Description](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-description): String
  [IntegrationMethod](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-integrationmethod): String
  [PayloadFormatVersion](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-payloadformatversion): String
  [TimeoutInMillis](#cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-timeoutinmillis): Integer
```

## Properties<a name="aws-properties-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-properties"></a>

`Description`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-description"></a>
The description of the integration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationMethod`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-integrationmethod"></a>
Specifies the integration's HTTP method type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadFormatVersion`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-payloadformatversion"></a>
Specifies the format of the payload sent to an integration\. Required for HTTP APIs\. For HTTP APIs, supported values for Lambda proxy integrations are `1.0` and `2.0`\. For all other integrations, `1.0` is the only supported value\. To learn more, see [Working with AWS Lambda proxy integrations for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInMillis`  <a name="cfn-apigatewayv2-apigatewaymanagedoverrides-integrationoverrides-timeoutinmillis"></a>
Custom timeout between 50 and 29,000 milliseconds for WebSocket APIs and between 50 and 30,000 milliseconds for HTTP APIs\. The default timeout is 29 seconds for WebSocket APIs and 30 seconds for HTTP APIs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)