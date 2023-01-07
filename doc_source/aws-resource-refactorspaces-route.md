# AWS::RefactorSpaces::Route<a name="aws-resource-refactorspaces-route"></a>

Creates an AWS Migration Hub Refactor Spaces route\. The account owner of the service resource is always the environment owner, regardless of the account creating the route\. Routes target a service in the application\. If an application does not have any routes, then the first route must be created as a `DEFAULT` `RouteType`\.

**Note**  
In the `AWS::RefactorSpaces::Route` resource, you can only update the `SourcePath` and `Methods` properties, which reside under the `UriPathRoute` property\. All other properties associated with the `AWS::RefactorSpaces::Route` cannot be updated, even though the property description might indicate otherwise\.

When you create a route, Refactor Spaces configures the Amazon API Gateway to send traffic to the target service\.
+ If the service has a URL endpoint, and the endpoint resolves to a private IP address, Refactor Spaces routes traffic using the API Gateway VPC link\. 
+ If the service has a URL endpoint, and the endpoint resolves to a public IP address, Refactor Spaces routes traffic over the public internet\.
+ If the service has a AWS Lambda function endpoint, then Refactor Spaces uses API Gateway’s Lambda integration\.

A health check is performed on the service when the route is created\. If the health check fails, the route transitions to `FAILED`, and no traffic is sent to the service\. For Lambda functions, the Lambda function state is checked\. If the function is not active, the function configuration is updated so Lambda resources are provisioned\. If the Lambda state is `Failed`, then the route creation fails\. For more information, see the [GetFunctionConfiguration's State response parameter](https://docs.aws.amazon.com/lambda/latest/dg/API_GetFunctionConfiguration.html#SSS-GetFunctionConfiguration-response-State) in the *AWS Lambda Developer Guide*\. For public URLs, a connection is opened to the public endpoint\. If the URL is not reachable, the health check fails\. For private URLs, a target groups is created and the target group health check is run\. The `HealthCheckProtocol`, `HealthCheckPort`, and `HealthCheckPath` are the same protocol, port, and path specified in the URL or Health URL if used\. All other settings use the default values, as described in [Health checks for your target groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html)\. The health check is considered successful if at least one target within the target group transitions to healthy state\.

## Syntax<a name="aws-resource-refactorspaces-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-refactorspaces-route-syntax.json"></a>

```
{
  "Type" : "AWS::RefactorSpaces::Route",
  "Properties" : {
      "[ApplicationIdentifier](#cfn-refactorspaces-route-applicationidentifier)" : String,
      "[EnvironmentIdentifier](#cfn-refactorspaces-route-environmentidentifier)" : String,
      "[RouteType](#cfn-refactorspaces-route-routetype)" : String,
      "[ServiceIdentifier](#cfn-refactorspaces-route-serviceidentifier)" : String,
      "[Tags](#cfn-refactorspaces-route-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UriPathRoute](#cfn-refactorspaces-route-uripathroute)" : UriPathRouteInput
    }
}
```

### YAML<a name="aws-resource-refactorspaces-route-syntax.yaml"></a>

```
Type: AWS::RefactorSpaces::Route
Properties: 
  [ApplicationIdentifier](#cfn-refactorspaces-route-applicationidentifier): String
  [EnvironmentIdentifier](#cfn-refactorspaces-route-environmentidentifier): String
  [RouteType](#cfn-refactorspaces-route-routetype): String
  [ServiceIdentifier](#cfn-refactorspaces-route-serviceidentifier): String
  [Tags](#cfn-refactorspaces-route-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UriPathRoute](#cfn-refactorspaces-route-uripathroute): 
    UriPathRouteInput
```

## Properties<a name="aws-resource-refactorspaces-route-properties"></a>

`ApplicationIdentifier`  <a name="cfn-refactorspaces-route-applicationidentifier"></a>
The unique identifier of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnvironmentIdentifier`  <a name="cfn-refactorspaces-route-environmentidentifier"></a>
The unique identifier of the environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteType`  <a name="cfn-refactorspaces-route-routetype"></a>
The route type of the route\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceIdentifier`  <a name="cfn-refactorspaces-route-serviceidentifier"></a>
The unique identifier of the service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-refactorspaces-route-tags"></a>
The tags assigned to the route\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UriPathRoute`  <a name="cfn-refactorspaces-route-uripathroute"></a>
The configuration for the URI path route type\.  
*Required*: No  
*Type*: [UriPathRouteInput](aws-properties-refactorspaces-route-uripathrouteinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-refactorspaces-route-return-values"></a>

### Ref<a name="aws-resource-refactorspaces-route-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a composite ID following this format: `<EnvironmentId>|<ApplicationId>|<RouteId>`, for example, `env-1234654123|app-1234654123|rte-1234654123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-refactorspaces-route-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-refactorspaces-route-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the route\.

`PathResourceToId`  <a name="PathResourceToId-fn::getatt"></a>
A mapping of Amazon API Gateway path resources to resource IDs\.

`RouteIdentifier`  <a name="RouteIdentifier-fn::getatt"></a>
The unique identifier of the route\.