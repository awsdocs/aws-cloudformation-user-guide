# AWS::ApiGatewayV2::RouteResponse<a name="aws-resource-apigatewayv2-routeresponse"></a>

The `AWS::ApiGatewayV2::RouteResponse` resource creates a route response for a WebSocket API\. For more information, see [Set up Route Responses for a WebSocket API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-route-response.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-routeresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-routeresponse-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::RouteResponse",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-routeresponse-apiid)" : String,
      "[ModelSelectionExpression](#cfn-apigatewayv2-routeresponse-modelselectionexpression)" : String,
      "[ResponseModels](#cfn-apigatewayv2-routeresponse-responsemodels)" : Json,
      "[ResponseParameters](#cfn-apigatewayv2-routeresponse-responseparameters)" : Json,
      "[RouteId](#cfn-apigatewayv2-routeresponse-routeid)" : String,
      "[RouteResponseKey](#cfn-apigatewayv2-routeresponse-routeresponsekey)" : String
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-routeresponse-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::RouteResponse
Properties: 
  [ApiId](#cfn-apigatewayv2-routeresponse-apiid): String
  [ModelSelectionExpression](#cfn-apigatewayv2-routeresponse-modelselectionexpression): String
  [ResponseModels](#cfn-apigatewayv2-routeresponse-responsemodels): Json
  [ResponseParameters](#cfn-apigatewayv2-routeresponse-responseparameters): Json
  [RouteId](#cfn-apigatewayv2-routeresponse-routeid): String
  [RouteResponseKey](#cfn-apigatewayv2-routeresponse-routeresponsekey): String
```

## Properties<a name="aws-resource-apigatewayv2-routeresponse-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-routeresponse-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelSelectionExpression`  <a name="cfn-apigatewayv2-routeresponse-modelselectionexpression"></a>
The model selection expression for the route response\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseModels`  <a name="cfn-apigatewayv2-routeresponse-responsemodels"></a>
The response models for the route response\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseParameters`  <a name="cfn-apigatewayv2-routeresponse-responseparameters"></a>
The route response parameters\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteId`  <a name="cfn-apigatewayv2-routeresponse-routeid"></a>
The route ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteResponseKey`  <a name="cfn-apigatewayv2-routeresponse-routeresponsekey"></a>
The route response key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-routeresponse-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-routeresponse-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Route Response resource ID, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-routeresponse--examples"></a>



### Route response creation example<a name="aws-resource-apigatewayv2-routeresponse--examples--Route_response_creation_example"></a>

The following example creates a `RouteResponse` resource for a WebSocket API called `MyApi` that already has an `integration` called `MyIntegration` and a `route` called `MyRoute`\.

#### JSON<a name="aws-resource-apigatewayv2-routeresponse--examples--Route_response_creation_example--json"></a>

```
{
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
}
```

#### YAML<a name="aws-resource-apigatewayv2-routeresponse--examples--Route_response_creation_example--yaml"></a>

```
MyRouteResponse:
  Type: 'AWS::ApiGatewayV2::RouteResponse'
  Properties:
    RouteId: !Ref MyRoute
    ApiId: !Ref MyApi
    RouteResponseKey: $default
```

## See also<a name="aws-resource-apigatewayv2-routeresponse--seealso"></a>
+ [CreateRouteResponse](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-routes-routeid-routeresponses.html#CreateRouteResponse) in the *Amazon API Gateway Version 2 API Reference*

