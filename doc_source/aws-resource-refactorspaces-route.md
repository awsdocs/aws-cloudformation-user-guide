# AWS::RefactorSpaces::Route<a name="aws-resource-refactorspaces-route"></a>

Creates an AWS Migration Hub Refactor Spaces route\. The account owner of the service resource is always the environment owner, regardless of which account creates the route\. Routes target a service in the application\. If an application does not have any routes, then the first route must be created as a `DEFAULT` `RouteType`\.

When created, the default route defaults to an active state so state is not a required input\. However, like all other state values the state of the default route can be updated after creation, but only when all other routes are also inactive\. Conversely, no route can be active without the default route also being active\.

**Note**  
 In the `AWS::RefactorSpaces::Route` resource, you can only update the `ActivationState` property, which resides under the `UriPathRoute` and `DefaultRoute` properties\. All other properties associated with the `AWS::RefactorSpaces::Route` cannot be updated, even though the property description might indicate otherwise\. Updating all other properties will result in the replacement of Route\. 

When you create a route, Refactor Spaces configures the Amazon API Gateway to send traffic to the target service as follows:
+ **URL Endpoints**

  If the service has a URL endpoint, and the endpoint resolves to a private IP address, Refactor Spaces routes traffic using the API Gateway VPC link\. If a service endpoint resolves to a public IP address, Refactor Spaces routes traffic over the public internet\. Services can have HTTP or HTTPS URL endpoints\. For HTTPS URLs, publicly\-signed certificates are supported\. Private Certificate Authorities \(CAs\) are permitted only if the CA's domain is also publicly resolvable\. 

  Refactor Spaces automatically resolves the public Domain Name System \(DNS\) names that are set in `CreateService:UrlEndpoint `when you create a service\. The DNS names resolve when the DNS time\-to\-live \(TTL\) expires, or every 60 seconds for TTLs less than 60 seconds\. This periodic DNS resolution ensures that the route configuration remains up\-to\-date\. 

  

  **One\-time health check**

  A one\-time health check is performed on the service when either the route is updated from inactive to active, or when it is created with an active state\. If the health check fails, the route transitions the route state to `FAILED`, an error code of `SERVICE_ENDPOINT_HEALTH_CHECK_FAILURE` is provided, and no traffic is sent to the service\.

  For private URLs, a target group is created on the Network Load Balancer and the load balancer target group runs default target health checks\. By default, the health check is run against the service endpoint URL\. Optionally, the health check can be performed against a different protocol, port, and/or path using the [CreateService:UrlEndpoint](https://docs.aws.amazon.com/migrationhub-refactor-spaces/latest/APIReference/API_CreateService.html#migrationhubrefactorspaces-CreateService-request-UrlEndpoint) parameter\. All other health check settings for the load balancer use the default values described in the [Health checks for your target groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) in the *Elastic Load Balancing guide*\. The health check is considered successful if at least one target within the target group transitions to a healthy state\.

  
+ **AWS Lambda function endpoints**

  If the service has an AWS Lambda function endpoint, then Refactor Spaces configures the Lambda function's resource policy to allow the application's API Gateway to invoke the function\.

  The Lambda function state is checked\. If the function is not active, the function configuration is updated so that Lambda resources are provisioned\. If the Lambda state is `Failed`, then the route creation fails\. For more information, see the [GetFunctionConfiguration's State response parameter](https://docs.aws.amazon.com/lambda/latest/dg/API_GetFunctionConfiguration.html#SSS-GetFunctionConfiguration-response-State) in the *AWS Lambda Developer Guide*\.

  A check is performed to determine that a Lambda function with the specified ARN exists\. If it does not exist, the health check fails\. For public URLs, a connection is opened to the public endpoint\. If the URL is not reachable, the health check fails\. 

**Environments without a network bridge**

When you create environments without a network bridge \([CreateEnvironment:NetworkFabricType](https://docs.aws.amazon.com/migrationhub-refactor-spaces/latest/APIReference/API_CreateEnvironment.html#migrationhubrefactorspaces-CreateEnvironment-request-NetworkFabricType) is `NONE)` and you use your own networking infrastructure, you need to configure [VPC to VPC connectivity](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/amazon-vpc-to-amazon-vpc-connectivity-options.html) between your network and the application proxy VPC\. Route creation from the application proxy to service endpoints will fail if your network is not configured to connect to the application proxy VPC\. For more information, see [ Create a route](https://docs.aws.amazon.com/migrationhub-refactor-spaces/latest/userguide/getting-started-create-role.html) in the *Refactor Spaces User Guide*\.



## Syntax<a name="aws-resource-refactorspaces-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-refactorspaces-route-syntax.json"></a>

```
{
  "Type" : "AWS::RefactorSpaces::Route",
  "Properties" : {
      "[ApplicationIdentifier](#cfn-refactorspaces-route-applicationidentifier)" : String,
      "[DefaultRoute](#cfn-refactorspaces-route-defaultroute)" : DefaultRouteInput,
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
  [DefaultRoute](#cfn-refactorspaces-route-defaultroute): 
    DefaultRouteInput
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

`DefaultRoute`  <a name="cfn-refactorspaces-route-defaultroute"></a>
 Configuration for the default route type\.   
*Required*: No  
*Type*: [DefaultRouteInput](aws-properties-refactorspaces-route-defaultrouteinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentIdentifier`  <a name="cfn-refactorspaces-route-environmentidentifier"></a>
The unique identifier of the environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteType`  <a name="cfn-refactorspaces-route-routetype"></a>
The route type of the route\.   
*Required*: Yes  
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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