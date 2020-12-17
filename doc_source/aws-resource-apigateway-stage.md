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
Specifies settings for logging access in this stage\.  
*Required*: No  
*Type*: [AccessLogSetting](aws-properties-apigateway-stage-accesslogsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheClusterEnabled`  <a name="cfn-apigateway-stage-cacheclusterenabled"></a>
Indicates whether cache clustering is enabled for the stage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheClusterSize`  <a name="cfn-apigateway-stage-cacheclustersize"></a>
The stage's cache cluster size\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CanarySetting`  <a name="cfn-apigateway-stage-canarysetting"></a>
Specifies settings for the canary deployment in this stage\.  
*Required*: No  
*Type*: [CanarySetting](aws-properties-apigateway-stage-canarysetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCertificateId`  <a name="cfn-apigateway-stage-clientcertificateid"></a>
The ID of the client certificate that API Gateway uses to call your integration endpoints in the stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentId`  <a name="cfn-apigateway-stage-deploymentid"></a>
The ID of the deployment that the stage is associated with\. This parameter is required to create a stage\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigateway-stage-description"></a>
A description of the stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentationVersion`  <a name="cfn-apigateway-stage-documentationversion"></a>
The version ID of the API documentation snapshot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MethodSettings`  <a name="cfn-apigateway-stage-methodsettings"></a>
Settings for all methods in the stage\.  
*Required*: No  
*Type*: List of [MethodSetting](aws-properties-apitgateway-stage-methodsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-stage-restapiid"></a>
The ID of the `RestApi` resource that you're deploying with this stage\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageName`  <a name="cfn-apigateway-stage-stagename"></a>
The name of the stage, which API Gateway uses as the first path segment in the invoked Uniform Resource Identifier \(URI\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apigateway-stage-tags"></a>
An array of arbitrary tags \(key\-value pairs\) to associate with the stage\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TracingEnabled`  <a name="cfn-apigateway-stage-tracingenabled"></a>
Specifies whether active X\-Ray tracing is enabled for this stage\.  
For more information, see [Trace API Gateway API Execution with AWS X\-Ray](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-xray.html) in the *API Gateway Developer Guide*\.  
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
+ [stage:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/stage-create/) in the *Amazon API Gateway REST API Reference*

