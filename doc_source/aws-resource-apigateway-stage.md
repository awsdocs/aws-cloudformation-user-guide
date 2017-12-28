# AWS::ApiGateway::Stage<a name="aws-resource-apigateway-stage"></a>

The `AWS::ApiGateway::Stage` resource creates a stage for an Amazon API Gateway \(API Gateway\) deployment\.


+ [Syntax](#aws-resource-apigateway-stage-syntax)
+ [Properties](#w3ab2c21c10c81b9)
+ [Return Value](#w3ab2c21c10c81c11)
+ [Example](#aws-resource-apigateway-stage-examples)

## Syntax<a name="aws-resource-apigateway-stage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-stage-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Stage",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-cacheclusterenabled)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-cacheclustersize)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-clientcertificateid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-deploymentid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-documentationversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsettings)" : [ MethodSetting, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-restapiid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-stagename)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-variables)" : { String:String, ... }
  }
}
```

### YAML<a name="aws-resource-apigateway-stage-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Stage"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-cacheclusterenabled): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-cacheclustersize): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-clientcertificateid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-deploymentid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-documentationversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-methodsettings):
    - MethodSetting
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-restapiid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-stagename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-stage-variables):
    String: String
```

## Properties<a name="w3ab2c21c10c81b9"></a>

`CacheClusterEnabled`  
Indicates whether cache clustering is enabled for the stage\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`CacheClusterSize`  
The stage's cache cluster size\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`ClientCertificateId`  
The identifier of the client certificate that API Gateway uses to call your integration endpoints in the stage\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DeploymentId`  
The ID of the deployment that the stage points to\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Description`  
A description of the stage's purpose\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DocumentationVersion`  
The version identifier of the API documentation snapshot\.  
*Required: *No  
*Type*: String

`MethodSettings`  
Settings for all methods in the stage\.  
*Required: *No  
*Type*: List of [API Gateway Stage MethodSetting](aws-properties-apigateway-stage-methodsetting.md)  
*Update requires*: No interruption

`RestApiId`  
The ID of the `RestApi` resource that you're deploying with this stage\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`StageName`  
The name of the stage, which API Gateway uses as the first path segment in the invoked Uniform Resource Identifier \(URI\)\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Variables`  
A map \(string\-to\-string map\) that defines the stage variables, where the variable name is the key and the variable value is the value\. Variable names are limited to alphanumeric characters\. Values must match the following regular expression: `[A-Za-z0-9-._~:/?#&amp;=,]+`\.  
*Required: *No  
*Type*: Mapping of key\-value pairs  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10c81c11"></a>

### Ref<a name="w3ab2c21c10c81c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the name of the stage, such as `MyTestStage`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="aws-resource-apigateway-stage-examples"></a>

The following example creates a stage for the `TestDeployment` deployment\. The stage also specifies method settings for the `MyRestApi` API\.

### JSON<a name="aws-resource-apigateway-stage-example.json"></a>

```
{
    "Resources": {
        "Prod": {
            "Type": "AWS::ApiGateway::Stage",
            "Properties": {
                "StageName": "Prod",
                "Description": "Prod Stage",
                "RestApiId": {
                    "Ref": "MyRestApi"
                },
                "DeploymentId": {
                    "Ref": "TestDeployment"
                },
                "DocumentationVersion": {
                    "Ref": "MyDocumentationVersion"
                },
                "ClientCertificateId": {
                    "Ref": "ClientCertificate"
                },
                "Variables": {
                    "Stack": "Prod"
                },
                "MethodSettings": [
                    {
                        "ResourcePath": "/",
                        "HttpMethod": "GET",
                        "MetricsEnabled": "true",
                        "DataTraceEnabled": "true"
                    },
                    {
                        "ResourcePath": "/stack",
                        "HttpMethod": "POST",
                        "MetricsEnabled": "true",
                        "DataTraceEnabled": "true",
                        "ThrottlingBurstLimit": "999"
                    },
                    {
                        "ResourcePath": "/stack",
                        "HttpMethod": "GET",
                        "MetricsEnabled": "true",
                        "DataTraceEnabled": "true",
                        "ThrottlingBurstLimit": "555"
                    }
                ]
            }
        }
    }
}
```

### YAML<a name="aws-resource-apigateway-stage-example.yaml"></a>

```
Resources:
  Prod:
    Type: 'AWS::ApiGateway::Stage'
    Properties:
      StageName: Prod
      Description: Prod Stage
      RestApiId: !Ref MyRestApi
      DeploymentId: !Ref TestDeployment
      DocumentationVersion: !Ref MyDocumentationVersion
      ClientCertificateId: !Ref ClientCertificate
      Variables:
        Stack: Prod
      MethodSettings:
        - ResourcePath: /
          HttpMethod: GET
          MetricsEnabled: 'true'
          DataTraceEnabled: 'true'
        - ResourcePath: /stack
          HttpMethod: POST
          MetricsEnabled: 'true'
          DataTraceEnabled: 'true'
          ThrottlingBurstLimit: '999'
        - ResourcePath: /stack
          HttpMethod: GET
          MetricsEnabled: 'true'
          DataTraceEnabled: 'true'
          ThrottlingBurstLimit: '555'
```