# AWS::ApiGatewayV2::Integration ResponseParameter<a name="aws-properties-apigatewayv2-integration-responseparameter"></a>

Supported only for HTTP APIs\. You use response parameters to transform the HTTP response from a backend integration before returning the response to clients\. Specify a key\-value map from a selection key to response parameters\. The selection key must be a valid HTTP status code within the range of 200\-599\. Response parameters are a key\-value map\. The key must match the pattern `<action>:<header>.<location>` or `overwrite.statuscode`\. The action can be `append`, `overwrite` or `remove`\. The value can be a static value, or map to response data, stage variables, or context variables that are evaluated at runtime\. To learn more, see [Transforming API requests and responses](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-parameter-mapping.html)\. 

## Syntax<a name="aws-properties-apigatewayv2-integration-responseparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-integration-responseparameter-syntax.json"></a>

```
{
  "[Destination](#cfn-apigatewayv2-integration-responseparameter-destination)" : String,
  "[Source](#cfn-apigatewayv2-integration-responseparameter-source)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-integration-responseparameter-syntax.yaml"></a>

```
  [Destination](#cfn-apigatewayv2-integration-responseparameter-destination): String
  [Source](#cfn-apigatewayv2-integration-responseparameter-source): String
```

## Properties<a name="aws-properties-apigatewayv2-integration-responseparameter-properties"></a>

`Destination`  <a name="cfn-apigatewayv2-integration-responseparameter-destination"></a>
Specifies the location of the response to modify, and how to modify it\. To learn more, see [Transforming API requests and responses](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-parameter-mapping.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-apigatewayv2-integration-responseparameter-source"></a>
Specifies the data to update the parameter with\. To learn more, see [Transforming API requests and responses](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-parameter-mapping.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)