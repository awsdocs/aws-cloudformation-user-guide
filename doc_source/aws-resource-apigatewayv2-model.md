# AWS::ApiGatewayV2::Model<a name="aws-resource-apigatewayv2-model"></a>

The `AWS::ApiGatewayV2::Model` resource updates data model for a WebSocket API\. For more information, see [Model Selection Expressions](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-selection-expressions.html#apigateway-websocket-api-model-selection-expressions) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-model-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-model-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Model",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-model-apiid)" : String,
      "[ContentType](#cfn-apigatewayv2-model-contenttype)" : String,
      "[Description](#cfn-apigatewayv2-model-description)" : String,
      "[Name](#cfn-apigatewayv2-model-name)" : String,
      "[Schema](#cfn-apigatewayv2-model-schema)" : Json
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-model-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Model
Properties: 
  [ApiId](#cfn-apigatewayv2-model-apiid): String
  [ContentType](#cfn-apigatewayv2-model-contenttype): String
  [Description](#cfn-apigatewayv2-model-description): String
  [Name](#cfn-apigatewayv2-model-name): String
  [Schema](#cfn-apigatewayv2-model-schema): Json
```

## Properties<a name="aws-resource-apigatewayv2-model-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-model-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContentType`  <a name="cfn-apigatewayv2-model-contenttype"></a>
The content\-type for the model, for example, "application/json"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-model-description"></a>
The description of the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigatewayv2-model-name"></a>
The name of the model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schema`  <a name="cfn-apigatewayv2-model-schema"></a>
The schema for the model\. For application/json models, this should be JSON schema draft 4 model\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-model-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-model-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the model ID, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-model--examples"></a>



### Model creation example<a name="aws-resource-apigatewayv2-model--examples--Model_creation_example"></a>

The following example creates a `model` resource called `MyModel` for an API called `MyApi`\.

#### JSON<a name="aws-resource-apigatewayv2-model--examples--Model_creation_example--json"></a>

```
{
    "MyModel": {
        "Type": "AWS::ApiGatewayV2::Model",
        "Properties": {
            "Name": "ModelName",
            "ApiId": {
                "Ref": "MyApi"
            },
            "ContentType": "application/json",
            "Schema": {
                "$schema": "http://json-schema.org/draft-04/schema#",
                "title": "DummySchema",
                "type": "object",
                "properties": {
                    "id": {
                        "type": "string"
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-model--examples--Model_creation_example--yaml"></a>

```
MyModel:
  Type: 'AWS::ApiGatewayV2::Model'
  Properties:
    Name: ModelName
    ApiId: !Ref MyApi
    ContentType: application/json
    Schema:
      $schema: 'http://json-schema.org/draft-04/schema#'
      title: DummySchema
      type: object
      properties:
        id:
          type: string
```

## See also<a name="aws-resource-apigatewayv2-model--seealso"></a>
+ [CreateModel](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-models.html#CreateModel) in the *Amazon API Gateway Version 2 API Reference*

