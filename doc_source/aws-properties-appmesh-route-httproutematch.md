# AWS::AppMesh::Route HttpRouteMatch<a name="aws-properties-appmesh-route-httproutematch"></a>

An object that represents the requirements for a route to match HTTP requests for a virtual router\.

## Syntax<a name="aws-properties-appmesh-route-httproutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httproutematch-syntax.json"></a>

```
{
  "[Headers](#cfn-appmesh-route-httproutematch-headers)" : [ HttpRouteHeader, ... ],
  "[Method](#cfn-appmesh-route-httproutematch-method)" : String,
  "[Path](#cfn-appmesh-route-httproutematch-path)" : HttpPathMatch,
  "[Port](#cfn-appmesh-route-httproutematch-port)" : Integer,
  "[Prefix](#cfn-appmesh-route-httproutematch-prefix)" : String,
  "[QueryParameters](#cfn-appmesh-route-httproutematch-queryparameters)" : [ QueryParameter, ... ],
  "[Scheme](#cfn-appmesh-route-httproutematch-scheme)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-httproutematch-syntax.yaml"></a>

```
  [Headers](#cfn-appmesh-route-httproutematch-headers): 
    - HttpRouteHeader
  [Method](#cfn-appmesh-route-httproutematch-method): String
  [Path](#cfn-appmesh-route-httproutematch-path): 
    HttpPathMatch
  [Port](#cfn-appmesh-route-httproutematch-port): Integer
  [Prefix](#cfn-appmesh-route-httproutematch-prefix): String
  [QueryParameters](#cfn-appmesh-route-httproutematch-queryparameters): 
    - QueryParameter
  [Scheme](#cfn-appmesh-route-httproutematch-scheme): String
```

## Properties<a name="aws-properties-appmesh-route-httproutematch-properties"></a>

`Headers`  <a name="cfn-appmesh-route-httproutematch-headers"></a>
The client request headers to match on\.  
*Required*: No  
*Type*: List of [HttpRouteHeader](aws-properties-appmesh-route-httprouteheader.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-appmesh-route-httproutematch-method"></a>
The client request method to match on\. Specify only one\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONNECT | DELETE | GET | HEAD | OPTIONS | PATCH | POST | PUT | TRACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-appmesh-route-httproutematch-path"></a>
The client request path to match on\.  
*Required*: No  
*Type*: [HttpPathMatch](aws-properties-appmesh-route-httppathmatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-appmesh-route-httproutematch-port"></a>
The port number to match on\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-route-httproutematch-prefix"></a>
Specifies the path to match requests with\. This parameter must always start with `/`, which by itself matches all requests to the virtual service name\. You can also match for path\-based routing of requests\. For example, if your virtual service name is `my-service.local` and you want the route to match requests to `my-service.local/metrics`, your prefix should be `/metrics`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryParameters`  <a name="cfn-appmesh-route-httproutematch-queryparameters"></a>
The client request query parameters to match on\.  
*Required*: No  
*Type*: List of [QueryParameter](aws-properties-appmesh-route-queryparameter.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scheme`  <a name="cfn-appmesh-route-httproutematch-scheme"></a>
The client request scheme to match on\. Specify only one\. Applicable only for HTTP2 routes\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)