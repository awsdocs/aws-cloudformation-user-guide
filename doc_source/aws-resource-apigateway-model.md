# AWS::ApiGateway::Model<a name="aws-resource-apigateway-model"></a>

The `AWS::ApiGateway::Model` resource defines the structure of a request or response payload for an Amazon API Gateway \(API Gateway\) method\.

**Topics**
+ [Syntax](#aws-resource-apigateway-model-syntax)
+ [Properties](#aws-resource-apigateway-model-props)
+ [Return Value](#aws-resource-apigateway-model-return-value)
+ [Example](#aws-resource-apigateway-model-example)

## Syntax<a name="aws-resource-apigateway-model-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-model-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Model",
  "Properties" : {
    "[ContentType](#cfn-apigateway-model-contenttype)" : String,
    "[Description](#cfn-apigateway-model-description)" : String,
    "[Name](#cfn-apigateway-model-name)" : String,
    "[RestApiId](#cfn-apigateway-model-restapiid)" : String,
    "[Schema](#cfn-apigateway-model-schema)" : JSON object
  }
}
```

### YAML<a name="aws-resource-apigateway-model-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Model"
Properties:
  [ContentType](#cfn-apigateway-model-contenttype): String
  [Description](#cfn-apigateway-model-description): String
  [Name](#cfn-apigateway-model-name): String
  [RestApiId](#cfn-apigateway-model-restapiid): String
  [Schema](#cfn-apigateway-model-schema): JSON object
```

## Properties<a name="aws-resource-apigateway-model-props"></a>

`ContentType`  <a name="cfn-apigateway-model-contenttype"></a>
The content type for the model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-apigateway-model-description"></a>
A description that identifies this model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-apigateway-model-name"></a>
A name for the model\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the model name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RestApiId`  <a name="cfn-apigateway-model-restapiid"></a>
The ID of a REST API with which to associate this model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Schema`  <a name="cfn-apigateway-model-schema"></a>
The schema to use to transform data to one or more output formats\. Specify null \(`{}`\) if you don't want to specify a schema\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-apigateway-model-return-value"></a>

### Ref<a name="aws-resource-apigateway-model-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the model name, such as `myModel`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-apigateway-model-example"></a>

The following example creates a model that transforms input data into the described schema\.

### JSON<a name="aws-resource-apigateway-model-example.json"></a>

```
"PetsModelNoFlatten": {
  "Type": "AWS::ApiGateway::Model",
  "Properties": {
    "RestApiId": { "Ref": "RestApi" },
    "ContentType": "application/json",
    "Description": "Schema for Pets example",
    "Name": "PetsModelNoFlatten",
    "Schema": {
      "$schema": "http://json-schema.org/draft-04/schema#",
      "title": "PetsModelNoFlatten",
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "number": { "type": "integer" },
          "class": { "type": "string" },
          "salesPrice": { "type": "number" }
        }
      }
    }
  }
}
```

### YAML<a name="aws-resource-apigateway-model-example.yaml"></a>

```
PetsModelNoFlatten: 
  Type: "AWS::ApiGateway::Model"
  Properties: 
    RestApiId: 
      Ref: RestApi
    ContentType: "application/json"
    Description: "Schema for Pets example"
    Name: PetsModelNoFlatten
    Schema: 
      "$schema": "http://json-schema.org/draft-04/schema#" 
      title: PetsModelNoFlatten
      type: array
      items: 
        type: object
        properties: 
          number: 
            type: integer
          class: 
            type: string
          salesPrice: 
            type: number
```