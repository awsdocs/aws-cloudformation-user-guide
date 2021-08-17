# AWS::ApiGatewayV2::Integration ResponseParameterList<a name="aws-properties-apigatewayv2-integration-responseparameterlist"></a>

Specifies a list of response parameters for an HTTP API\.

## Syntax<a name="aws-properties-apigatewayv2-integration-responseparameterlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-integration-responseparameterlist-syntax.json"></a>

```
{
  "[ResponseParameters](#cfn-apigatewayv2-integration-responseparameterlist-responseparameters)" : [ ResponseParameter, ... ]
}
```

### YAML<a name="aws-properties-apigatewayv2-integration-responseparameterlist-syntax.yaml"></a>

```
  [ResponseParameters](#cfn-apigatewayv2-integration-responseparameterlist-responseparameters): 
    - ResponseParameter
```

## Properties<a name="aws-properties-apigatewayv2-integration-responseparameterlist-properties"></a>

`ResponseParameters`  <a name="cfn-apigatewayv2-integration-responseparameterlist-responseparameters"></a>
Supported only for HTTP APIs\. You use response parameters to transform the HTTP response from a backend integration before returning the response to clients\. Specify a key\-value map from a selection key to response parameters\. The selection key must be a valid HTTP status code within the range of 200\-599\. Response parameters are a key\-value map\. The key must match the pattern `<action>:<header>.<location>` or `overwrite.statuscode`\. The action can be `append`, `overwrite` or `remove`\. The value can be a static value, or map to response data, stage variables, or context variables that are evaluated at runtime\. To learn more, see [Transforming API requests and responses](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-parameter-mapping.html)\.   
*Required*: No  
*Type*: List of [ResponseParameter](aws-properties-apigatewayv2-integration-responseparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)