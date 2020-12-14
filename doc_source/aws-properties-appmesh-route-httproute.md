# AWS::AppMesh::Route HttpRoute<a name="aws-properties-appmesh-route-httproute"></a>

An object that represents an HTTP or HTTP/2 route type\.

## Syntax<a name="aws-properties-appmesh-route-httproute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httproute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-route-httproute-action)" : HttpRouteAction,
  "[Match](#cfn-appmesh-route-httproute-match)" : HttpRouteMatch,
  "[RetryPolicy](#cfn-appmesh-route-httproute-retrypolicy)" : HttpRetryPolicy,
  "[Timeout](#cfn-appmesh-route-httproute-timeout)" : HttpTimeout
}
```

### YAML<a name="aws-properties-appmesh-route-httproute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-route-httproute-action): 
    HttpRouteAction
  [Match](#cfn-appmesh-route-httproute-match): 
    HttpRouteMatch
  [RetryPolicy](#cfn-appmesh-route-httproute-retrypolicy): 
    HttpRetryPolicy
  [Timeout](#cfn-appmesh-route-httproute-timeout): 
    HttpTimeout
```

## Properties<a name="aws-properties-appmesh-route-httproute-properties"></a>

`Action`  <a name="cfn-appmesh-route-httproute-action"></a>
An object that represents the action to take if a match is determined\.  
*Required*: Yes  
*Type*: [HttpRouteAction](aws-properties-appmesh-route-httprouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-route-httproute-match"></a>
An object that represents the criteria for determining a request match\.  
*Required*: Yes  
*Type*: [HttpRouteMatch](aws-properties-appmesh-route-httproutematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-appmesh-route-httproute-retrypolicy"></a>
An object that represents a retry policy\.  
*Required*: No  
*Type*: [HttpRetryPolicy](aws-properties-appmesh-route-httpretrypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-appmesh-route-httproute-timeout"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [HttpTimeout](aws-properties-appmesh-route-httptimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)