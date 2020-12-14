# AWS::ApiGatewayV2::Stage<a name="aws-resource-apigatewayv2-stage"></a>

The `AWS::ApiGatewayV2::Stage` resource updates a stage for an API\.

## Syntax<a name="aws-resource-apigatewayv2-stage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-stage-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Stage",
  "Properties" : {
      "[AccessLogSettings](#cfn-apigatewayv2-stage-accesslogsettings)" : AccessLogSettings,
      "[ApiId](#cfn-apigatewayv2-stage-apiid)" : String,
      "[AutoDeploy](#cfn-apigatewayv2-stage-autodeploy)" : Boolean,
      "[ClientCertificateId](#cfn-apigatewayv2-stage-clientcertificateid)" : String,
      "[DefaultRouteSettings](#cfn-apigatewayv2-stage-defaultroutesettings)" : RouteSettings,
      "[DeploymentId](#cfn-apigatewayv2-stage-deploymentid)" : String,
      "[Description](#cfn-apigatewayv2-stage-description)" : String,
      "[RouteSettings](#cfn-apigatewayv2-stage-routesettings)" : Json,
      "[StageName](#cfn-apigatewayv2-stage-stagename)" : String,
      "[StageVariables](#cfn-apigatewayv2-stage-stagevariables)" : Json,
      "[Tags](#cfn-apigatewayv2-stage-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-stage-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Stage
Properties: 
  [AccessLogSettings](#cfn-apigatewayv2-stage-accesslogsettings): 
    AccessLogSettings
  [ApiId](#cfn-apigatewayv2-stage-apiid): String
  [AutoDeploy](#cfn-apigatewayv2-stage-autodeploy): Boolean
  [ClientCertificateId](#cfn-apigatewayv2-stage-clientcertificateid): String
  [DefaultRouteSettings](#cfn-apigatewayv2-stage-defaultroutesettings): 
    RouteSettings
  [DeploymentId](#cfn-apigatewayv2-stage-deploymentid): String
  [Description](#cfn-apigatewayv2-stage-description): String
  [RouteSettings](#cfn-apigatewayv2-stage-routesettings): Json
  [StageName](#cfn-apigatewayv2-stage-stagename): String
  [StageVariables](#cfn-apigatewayv2-stage-stagevariables): Json
  [Tags](#cfn-apigatewayv2-stage-tags): Json
```

## Properties<a name="aws-resource-apigatewayv2-stage-properties"></a>

`AccessLogSettings`  <a name="cfn-apigatewayv2-stage-accesslogsettings"></a>
Settings for logging access in this stage\.  
*Required*: No  
*Type*: [AccessLogSettings](aws-properties-apigatewayv2-stage-accesslogsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApiId`  <a name="cfn-apigatewayv2-stage-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoDeploy`  <a name="cfn-apigatewayv2-stage-autodeploy"></a>
Specifies whether updates to an API automatically trigger a new deployment\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCertificateId`  <a name="cfn-apigatewayv2-stage-clientcertificateid"></a>
The identifier of a client certificate for a `Stage`\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultRouteSettings`  <a name="cfn-apigatewayv2-stage-defaultroutesettings"></a>
The default route settings for the stage\.  
*Required*: No  
*Type*: [RouteSettings](aws-properties-apigatewayv2-stage-routesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentId`  <a name="cfn-apigatewayv2-stage-deploymentid"></a>
The deployment identifier for the API stage\. Can't be updated if `autoDeploy` is enabled\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-stage-description"></a>
The description for the API stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteSettings`  <a name="cfn-apigatewayv2-stage-routesettings"></a>
Route settings for the stage\.  
*Required*: No  
*Type*: [Json](aws-properties-apigatewayv2-stage-routesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageName`  <a name="cfn-apigatewayv2-stage-stagename"></a>
The stage name\. Stage names can contain only alphanumeric characters, hyphens, and underscores, or be `$default`\. Maximum length is 128 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageVariables`  <a name="cfn-apigatewayv2-stage-stagevariables"></a>
A map that defines the stage variables for a `Stage`\. Variable names can have alphanumeric and underscore characters, and the values must match \[A\-Za\-z0\-9\-\.\_\~:/?\#&=,\]\+\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigatewayv2-stage-tags"></a>
The collection of tags\. Each tag element is associated with a given resource\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-stage-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-stage-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the stage name, such as `MyTestStage`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-stage--examples"></a>



### Stage creation example<a name="aws-resource-apigatewayv2-stage--examples--Stage_creation_example"></a>

The following example creates a `stage` resource called `MyStage` and associates it with an existing `deployment` called `MyDeployment`\.

#### JSON<a name="aws-resource-apigatewayv2-stage--examples--Stage_creation_example--json"></a>

```
{
    "MyStage": {
        "Type": "AWS::ApiGatewayV2::Stage",
        "Properties": {
            "StageName": "Prod",
            "Description": "Prod Stage",
            "DeploymentId": {
                "Ref": "MyDeployment"
            },
            "ApiId": {
                "Ref": "CFNWebSocket"
            },
            "DefaultRouteSettings": {
                "DetailedMetricsEnabled": true,
                "LoggingLevel": "INFO",
                "DataTraceEnabled": false,
                "ThrottlingBurstLimit": 10,
                "ThrottlingRateLimit": 10
            },
            "AccessLogSettings": {
                "DestinationArn": "arn:aws:logs:us-east-1:123456789:log-group:my-log-group",
                "Format": "{\"requestId\":\"$context.requestId\", \"ip\": \"$context.identity.sourceIp\", \"caller\":\"$context.identity.caller\", \"user\":\"$context.identity.user\",\"requestTime\":\"$context.requestTime\", \"eventType\":\"$context.eventType\",\"routeKey\":\"$context.routeKey\", \"status\":\"$context.status\",\"connectionId\":\"$context.connectionId\"}"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-stage--examples--Stage_creation_example--yaml"></a>

```
MyStage:
  Type: 'AWS::ApiGatewayV2::Stage'
  Properties:
    StageName: Prod
    Description: Prod Stage
    DeploymentId: !Ref MyDeployment
    ApiId: !Ref CFNWebSocket
    DefaultRouteSettings:
      DetailedMetricsEnabled: true
      LoggingLevel: INFO
      DataTraceEnabled: false
      ThrottlingBurstLimit: 10
      ThrottlingRateLimit: 10
    AccessLogSettings:
      DestinationArn: 'arn:aws:logs:us-east-1:123456789:log-group:my-log-group'
      Format: >-
        {"requestId":"$context.requestId", "ip": "$context.identity.sourceIp",
        "caller":"$context.identity.caller",
        "user":"$context.identity.user","requestTime":"$context.requestTime",
        "eventType":"$context.eventType","routeKey":"$context.routeKey",
        "status":"$context.status","connectionId":"$context.connectionId"}
```

## See also<a name="aws-resource-apigatewayv2-stage--seealso"></a>
+ [CreateStage](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-stages.html#CreateStage) in the *Amazon API Gateway Version 2 API Reference*

