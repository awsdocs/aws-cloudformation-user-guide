# AWS::AppMesh::Route HttpRouteAction<a name="aws-properties-appmesh-route-httprouteaction"></a>

An object representing the traffic distribution requirements for matched HTTP requests\.

## Syntax<a name="aws-properties-appmesh-route-httprouteaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httprouteaction-syntax.json"></a>

```
{
  "[WeightedTargets](#cfn-appmesh-route-httprouteaction-weightedtargets)" : [ [WeightedTarget](aws-properties-appmesh-route-weightedtarget.md), ... ]
}
```

### YAML<a name="aws-properties-appmesh-route-httprouteaction-syntax.yaml"></a>

```
  [WeightedTargets](#cfn-appmesh-route-httprouteaction-weightedtargets): 
    - [WeightedTarget](aws-properties-appmesh-route-weightedtarget.md)
```

## Properties<a name="aws-properties-appmesh-route-httprouteaction-properties"></a>

`WeightedTargets`  <a name="cfn-appmesh-route-httprouteaction-weightedtargets"></a>
The targets that traffic is routed to when a request matches the route\. You can specify one or more targets and their relative weights to distribute traffic with\.  
*Required*: Yes  
*Type*: List of [WeightedTarget](aws-properties-appmesh-route-weightedtarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)