# AWS::AppMesh::Route TcpRouteMatch<a name="aws-properties-appmesh-route-tcproutematch"></a>

An object representing the TCP route to match\.

## Syntax<a name="aws-properties-appmesh-route-tcproutematch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tcproutematch-syntax.json"></a>

```
{
  "[Port](#cfn-appmesh-route-tcproutematch-port)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-route-tcproutematch-syntax.yaml"></a>

```
  [Port](#cfn-appmesh-route-tcproutematch-port): Integer
```

## Properties<a name="aws-properties-appmesh-route-tcproutematch-properties"></a>

`Port`  <a name="cfn-appmesh-route-tcproutematch-port"></a>
The port number to match on\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)