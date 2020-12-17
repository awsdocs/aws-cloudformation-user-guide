# AWS::ApiGateway::DocumentationPart<a name="aws-resource-apigateway-documentationpart"></a>

The `AWS::ApiGateway::DocumentationPart` resource creates a documentation part for an API\. For more information, see [Representation of API Documentation in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-documenting-api-content-representation.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigateway-documentationpart-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-documentationpart-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::DocumentationPart",
  "Properties" : {
      "[Location](#cfn-apigateway-documentationpart-location)" : Location,
      "[Properties](#cfn-apigateway-documentationpart-properties)" : String,
      "[RestApiId](#cfn-apigateway-documentationpart-restapiid)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-documentationpart-syntax.yaml"></a>

```
Type: AWS::ApiGateway::DocumentationPart
Properties: 
  [Location](#cfn-apigateway-documentationpart-location): 
    Location
  [Properties](#cfn-apigateway-documentationpart-properties): String
  [RestApiId](#cfn-apigateway-documentationpart-restapiid): String
```

## Properties<a name="aws-resource-apigateway-documentationpart-properties"></a>

`Location`  <a name="cfn-apigateway-documentationpart-location"></a>
The location of the API entity that the documentation applies to\.  
*Required*: Yes  
*Type*: [Location](aws-properties-apigateway-documentationpart-location.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Properties`  <a name="cfn-apigateway-documentationpart-properties"></a>
The documentation content map of the targeted API entity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-documentationpart-restapiid"></a>
The identifier of the targeted API entity\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apigateway-documentationpart-return-values"></a>

### Ref<a name="aws-resource-apigateway-documentationpart-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the documentation part, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-documentationpart--examples"></a>



### Associate documentation part with documentation version<a name="aws-resource-apigateway-documentationpart--examples--Associate_documentation_part_with_documentation_version"></a>

The following example associates a documentation part for an API entity with a documentation version\.

#### JSON<a name="aws-resource-apigateway-documentationpart--examples--Associate_documentation_part_with_documentation_version--json"></a>

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

#### YAML<a name="aws-resource-apigateway-documentationpart--examples--Associate_documentation_part_with_documentation_version--yaml"></a>

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
    Type: AWS::ApiGateway::RestApi
    Properties:
      Name: !Ref apiName
  DocumentationPart:
    Type: AWS::ApiGateway::DocumentationPart
    Properties:
      Location:
        Type: !Ref type
      RestApiId: !Ref RestApi
      Property: !Ref property
  DocumentationVersion:
    Type: AWS::ApiGateway::DocumentationVersion
    Properties:
      Description: !Ref description
      DocumentationVersion: !Ref version
      RestApiId: !Ref RestApi
    DependsOn: DocumentationPart
```

## See also<a name="aws-resource-apigateway-documentationpart--seealso"></a>
+ [documentationpart:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/documentationpart-create/) in the *Amazon API Gateway REST API Reference*

