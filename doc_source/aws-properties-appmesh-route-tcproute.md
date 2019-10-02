# AWS::AppMesh::Route TcpRoute<a name="aws-properties-appmesh-route-tcproute"></a>

An object representing the TCP routing specification for a route\.

## Syntax<a name="aws-properties-appmesh-route-tcproute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-tcproute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-route-tcproute-action)" : [TcpRouteAction](aws-properties-appmesh-route-tcprouteaction.md)
}
```

### YAML<a name="aws-properties-appmesh-route-tcproute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-route-tcproute-action): 
    [TcpRouteAction](aws-properties-appmesh-route-tcprouteaction.md)
```

## Properties<a name="aws-properties-appmesh-route-tcproute-properties"></a>

`Action`  <a name="cfn-appmesh-route-tcproute-action"></a>
The action to take if a match is determined\.  
*Required*: Yes  
*Type*: [TcpRouteAction](aws-properties-appmesh-route-tcprouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
