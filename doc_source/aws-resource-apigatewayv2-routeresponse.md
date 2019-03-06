# AWS::ApiGatewayV2::RouteResponse<a name="aws-resource-apigatewayv2-routeresponse"></a>

The `AWS::ApiGatewayV2::RouteResponse` resource defines the route response for a WebSocket API route\. For more information, see [CreateRouteResponse](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-routes-routeid-routeresponses.html#CreateRouteResponse) in the *Amazon API Gateway V2 API Reference*\.

## Syntax<a name="aws-resource-apigatewayv2-routeresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-routeresponse-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::RouteResponse",
  "Properties" : {
    "[ApiId](#cfn-apigatewayv2-routeresponse-apiid)" : String,
    "[ModelSelectionExpression](#cfn-apigatewayv2-routeresponse-modelselectionexpression)" : String,
    "[ResponseModels](#cfn-apigatewayv2-routeresponse-responsemodels)" : JSON object,
    "[ResponseParameters](#cfn-apigatewayv2-routeresponse-responseparameters)" : JSON object,
    "[RouteId](#cfn-apigatewayv2-routeresponse-routeid)" : String,
    "[RouteResponseKey](#cfn-apigatewayv2-routeresponse-routeresponsekey)" : String
  }
}
```

### YAML<a name="aws-resource-apigatewayv2-routeresponse-syntax.yaml"></a>

```
Type: "AWS::ApiGatewayV2::RouteResponse"
Properties:
  [ApiId](#cfn-apigatewayv2-routeresponse-apiid): String
  [ModelSelectionExpression](#cfn-apigatewayv2-routeresponse-modelselectionexpression): String
  [RouteResponseKey](#cfn-apigatewayv2-routeresponse-routeresponsekey): String
  [ResponseModels](#cfn-apigatewayv2-routeresponse-responsemodels): JSON object
  [ResponseParameters](#cfn-apigatewayv2-routeresponse-responseparameters): JSON object
  [RouteId](#cfn-apigatewayv2-routeresponse-routeid): String
```

## Properties<a name="aws-resource-apigatewayv2-routeresponse-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-routeresponse-apiid"></a>
The API ID  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ModelSelectionExpression`  <a name="cfn-apigatewayv2-routeresponse-modelselectionexpression"></a>
The model selection expression for the route response\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseModels`  <a name="cfn-apigatewayv2-routeresponse-responsemodels"></a>
The response models for the route response\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResponseParameters`  <a name="cfn-apigatewayv2-routeresponse-responseparameters"></a>
The route response parameters\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RouteId`  <a name="cfn-apigatewayv2-routeresponse-routeid"></a>
The route ID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RouteResponseKey`  <a name="cfn-apigatewayv2-routeresponse-routeresponsekey"></a>
The route response key\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-routeresponse-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-routeresponse-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::RouteResponse` resource to the intrinsic `Ref` function, the function returns the Route Response resource ID, such as `abc123`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-routeresponse-examples"></a>

### Route response creation example<a name="aws-resource-apigatewayv2-routeresponse-example1"></a>

The following example creates a `RouteResponse` resource for a WebSocket API called `MyApi` that already has an `integration` called `MyIntegration` and a `route` called `MyRoute`\.

#### JSON<a name="aws-resource-apigatewayv2-routeresponse-example1.json"></a>

```
"MyRouteResponse": {
            "Type": "AWS::ApiGatewayV2::RouteResponse",
            "Properties": {
                "RouteId": {
                    "Ref": "MyRoute"
                },
                "ApiId": {
                    "Ref": "MyApi"
                },
                "RouteResponseKey": "$default"
            }
        }
```

#### YAML<a name="aws-resource-apigatewayv2-routeresponse-example1.yaml"></a>

```
MyRouteResponse:
    Type: 'AWS::ApiGatewayV2::RouteResponse'
    Properties:
      RouteId:
        Ref: MyRoute
      ApiId:
        Ref: MyApi
      RouteResponseKey: $default
```

## See Also<a name="aws-resource-apigatewayv2-routeresponse-seealso"></a>
+  [CreateRouteResponse](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-routes-routeid-routeresponses.html#CreateRouteResponse) in the *Amazon API Gateway V2 API Reference* 