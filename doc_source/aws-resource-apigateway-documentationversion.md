# AWS::ApiGateway::DocumentationVersion<a name="aws-resource-apigateway-documentationversion"></a>

The `AWS::ApiGateway::DocumentationVersion` resource creates a snapshot of the documentation for an API\. For more information, see [Representation of API Documentation in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-documenting-api-content-representation.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigateway-documentationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-documentationversion-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::DocumentationVersion",
  "Properties" : {
      "[Description](#cfn-apigateway-documentationversion-description)" : String,
      "[DocumentationVersion](#cfn-apigateway-documentationversion-documentationversion)" : String,
      "[RestApiId](#cfn-apigateway-documentationversion-restapiid)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-documentationversion-syntax.yaml"></a>

```
Type: AWS::ApiGateway::DocumentationVersion
Properties: 
  [Description](#cfn-apigateway-documentationversion-description): String
  [DocumentationVersion](#cfn-apigateway-documentationversion-documentationversion): String
  [RestApiId](#cfn-apigateway-documentationversion-restapiid): String
```

## Properties<a name="aws-resource-apigateway-documentationversion-properties"></a>

`Description`  <a name="cfn-apigateway-documentationversion-description"></a>
The description of the API documentation snapshot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentationVersion`  <a name="cfn-apigateway-documentationversion-documentationversion"></a>
The version identifier of the API documentation snapshot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-documentationversion-restapiid"></a>
The identifier of the API\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-apigateway-documentationversion--examples"></a>



### Associate documentation version with stage<a name="aws-resource-apigateway-documentationversion--examples--Associate_documentation_version_with_stage"></a>

The following example associates a documentation version with an API stage\.

#### JSON<a name="aws-resource-apigateway-documentationversion--examples--Associate_documentation_version_with_stage--json"></a>

```
{
    "Parameters": {
        "apiName": {
            "Type": "String"
        },
        "description": {
            "Type": "String"
        },
        "property": {
            "Type": "String"
        },
        "stageName": {
            "Type": "String"
        },
        "type": {
            "Type": "String"
        },
        "version": {
            "Type": "String"
        }
    },
    "Resources": {
        "Deployment": {
            "Type": "AWS::ApiGateway::Deployment",
            "Properties": {
                "RestApiId": {
                    "Ref": "RestApi"
                }
            },
            "DependsOn": [
                "Method"
            ]
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
        },
        "Method": {
            "Type": "AWS::ApiGateway::Method",
            "Properties": {
                "AuthorizationType": "NONE",
                "HttpMethod": "POST",
                "ResourceId": {
                    "Fn::GetAtt": [
                        "RestApi",
                        "RootResourceId"
                    ]
                },
                "RestApiId": {
                    "Ref": "RestApi"
                },
                "Integration": {
                    "Type": "MOCK"
                }
            }
        },
        "RestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Name": {
                    "Ref": "apiName"
                }
            }
        },
        "Stage": {
            "Type": "AWS::ApiGateway::Stage",
            "Properties": {
                "DeploymentId": {
                    "Ref": "Deployment"
                },
                "DocumentationVersion": {
                    "Ref": "version"
                },
                "RestApiId": {
                    "Ref": "RestApi"
                },
                "StageName": {
                    "Ref": "stageName"
                }
            },
            "DependsOn": "DocumentationVersion"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-documentationversion--examples--Associate_documentation_version_with_stage--yaml"></a>

```
Parameters:
  apiName:
    Type: String
  description:
    Type: String
  property:
    Type: String
  stageName:
    Type: String
  type:
    Type: String
  version:
    Type: String
Resources:
  Deployment:
    Type: AWS::ApiGateway::Deployment
    Properties:
      RestApiId: !Ref RestApi
    DependsOn:
      - Method
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
  Method:
    Type: AWS::ApiGateway::Method
    Properties:
      AuthorizationType: NONE
      HttpMethod: POST
      ResourceId: !GetAtt 
        - RestApi
        - RootResourceId
      RestApiId: !Ref RestApi
      Integration:
        Type: MOCK
  RestApi:
    Type: AWS::ApiGateway::RestApi
    Properties:
      Name: !Ref apiName
  Stage:
    Type: AWS::ApiGateway::Stage
    Properties:
      DeploymentId: !Ref Deployment
      DocumentationVersion: !Ref version
      RestApiId: !Ref RestApi
      StageName: !Ref stageName
    DependsOn: DocumentationVersion
```

## See also<a name="aws-resource-apigateway-documentationversion--seealso"></a>
+ [documentationpart:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/documentationpart-create/) in the *Amazon API Gateway REST API Reference*

