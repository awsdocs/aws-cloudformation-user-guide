# AWS::ApiGatewayV2::Model<a name="aws-resource-apigatewayv2-model"></a>

The `AWS::ApiGatewayV2::Model` resource define a data model for an API\. For more information, see [CreateModel](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-models.html#CreateModel) in the *Amazon API Gateway V2 API Reference*\. 

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
    "[Schema](#cfn-apigatewayv2-model-schema)" : JSON object
  }
}
```

### YAML<a name="aws-resource-apigatewayv2-model-syntax.yaml"></a>

```
Type: "AWS::ApiGatewayV2::Model"
Properties:
  [ApiId](#cfn-apigatewayv2-model-apiid): String
  [ContentType](#cfn-apigatewayv2-model-contenttype): String
  [Description](#cfn-apigatewayv2-model-description): String
  [Name](#cfn-apigatewayv2-model-name): String
  [Schema](#cfn-apigatewayv2-model-schema): JSON object
```

## Properties<a name="aws-resource-apigatewayv2-model-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-model-apiid"></a>
The ID of the API with which to associate this model\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ContentType`  <a name="cfn-apigatewayv2-model-contenttype"></a>
The content type for the model\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-apigatewayv2-model-description"></a>
A description that identifies this model\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-apigatewayv2-model-name"></a>
A name for the model\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the model name\. For more information, see [Name Type](aws-properties-name.md)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schema`  <a name="cfn-apigatewayv2-model-schema"></a>
The schema to use to transform data to one or more output formats\. Specify null \(`{}`\) if you don't want to specify a schema\.  
 *Required*: Yes  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-model-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-model-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::Model` resource to the intrinsic `Ref` function, the function returns the model ID, such as `abc123`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-model-examples"></a>

### Model creation example<a name="aws-resource-apigatewayv2-model-example1"></a>

The following example creates a `model` resource called `MyModel` for an API called `MyApi`\.

#### JSON<a name="aws-resource-apigatewayv2-model-example1.json"></a>

```
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
```

#### YAML<a name="aws-resource-apigatewayv2-model-example1.yaml"></a>

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

## See Also<a name="aws-resource-apigatewayv2-model-seealso"></a>
+  [CreateModel](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-models.html#CreateModel) in the *Amazon API Gateway V2 API Reference* 