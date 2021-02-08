# AWS::ApiGateway::Model<a name="aws-resource-apigateway-model"></a>

The `AWS::ApiGateway::Model` resource defines the structure of a request or response payload for an API method\.

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
      "[Schema](#cfn-apigateway-model-schema)" : Json
    }
}
```

### YAML<a name="aws-resource-apigateway-model-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Model
Properties: 
  [ContentType](#cfn-apigateway-model-contenttype): String
  [Description](#cfn-apigateway-model-description): String
  [Name](#cfn-apigateway-model-name): String
  [RestApiId](#cfn-apigateway-model-restapiid): String
  [Schema](#cfn-apigateway-model-schema): Json
```

## Properties<a name="aws-resource-apigateway-model-properties"></a>

`ContentType`  <a name="cfn-apigateway-model-contenttype"></a>
The content type for the model\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-apigateway-model-description"></a>
A description that identifies this model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigateway-model-name"></a>
A name for the model\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the model name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-model-restapiid"></a>
The ID of a REST API with which to associate this model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Schema`  <a name="cfn-apigateway-model-schema"></a>
The schema to use to transform data to one or more output formats\. Specify null \(`{}`\) if you don't want to specify a schema\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-model-return-values"></a>

### Ref<a name="aws-resource-apigateway-model-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the model name, such as `myModel`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-model--examples"></a>



### Create model<a name="aws-resource-apigateway-model--examples--Create_model"></a>

The following example creates a model that transforms input data into the described schema\.

#### JSON<a name="aws-resource-apigateway-model--examples--Create_model--json"></a>

```
{
    "PetsModelNoFlatten": {
        "Type": "AWS::ApiGateway::Model",
        "Properties": {
            "RestApiId": {
                "Ref": "RestApi"
            },
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
                        "number": {
                            "type": "integer"
                        },
                        "class": {
                            "type": "string"
                        },
                        "salesPrice": {
                            "type": "number"
                        }
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-model--examples--Create_model--yaml"></a>

```
PetsModelNoFlatten:
  Type: 'AWS::ApiGateway::Model'
  Properties:
    RestApiId: !Ref RestApi
    ContentType: application/json
    Description: Schema for Pets example
    Name: PetsModelNoFlatten
    Schema:
      $schema: 'http://json-schema.org/draft-04/schema#'
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

## See also<a name="aws-resource-apigateway-model--seealso"></a>
+ [model:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/model-create/) in the *Amazon API Gateway REST API Reference*

