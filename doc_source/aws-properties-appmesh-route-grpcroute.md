# AWS::AppMesh::Route GrpcRoute<a name="aws-properties-appmesh-route-grpcroute"></a>

An object that represents a gRPC route type\.

## Syntax<a name="aws-properties-appmesh-route-grpcroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-grpcroute-syntax.json"></a>

```
{
  "[Action](#cfn-appmesh-route-grpcroute-action)" : GrpcRouteAction,
  "[Match](#cfn-appmesh-route-grpcroute-match)" : GrpcRouteMatch,
  "[RetryPolicy](#cfn-appmesh-route-grpcroute-retrypolicy)" : GrpcRetryPolicy,
  "[Timeout](#cfn-appmesh-route-grpcroute-timeout)" : GrpcTimeout
}
```

### YAML<a name="aws-properties-appmesh-route-grpcroute-syntax.yaml"></a>

```
  [Action](#cfn-appmesh-route-grpcroute-action): 
    GrpcRouteAction
  [Match](#cfn-appmesh-route-grpcroute-match): 
    GrpcRouteMatch
  [RetryPolicy](#cfn-appmesh-route-grpcroute-retrypolicy): 
    GrpcRetryPolicy
  [Timeout](#cfn-appmesh-route-grpcroute-timeout): 
    GrpcTimeout
```

## Properties<a name="aws-properties-appmesh-route-grpcroute-properties"></a>

`Action`  <a name="cfn-appmesh-route-grpcroute-action"></a>
An object that represents the action to take if a match is determined\.  
*Required*: Yes  
*Type*: [GrpcRouteAction](aws-properties-appmesh-route-grpcrouteaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-route-grpcroute-match"></a>
An object that represents the criteria for determining a request match\.  
*Required*: Yes  
*Type*: [GrpcRouteMatch](aws-properties-appmesh-route-grpcroutematch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryPolicy`  <a name="cfn-appmesh-route-grpcroute-retrypolicy"></a>
An object that represents a retry policy\.  
*Required*: No  
*Type*: [GrpcRetryPolicy](aws-properties-appmesh-route-grpcretrypolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-appmesh-route-grpcroute-timeout"></a>
An object that represents types of timeouts\.   
*Required*: No  
*Type*: [GrpcTimeout](aws-properties-appmesh-route-grpctimeout.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)