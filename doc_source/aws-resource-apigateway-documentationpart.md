# AWS::ApiGateway::DocumentationPart<a name="aws-resource-apigateway-documentationpart"></a>

The `AWS::ApiGateway::DocumentationPart` resource creates a documentation part for an Amazon API Gateway API entity\. For more information, see [ Representation of API Documentation in API Gateway](http://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-documenting-api-content-representation.html) in the *API Gateway Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-apigateway-documentationpart-syntax)
+ [Properties](#aws-resource-apigateway-documentationpart-properties)
+ [Return Value](#aws-resource-apigateway-documentationpart-returnvalues)
+ [Example](#aws-resource-apigateway-documentationpart-examples)

## Syntax<a name="aws-resource-apigateway-documentationpart-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-documentationpart-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::DocumentationPart",
  "Properties" : {
    "[Location](#cfn-apigateway-documentationpart-location)" : [*Location*](aws-properties-apigateway-documentationpart-location.md),
    "[Properties](#cfn-apigateway-documentationpart-properties)" : String,
    "[RestApiId](#cfn-apigateway-documentationpart-restapiid)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-documentationpart-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::DocumentationPart"
Properties:
  [Location](#cfn-apigateway-documentationpart-location): 
    [*Location*](aws-properties-apigateway-documentationpart-location.md)
  [Properties](#cfn-apigateway-documentationpart-properties): String
  [RestApiId](#cfn-apigateway-documentationpart-restapiid): String
```

## Properties<a name="aws-resource-apigateway-documentationpart-properties"></a>

**Note**  
For more information about each property, including constraints and valid values, see [ DocumentationPart](http://docs.aws.amazon.com/apigateway/api-reference/resource/documentation-part) in the *Amazon API Gateway REST API Reference*\.

`Location`  <a name="cfn-apigateway-documentationpart-location"></a>
The location of the API entity that the documentation applies to\.  
 *Required*: Yes  
 *Type*: [Amazon API Gateway DocumentationPart Location](aws-properties-apigateway-documentationpart-location.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Properties`  <a name="cfn-apigateway-documentationpart-properties"></a>
The documentation content map of the targeted API entity\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RestApiId`  <a name="cfn-apigateway-documentationpart-restapiid"></a>
The identifier of the targeted API entity\.  
 *Required*: Yes  
*Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Value<a name="aws-resource-apigateway-documentationpart-returnvalues"></a>

### Ref<a name="aws-resource-apigateway-documentationpart-ref"></a>

When you pass the logical ID of an `AWS::ApiGateway::DocumentationPart` resource to the intrinsic `Ref` function, the function returns the ID of the documentation part, such as `abc123`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-apigateway-documentationpart-examples"></a>

### <a name="w3ab2c21c10c40c13b3"></a>

The following example associates a documentation part for an API entity with a documentation version\.

#### JSON<a name="aws-resource-apigateway-documentationpart-example1.json"></a>

```
{
    "Parameters": {
        "apiName": {
            "Type": "String"
        },
        "description": {
            "Type": "String"
        },
        "version": {
            "Type": "String"
        },
        "type": {
            "Type": "String"
        },
        "property": {
            "Type": "String"
        }
    },
    "Resources": {
        "RestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Name": {
                    "Ref": "apiName"
                }
            }
        },
        "DocumentationPart": {
            "Type": "AWS::ApiGateway::DocumentationPart",
            "Properties": {
                "Location": {
                    "Type": {
                        "Ref": "type"
                    }
                },
                "RestApiId": {
                    "Ref": "RestApi"
                },
                "Property": {
                    "Ref": "property"
                }
            }
        },
        "DocumentationVersion": {
            "Type": "AWS::ApiGateway::DocumentationVersion",
            "Properties": {
                "Description": {
                    "Ref": "description"
                },
                "DocumentationVersion": {
                    "Ref": "version"
                },
                "RestApiId": {
                    "Ref": "RestApi"
                }
            },
            "DependsOn": "DocumentationPart"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-documentationpart-example1.yaml"></a>

```
Parameters:
  apiName:
    Type: String
  description:
    Type: String
  version:
    Type: String
  type:
    Type: String
  property:
    Type: String
Resources:
  RestApi:
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      Name: !Ref apiName
  DocumentationPart:
    Type: 'AWS::ApiGateway::DocumentationPart'
    Properties:
      Location:
        Type: !Ref type
      RestApiId: !Ref RestApi
      Property: !Ref property
  DocumentationVersion:
    Type: 'AWS::ApiGateway::DocumentationVersion'
    Properties:
      Description: !Ref description
      DocumentationVersion: !Ref version
      RestApiId: !Ref RestApi
    DependsOn: DocumentationPart
```