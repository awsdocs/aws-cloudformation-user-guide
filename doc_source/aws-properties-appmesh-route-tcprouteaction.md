# AWS::AppMesh::Route TcpRouteAction<a name="aws-properties-appmesh-route-tcprouteaction"></a>

An object that represents the action to take if a match is determined\.

## Syntax<a name="aws-properties-appmesh-route-tcprouteaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tcprouteaction-syntax.json"></a>

```
{
  "[WeightedTargets](#cfn-appmesh-route-tcprouteaction-weightedtargets)" : [ WeightedTarget, ... ]
}
```

### YAML<a name="aws-properties-appmesh-route-tcprouteaction-syntax.yaml"></a>

```
  [WeightedTargets](#cfn-appmesh-route-tcprouteaction-weightedtargets): 
    - WeightedTarget
```

## Properties<a name="aws-properties-appmesh-route-tcprouteaction-properties"></a>

`WeightedTargets`  <a name="cfn-appmesh-route-tcprouteaction-weightedtargets"></a>
An object that represents the targets that traffic is routed to when a request matches the route\.  
*Required*: Yes  
*Type*: List of [WeightedTarget](aws-properties-appmesh-route-weightedtarget.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)