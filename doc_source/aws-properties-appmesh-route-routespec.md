# AWS::AppMesh::Route RouteSpec<a name="aws-properties-appmesh-route-routespec"></a>

An object representing the specification of a route\.

## Syntax<a name="aws-properties-appmesh-route-routespec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-routespec-syntax.json"></a>

```
{
  "[HttpRoute](#cfn-appmesh-route-routespec-httproute)" : [HttpRoute](aws-properties-appmesh-route-httproute.md),
  "[TcpRoute](#cfn-appmesh-route-routespec-tcproute)" : [TcpRoute](aws-properties-appmesh-route-tcproute.md)
}
```

### YAML<a name="aws-properties-appmesh-route-routespec-syntax.yaml"></a>

```
  [HttpRoute](#cfn-appmesh-route-routespec-httproute): 
    [HttpRoute](aws-properties-appmesh-route-httproute.md)
  [TcpRoute](#cfn-appmesh-route-routespec-tcproute): 
    [TcpRoute](aws-properties-appmesh-route-tcproute.md)
```

## Properties<a name="aws-properties-appmesh-route-routespec-properties"></a>

`HttpRoute`  <a name="cfn-appmesh-route-routespec-httproute"></a>
The HTTP routing information for the route\.  
*Required*: No  
*Type*: [HttpRoute](aws-properties-appmesh-route-httproute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TcpRoute`  <a name="cfn-appmesh-route-routespec-tcproute"></a>
The TCP routing information for the route\.  
*Required*: No  
*Type*: [TcpRoute](aws-properties-appmesh-route-tcproute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)