# AWS::ApiGatewayV2::Stage<a name="aws-resource-apigatewayv2-stage"></a>

The `AWS::ApiGatewayV2::Stage` resource creates a stage for an Amazon API Gateway deployment\. For more information, see [CreateStage](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-stages.html#CreateStage) in the *Amazon API Gateway V2 API Reference*\. 

## Syntax<a name="aws-resource-apigatewayv2-stage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-stage-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Stage",
  "Properties" : {
    "[AccessLogSettings](#cfn-apigatewayv2-stage-accesslogsettings)" : [*AccessLogSettings*](aws-properties-apigatewayv2-stage-accesslogsettings.md),
    "[ApiId](#cfn-apigatewayv2-stage-apiid)" : String,
    "[ClientCertificateId](#cfn-apigatewayv2-stage-clientcertificateid)" : String,
    "[DefaultRouteSettings](#cfn-apigatewayv2-stage-defaultroutesettings)" : [*RouteSettings*](aws-properties-apigatewayv2-stage-routesettings.md),
    "[DeploymentId](#cfn-apigatewayv2-stage-deploymentid)" : String,
    "[Description](#cfn-apigatewayv2-stage-description)" : String,
    "[RouteSettings](#cfn-apigatewayv2-stage-routesettings)" : JSON object,
    "[StageName](#cfn-apigatewayv2-stage-stagename)" : String,
    "[StageVariables](#cfn-apigatewayv2-stage-stagevariables)" : JSON object
  }
}
```

### YAML<a name="aws-resource-apigatewayv2-stage-syntax.yaml"></a>

```
Type: "AWS::ApiGatewayV2::Stage"
Properties:
  [AccessLogSettings](#cfn-apigatewayv2-stage-accesslogsettings): 
    [*AccessLogSettings*](aws-properties-apigatewayv2-stage-accesslogsettings.md)
  [ApiId](#cfn-apigatewayv2-stage-apiid): String
  [ClientCertificateId](#cfn-apigatewayv2-stage-clientcertificateid): String
  [DefaultRouteSettings](#cfn-apigatewayv2-stage-defaultroutesettings): 
    [*RouteSettings*](aws-properties-apigatewayv2-stage-routesettings.md)
  [DeploymentId](#cfn-apigatewayv2-stage-deploymentid): String
  [Description](#cfn-apigatewayv2-stage-description): String
  [RouteSettings](#cfn-apigatewayv2-stage-routesettings): JSON object
  [StageName](#cfn-apigatewayv2-stage-stagename): String
  [StageVariables](#cfn-apigatewayv2-stage-stagevariables): JSON object
```

## Properties<a name="aws-resource-apigatewayv2-stage-properties"></a>

`AccessLogSettings`  <a name="cfn-apigatewayv2-stage-accesslogsettings"></a>
Settings for logging access in this stage\.  
 *Required*: No  
 *Type*: [AccessLogSettings](aws-properties-apigatewayv2-stage-accesslogsettings.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApiId`  <a name="cfn-apigatewayv2-stage-apiid"></a>
The API ID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ClientCertificateId`  <a name="cfn-apigatewayv2-stage-clientcertificateid"></a>
The ID of a client certificate for the stage\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeploymentId`  <a name="cfn-apigatewayv2-stage-deploymentid"></a>
The ID of the deployment that the stage is associated with\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DefaultRouteSettings`  <a name="cfn-apigatewayv2-stage-defaultroutesettings"></a>
Default route settings for the stage\.  
 *Required*: No  
 *Type*: [RouteSettings](aws-properties-apigatewayv2-stage-routesettings.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-apigatewayv2-stage-description"></a>
Description of the stage\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RouteSettings`  <a name="cfn-apigatewayv2-stage-routesettings"></a>
Route settings for the stage\. This is a mapping of Strings to RouteSettings\.  
 *Required*: No  
 *Type*: Mapping of key\-value pairs  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StageName`  <a name="cfn-apigatewayv2-stage-stagename"></a>
The name of the stage\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`StageVariables`  <a name="cfn-apigatewayv2-stage-stagevariables"></a>
A String to String mapping that defines the stage variables for a stage resource\. Variable names can have alphanumeric and underscore characters, and the values must match \[A\-Za\-z0\-9\-\.\_\~:/?\#&=,\]\+\.  
 *Required*: No  
 *Type*: Mapping of key\-value pairs  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigatewayv2-stage-returnvalues"></a>

### Ref<a name="aws-resource-apigatewayv2-stage-ref"></a>

When you pass the logical ID of an `AWS::ApiGatewayV2::Stage` resource to the intrinsic `Ref` function, the function returns the stage name, such as `MyTestStage`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-apigatewayv2-stage-examples"></a>

### Stage creation example<a name="aws-resource-apigatewayv2-stage-example1"></a>

The following example creates a `stage` resource called `MyStage` and associates it with an existing `deployment` called `MyDeployment`\.

#### JSON<a name="aws-resource-apigatewayv2-stage-example1.json"></a>

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
                "DataTraceEnabled": true,
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

#### YAML<a name="aws-resource-apigatewayv2-stage-example1.yaml"></a>

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
      DataTraceEnabled: true
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

## See Also<a name="aws-resource-apigatewayv2-stage-seealso"></a>
+  [CreateStage](https://docs.aws.amazon.com//apigatewayv2/latest/api-reference/apis-apiid-stages.html#CreateStage) in the *Amazon API Gateway V2 API Reference* 