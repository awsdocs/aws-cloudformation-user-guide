# AWS::ApiGateway::Stage<a name="aws-resource-apigateway-stage"></a>

The `AWS::ApiGateway::Stage` resource creates a stage for a deployment\.

## Syntax<a name="aws-resource-apigateway-stage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-stage-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Stage",
  "Properties" : {
      "[AccessLogSetting](#cfn-apigateway-stage-accesslogsetting)" : AccessLogSetting,
      "[CacheClusterEnabled](#cfn-apigateway-stage-cacheclusterenabled)" : Boolean,
      "[CacheClusterSize](#cfn-apigateway-stage-cacheclustersize)" : String,
      "[CanarySetting](#cfn-apigateway-stage-canarysetting)" : CanarySetting,
      "[ClientCertificateId](#cfn-apigateway-stage-clientcertificateid)" : String,
      "[DeploymentId](#cfn-apigateway-stage-deploymentid)" : String,
      "[Description](#cfn-apigateway-stage-description)" : String,
      "[DocumentationVersion](#cfn-apigateway-stage-documentationversion)" : String,
      "[MethodSettings](#cfn-apigateway-stage-methodsettings)" : [ MethodSetting, ... ],
      "[RestApiId](#cfn-apigateway-stage-restapiid)" : String,
      "[StageName](#cfn-apigateway-stage-stagename)" : String,
      "[Tags](#cfn-apigateway-stage-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TracingEnabled](#cfn-apigateway-stage-tracingenabled)" : Boolean,
      "[Variables](#cfn-apigateway-stage-variables)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-apigateway-stage-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Stage
Properties: 
  [AccessLogSetting](#cfn-apigateway-stage-accesslogsetting): 
    AccessLogSetting
  [CacheClusterEnabled](#cfn-apigateway-stage-cacheclusterenabled): Boolean
  [CacheClusterSize](#cfn-apigateway-stage-cacheclustersize): String
  [CanarySetting](#cfn-apigateway-stage-canarysetting): 
    CanarySetting
  [ClientCertificateId](#cfn-apigateway-stage-clientcertificateid): String
  [DeploymentId](#cfn-apigateway-stage-deploymentid): String
  [Description](#cfn-apigateway-stage-description): String
  [DocumentationVersion](#cfn-apigateway-stage-documentationversion): String
  [MethodSettings](#cfn-apigateway-stage-methodsettings): 
    - MethodSetting
  [RestApiId](#cfn-apigateway-stage-restapiid): String
  [StageName](#cfn-apigateway-stage-stagename): String
  [Tags](#cfn-apigateway-stage-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TracingEnabled](#cfn-apigateway-stage-tracingenabled): Boolean
  [Variables](#cfn-apigateway-stage-variables): 
    Key : Value
```

## Properties<a name="aws-resource-apigateway-stage-properties"></a>

`AccessLogSetting`  <a name="cfn-apigateway-stage-accesslogsetting"></a>
Access log settings, including the access log format and access log destination ARN\.  
*Required*: No  
*Type*: [AccessLogSetting](aws-properties-apigateway-stage-accesslogsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheClusterEnabled`  <a name="cfn-apigateway-stage-cacheclusterenabled"></a>
Specifies whether a cache cluster is enabled for the stage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheClusterSize`  <a name="cfn-apigateway-stage-cacheclustersize"></a>
The stage's cache capacity in GB\. For more information about choosing a cache size, see [Enabling API caching to enhance responsiveness](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `0.5 | 1.6 | 118 | 13.5 | 237 | 28.4 | 58.2 | 6.1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CanarySetting`  <a name="cfn-apigateway-stage-canarysetting"></a>
Settings for the canary deployment in this stage\.  
*Required*: No  
*Type*: [CanarySetting](aws-properties-apigateway-stage-canarysetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCertificateId`  <a name="cfn-apigateway-stage-clientcertificateid"></a>
The identifier of a client certificate for an API stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentId`  <a name="cfn-apigateway-stage-deploymentid"></a>
The identifier of the Deployment that the stage points to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigateway-stage-description"></a>
The stage's description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentationVersion`  <a name="cfn-apigateway-stage-documentationversion"></a>
The version of the associated API documentation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MethodSettings`  <a name="cfn-apigateway-stage-methodsettings"></a>
A map that defines the method settings for a Stage resource\. Keys \(designated as `/{method_setting_key` below\) are method paths defined as `{resource_path}/{http_method}` for an individual method override, or `/\*/\*` for overriding all methods in the stage\.   
*Required*: No  
*Type*: List of [MethodSetting](aws-properties-apigateway-stage-methodsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-stage-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageName`  <a name="cfn-apigateway-stage-stagename"></a>
The name of the stage is the first path segment in the Uniform Resource Identifier \(URI\) of a call to API Gateway\. Stage names can only contain alphanumeric characters, hyphens, and underscores\. Maximum length is 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apigateway-stage-tags"></a>
The collection of tags\. Each tag element is associated with a given resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TracingEnabled`  <a name="cfn-apigateway-stage-tracingenabled"></a>
Specifies whether active tracing with X\-ray is enabled for the Stage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variables`  <a name="cfn-apigateway-stage-variables"></a>
A map \(string\-to\-string map\) that defines the stage variables, where the variable name is the key and the variable value is the value\. Variable names are limited to alphanumeric characters\. Values must match the following regular expression: `[A-Za-z0-9-._~:/?#&=,]+`\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-stage-return-values"></a>

### Ref<a name="aws-resource-apigateway-stage-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the stage, such as `MyTestStage`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-stage--examples"></a>



### Create stage<a name="aws-resource-apigateway-stage--examples--Create_stage"></a>

The following example creates a stage for the `TestDeployment` deployment\. The stage also specifies method settings for the `MyRestApi` API\.

#### JSON<a name="aws-resource-apigateway-stage--examples--Create_stage--json"></a>

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
                        "DataTraceEnabled": "false"
                    },
                    {
                        "ResourcePath": "/stack",
                        "HttpMethod": "POST",
                        "MetricsEnabled": "true",
                        "DataTraceEnabled": "false",
                        "ThrottlingBurstLimit": "999"
                    },
                    {
                        "ResourcePath": "/stack",
                        "HttpMethod": "GET",
                        "MetricsEnabled": "true",
                        "DataTraceEnabled": "false",
                        "ThrottlingBurstLimit": "555"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-stage--examples--Create_stage--yaml"></a>

```
Resources:
  Prod:
    Type: AWS::ApiGateway::Stage
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
          DataTraceEnabled: 'false'
        - ResourcePath: /stack
          HttpMethod: POST
          MetricsEnabled: 'true'
          DataTraceEnabled: 'false'
          ThrottlingBurstLimit: '999'
        - ResourcePath: /stack
          HttpMethod: GET
          MetricsEnabled: 'true'
          DataTraceEnabled: 'false'
          ThrottlingBurstLimit: '555'
```

## See also<a name="aws-resource-apigateway-stage--seealso"></a>
+ [stage:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateStage.html) in the *Amazon API Gateway REST API Reference*

