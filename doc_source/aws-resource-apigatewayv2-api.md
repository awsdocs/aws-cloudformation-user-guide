# AWS::ApiGatewayV2::Api<a name="aws-resource-apigatewayv2-api"></a>

The `AWS::ApiGatewayV2::Api` resource contains an Amazon API Gateway API\. For more information, see [CreateApi](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis.html#CreateApi) in the *Amazon API Gateway V2 API Reference*\. 

## Syntax<a name="aws-resource-apigatewayv2-api-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-api-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Api",
  "Properties" : {
    
    "[ApiKeySelectionExpression](#cfn-apigatewayv2-api-apikeyselectionexpression)" : String,
    "[Description](#cfn-apigatewayv2-api-description)" : String,
    "[DisableSchemaValidation](#cfn-apigatewayv2-api-disableschemavalidation)" : Boolean,
    "[Name](#cfn-apigatewayv2-api-name)" : String,
    "[ProtocolType](#cfn-apigatewayv2-api-protocoltype)" : String,
    "[RouteSelectionExpression](#cfn-apigatewayv2-api-routeselectionexpression)" : String,
    "[Version](#cfn-apigatewayv2-api-version)" : String
  }
}
```

### YAML<a name="aws-resource-apigatewayv2-api-syntax.yaml"></a>

```
Type: "AWS::ApiGatewayV2::Api"
Properties:
  [ApiKeySelectionExpression](#cfn-apigatewayv2-api-apikeyselectionexpression): String
  [Description](#cfn-apigatewayv2-api-description): String
  [DisableSchemaValidation](#cfn-apigatewayv2-api-disableschemavalidation): Boolean
  [Name](#cfn-apigatewayv2-api-name): String
  [ProtocolType](#cfn-apigatewayv2-api-protocoltype): String
  [RouteSelectionExpression](#cfn-apigatewayv2-api-routeselectionexpression): String
  [Version](#cfn-apigatewayv2-api-version): String
```

## Properties<a name="aws-resource-apigatewayv2-api-properties"></a>

`ApiKeySelectionExpression`  <a name="cfn-apigatewayv2-api-apikeyselectionexpression"></a>
An API key selection expression\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-apigatewayv2-api-description"></a>
The description of the API\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisableSchemaValidation`  <a name="cfn-apigatewayv2-api-disableschemavalidation"></a>
Avoid validating models when creating a deployment\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-apigatewayv2-api-name"></a>
The name of the API\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProtocolType`  <a name="cfn-apigatewayv2-api-protocoltype"></a>
The API protocol\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RouteSelectionExpression`  <a name="cfn-apigatewayv2-api-routeselectionexpression"></a>
The route selection expression for the API\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-apigatewayv2-api-version"></a>
A version identifier for the API\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-api-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-api-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::Api` resource to the intrinsic `Ref` function, the function returns the API ID, such as `a1bcdef2gh`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-api-examples"></a>

### API creation example<a name="aws-resource-apigatewayv2-api-example1"></a>

The following example creates an `Api` resource called `MyApi`\.

#### JSON<a name="aws-resource-apigatewayv2-api-example1.json"></a>

```
{
    "MyApi": {
      "Type": "AWS::ApiGatewayV2::Api",
      "Properties": {
        "Name": "MyApi",
        "ProtocolType": "WEBSOCKET",
        "RouteSelectionExpression": "$request.body.action",
        "ApiKeySelectionExpression": "$request.header.x-api-key"
      }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-api-example1.yaml"></a>

```
MyApi:
  Type: 'AWS::ApiGatewayV2::Api'
  Properties:
    Name: MyApi
    ProtocolType: WEBSOCKET
    RouteSelectionExpression: $request.body.action
    ApiKeySelectionExpression: $request.header.x-api-key
```

## See Also<a name="aws-resource-apigatewayv2-api-seealso"></a>
+  [CreateApi](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis.html#CreateApi) in the *Amazon API Gateway V2 API Reference* 