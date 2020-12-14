# AWS::ApiGatewayV2::Api Cors<a name="aws-properties-apigatewayv2-api-cors"></a>

The `Cors` property specifies a CORS configuration for an API\. Supported only for HTTP APIs\. See [Configuring CORS](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-cors.html) for more information\.

## Syntax<a name="aws-properties-apigatewayv2-api-cors-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-api-cors-syntax.json"></a>

```
{
  "[AllowCredentials](#cfn-apigatewayv2-api-cors-allowcredentials)" : Boolean,
  "[AllowHeaders](#cfn-apigatewayv2-api-cors-allowheaders)" : [ String, ... ],
  "[AllowMethods](#cfn-apigatewayv2-api-cors-allowmethods)" : [ String, ... ],
  "[AllowOrigins](#cfn-apigatewayv2-api-cors-alloworigins)" : [ String, ... ],
  "[ExposeHeaders](#cfn-apigatewayv2-api-cors-exposeheaders)" : [ String, ... ],
  "[MaxAge](#cfn-apigatewayv2-api-cors-maxage)" : Integer
}
```

### YAML<a name="aws-properties-apigatewayv2-api-cors-syntax.yaml"></a>

```
  [AllowCredentials](#cfn-apigatewayv2-api-cors-allowcredentials): Boolean
  [AllowHeaders](#cfn-apigatewayv2-api-cors-allowheaders): 
    - String
  [AllowMethods](#cfn-apigatewayv2-api-cors-allowmethods): 
    - String
  [AllowOrigins](#cfn-apigatewayv2-api-cors-alloworigins): 
    - String
  [ExposeHeaders](#cfn-apigatewayv2-api-cors-exposeheaders): 
    - String
  [MaxAge](#cfn-apigatewayv2-api-cors-maxage): Integer
```

## Properties<a name="aws-properties-apigatewayv2-api-cors-properties"></a>

`AllowCredentials`  <a name="cfn-apigatewayv2-api-cors-allowcredentials"></a>
Specifies whether credentials are included in the CORS request\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowHeaders`  <a name="cfn-apigatewayv2-api-cors-allowheaders"></a>
Represents a collection of allowed headers\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowMethods`  <a name="cfn-apigatewayv2-api-cors-allowmethods"></a>
Represents a collection of allowed HTTP methods\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowOrigins`  <a name="cfn-apigatewayv2-api-cors-alloworigins"></a>
Represents a collection of allowed origins\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExposeHeaders`  <a name="cfn-apigatewayv2-api-cors-exposeheaders"></a>
Represents a collection of exposed headers\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAge`  <a name="cfn-apigatewayv2-api-cors-maxage"></a>
The number of seconds that the browser should cache preflight request results\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)