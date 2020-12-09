# AWS::AppMesh::Route TcpRoute<a name="aws-properties-appmesh-route-tcproute"></a>

An object that represents a TCP route type\.

## Syntax<a name="aws-properties-appmesh-route-tcproute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tcproute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-route-tcproute-action)" : TcpRouteAction,
  "[Timeout](#cfn-appmesh-route-tcproute-timeout)" : TcpTimeout
}
```

### YAML<a name="aws-properties-appmesh-route-tcproute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-route-tcproute-action): 
    TcpRouteAction
  [Timeout](#cfn-appmesh-route-tcproute-timeout): 
    TcpTimeout
```

## Properties<a name="aws-properties-appmesh-route-tcproute-properties"></a>

`Action`  <a name="cfn-appmesh-route-tcproute-action"></a>
The action to take if a match is determined\.  
*Required*: Yes  
*Type*: [TcpRouteAction](aws-properties-appmesh-route-tcprouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-appmesh-route-tcproute-timeout"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [TcpTimeout](aws-properties-appmesh-route-tcptimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)