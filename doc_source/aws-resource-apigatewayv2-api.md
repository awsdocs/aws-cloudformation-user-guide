# AWS::ApiGatewayV2::Api<a name="aws-resource-apigatewayv2-api"></a>

The `AWS::ApiGatewayV2::Api` resource creates an API\. Currently only WebSocket APIs are supported\. For more information about WebSocket APIs, see [About WebSocket APIs in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-overview.html) in the *API Gateway Developer Guide*\.

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
Type: AWS::ApiGatewayV2::Api
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
An API key selection expression\. See [API Key Selection Expressions](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-selection-expressions.html#apigateway-websocket-api-apikey-selection-expressions)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-api-description"></a>
The description of the API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableSchemaValidation`  <a name="cfn-apigatewayv2-api-disableschemavalidation"></a>
Avoid validating models when creating a deployment\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigatewayv2-api-name"></a>
The name of the API\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtocolType`  <a name="cfn-apigatewayv2-api-protocoltype"></a>
The API protocol: Currently only `WEBSOCKET` is supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteSelectionExpression`  <a name="cfn-apigatewayv2-api-routeselectionexpression"></a>
The route selection expression for the API\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-apigatewayv2-api-version"></a>
A version identifier for the API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-apigatewayv2-api-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-api-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the API ID, such as `a1bcdef2gh`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-api--examples"></a>

### API creation example<a name="aws-resource-apigatewayv2-api--examples--API_creation_example"></a>

The following example creates an `Api` resource called `MyApi`\.

#### JSON<a name="aws-resource-apigatewayv2-api--examples--API_creation_example--json"></a>

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

#### YAML<a name="aws-resource-apigatewayv2-api--examples--API_creation_example--yaml"></a>

```
MyApi:
  Type: 'AWS::ApiGatewayV2::Api'
  Properties:
    Name: MyApi
    ProtocolType: WEBSOCKET
    RouteSelectionExpression: $request.body.action
    ApiKeySelectionExpression: $request.header.x-api-key
```

## See Also<a name="aws-resource-apigatewayv2-api--seealso"></a>
+ [CreateApi](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis.html#CreateApi) in the *Amazon API Gateway Version 2 API Reference*

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
