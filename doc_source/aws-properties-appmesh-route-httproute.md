# AWS::AppMesh::Route HttpRoute<a name="aws-properties-appmesh-route-httproute"></a>

An object representing the HTTP routing specification for a route\.

## Syntax<a name="aws-properties-appmesh-route-httproute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httproute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-route-httproute-action)" : [HttpRouteAction](aws-properties-appmesh-route-httprouteaction.md),
  "[Match](#cfn-appmesh-route-httproute-match)" : [HttpRouteMatch](aws-properties-appmesh-route-httproutematch.md),
  "[RetryPolicy](#cfn-appmesh-route-httproute-retrypolicy)" : [HttpRetryPolicy](aws-properties-appmesh-route-httpretrypolicy.md)
}
```

### YAML<a name="aws-properties-appmesh-route-httproute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-route-httproute-action): 
    [HttpRouteAction](aws-properties-appmesh-route-httprouteaction.md)
  [Match](#cfn-appmesh-route-httproute-match): 
    [HttpRouteMatch](aws-properties-appmesh-route-httproutematch.md)
  [RetryPolicy](#cfn-appmesh-route-httproute-retrypolicy): 
    [HttpRetryPolicy](aws-properties-appmesh-route-httpretrypolicy.md)
```

## Properties<a name="aws-properties-appmesh-route-httproute-properties"></a>

`Action`  <a name="cfn-appmesh-route-httproute-action"></a>
The action to take if a match is determined\.  
*Required*: Yes  
*Type*: [HttpRouteAction](aws-properties-appmesh-route-httprouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-route-httproute-match"></a>
The criteria for determining an HTTP request match\.  
*Required*: Yes  
*Type*: [HttpRouteMatch](aws-properties-appmesh-route-httproutematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-appmesh-route-httproute-retrypolicy"></a>
An object that represents a retry policy\.  
*Required*: No  
*Type*: [HttpRetryPolicy](aws-properties-appmesh-route-httpretrypolicy.md)  
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
