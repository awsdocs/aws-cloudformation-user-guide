# AWS::AppMesh::Route HttpRouteMatch<a name="aws-properties-appmesh-route-httproutematch"></a>

An object representing the requirements for a route to match HTTP requests for a virtual router\.

## Syntax<a name="aws-properties-appmesh-route-httproutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httproutematch-syntax.json"></a>

```
{
  "[Headers](#cfn-appmesh-route-httproutematch-headers)" : [ [HttpRouteHeader](aws-properties-appmesh-route-httprouteheader.md), ... ],
  "[Method](#cfn-appmesh-route-httproutematch-method)" : String,
  "[Prefix](#cfn-appmesh-route-httproutematch-prefix)" : String,
  "[Scheme](#cfn-appmesh-route-httproutematch-scheme)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-httproutematch-syntax.yaml"></a>

```
  [Headers](#cfn-appmesh-route-httproutematch-headers): 
    - [HttpRouteHeader](aws-properties-appmesh-route-httprouteheader.md)
  [Method](#cfn-appmesh-route-httproutematch-method): String
  [Prefix](#cfn-appmesh-route-httproutematch-prefix): String
  [Scheme](#cfn-appmesh-route-httproutematch-scheme): String
```

## Properties<a name="aws-properties-appmesh-route-httproutematch-properties"></a>

`Headers`  <a name="cfn-appmesh-route-httproutematch-headers"></a>
The client request headers to match on\.  
*Required*: No  
*Type*: List of [HttpRouteHeader](aws-properties-appmesh-route-httprouteheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-appmesh-route-httproutematch-method"></a>
The client request header method to match on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-route-httproutematch-prefix"></a>
Specifies the path to match requests with\. This parameter must always start with `/`, which by itself matches all requests to the virtual service name\. You can also match for path\-based routing of requests\. For example, if your virtual service name is `my-service.local` and you want the route to match requests to `my-service.local/metrics`, your prefix should be `/metrics`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scheme`  <a name="cfn-appmesh-route-httproutematch-scheme"></a>
The client request header scheme to match on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)